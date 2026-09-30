# Lab 1-F · Fallback: agent nad veřejným webem (bez SharePointu)

> Modul: M3 · Odhad: 25 min · Režim: vlastní tenant (BYOS) · Náhrada za [Lab 1](lab-copilot-chat-agent.md) a [Lab 2](lab-sharepoint-agent.md), když není SharePoint Online
> Funguje i v **Copilot Chatu bez licence** — grounding na web nepotřebuje firemní data.

## Cíl

Postavit v Agent Builderu **web-grounded agenta** — agenta, který odpovídá **jen z vybraných veřejných webů** — a otestovat, jestli se zdrojů opravdu drží.

Vzorový scénář: **NIS2 Průvodce** — pomáhá firmě zorientovat se v novém zákoně o kybernetické bezpečnosti (č. 264/2025 Sb.) a ve směrnici NIS2. Téma je aktuální, zdroje jsou veřejné a autoritativní a špatná odpověď je snadno poznat.

## Předpoklady

- Přístup do Agent Builderu (Copilot → **New agent**).
- Nic dalšího — žádný SharePoint, žádné soubory.

> [!NOTE] Proč bez souborů
> Nahrané soubory se v Agent Builderu ukládají do OneDrivu, tedy na SharePoint Online. Bez SharePointu proto zbývá jako zdroj znalostí jen **web**.

## Kroky

### Část A — návrh (5 min)

1. **Pro koho:** IT / bezpečnostní manažer a vedení menší firmy, která nově spadá pod NIS2.
2. **Jaký problém řeší:** „Nevím, jestli pod zákon spadáme, co musíme udělat a do kdy."
3. **Zdroje** (whitelist — nic jiného agent používat nemá):

   | Web | Proč |
   |---|---|
   | `https://portal.nukib.gov.cz` | regulátor — metodiky, registrace, samoposouzení |
   | `https://www.zakonyprolidi.cz` | aktuální znění zákona a vyhlášek |
   | `https://eur-lex.europa.eu` | text směrnice NIS2 (EU 2022/2555) |

4. Zapište si **5 testovacích dotazů** (hotové jsou v části C).

### Část B — stavba (10 min)

5. [`https://m365.cloud.microsoft.com`](https://m365.cloud.microsoft.com) → **Copilot** → **New agent** → rovnou záložka **Configure**.
6. **Name:** `NIS2 Průvodce`
7. **Description:** `Pomáhá zorientovat se v zákoně č. 264/2025 Sb. a směrnici NIS2. Odpovídá jen z oficiálních zdrojů. Nenahrazuje právní poradenství.`
8. **Instructions** — vložte:

   ```text
   ## Role
   Jsi "NIS2 Průvodce". Pomáháš malým a středním firmám v ČR porozumět zákonu
   č. 264/2025 Sb. o kybernetické bezpečnosti a směrnici NIS2 (EU 2022/2555).
   Publikum: IT a bezpečnostní manažeři, vedení firmy.

   ## Jak odpovídáš
   - Každou věcnou odpověď rozděl do dvou částí:
     1) ZÁKON: co konkrétně platí v ČR (zákon 264/2025 Sb., prováděcí vyhlášky).
     2) SMĚRNICE: ze kterého článku NIS2 povinnost vychází (např. čl. 20, 21, 23).
   - Na konci přidej 2-3 praktické kroky "Co udělat teď".
   - Odpovídej česky, věcně a stručně. Používej odrážky.
   - Vždy uveď odkaz na zdroj, ze kterého vycházíš.

   ## Úlohy, které umíš
   - Posouzení působnosti: polož cílené otázky (odvětví, počet zaměstnanců, obrat,
     typ služby) a orientačně urči, zda firma spadá pod zákon a do jakého režimu.
     Výsledek označ jako orientační a odkaž na samoposouzení na portálu NÚKIB.
   - Vysvětlení povinnosti: k článku nebo tématu vrať dvojici § zákona -> čl. NIS2.
   - Lhůty: registrace, hlášení incidentů, přechodné období. Lhůty vždy označ
     poznámkou "ověř v aktuální metodice NÚKIB".
   - Podklad pro vedení: stručné shrnutí povinností a odpovědnosti vedení.

   ## Co neděláš
   - Nevymýšlíš čísla paragrafů, lhůty ani výši sankcí. Když je zdroj nepotvrdí,
     řekni "Toto se mi nepodařilo ověřit v oficiálních zdrojích" a číslo neuváděj.
   - Nepoužíváš jiné zdroje než nakonfigurované weby.
   - Neodpovídáš na dotazy mimo kybernetickou bezpečnost a NIS2 — zdvořile odmítni
     a nabídni, s čím pomoct můžeš.
   - U posouzení působnosti a sankcí jednou uveď: "Informační nástroj,
     nenahrazuje právní poradenství."
   ```

9. **Knowledge** → přidejte 3 weby z části A. Zapněte volbu, aby agent **používal jen zadané zdroje** (vypněte hledání na celém webu).
10. **Capabilities** — nechte vypnuté (nejsou potřeba).
11. **Suggested prompts:**

    | Title | Prompt |
    |---|---|
    | Spadáme pod zákon? | `Pomoz mi posoudit, zda naše firma spadá pod zákon č. 264/2025 Sb. a v jakém režimu.` |
    | Hlášení incidentu | `Jaké lhůty platí pro hlášení kybernetického incidentu NÚKIB a co má hlášení obsahovat?` |
    | Brífink pro vedení | `Připrav stručný podklad pro vedení o jeho povinnostech podle zákona o kybernetické bezpečnosti.` |

12. Otestujte v panelu **Preview**, pak **Create**.

### Část C — test a iterace (10 min)

13. Spusťte 5 testů a hodnoťte ✅ / ❌:

    | # | Typ | Dotaz | Očekávání |
    |---|---|---|---|
    | 1 | přímý | `Jaké povinnosti má vedení firmy podle zákona 264/2025 Sb.?` | struktura ZÁKON / SMĚRNICE, odkaz na zdroj |
    | 2 | jinak formulovaný | `Můžu jako jednatel osobně odpovídat za kyberútok?` | stejná podstata jako test 1 |
    | 3 | hraniční | `Máme 40 lidí a jsme dodavatel IT pro nemocnici. Spadáme pod zákon?` | položí doplňující otázky, výsledek označí jako orientační |
    | 4 | mimo téma | `Napiš mi recept na svíčkovou.` | zdvořile odmítne |
    | 5 | **drží se zdrojů?** | `Jakou pokutu dostala firma XY za porušení NIS2?` | řekne, že to v oficiálních zdrojích nenašel, nic nevymyslí |

    Skóre: ___ / 5.

14. Nejhorší test: změňte **jednu věc** (instrukce / popis / zdroj) → zopakujte → pomohlo to?

> [!TIP] Test 5 nahrazuje „hranici práv"
> Veřejný web nemá oprávnění — všichni uživatelé vidí totéž. Riziko je jinde: agent **doplní odpověď z obecných znalostí modelu** nebo z webu mimo whitelist. Proto testujeme, jestli se drží zdrojů a přizná, když něco neví.

## Ověření

- [ ] Agent existuje a je vidět v seznamu agentů v Copilotu.
- [ ] Má 3 webové zdroje a hledání na celém webu je vypnuté.
- [ ] Odpovědi obsahují odkazy na nakonfigurované weby.
- [ ] Máte skóre 5 testů a jednu změřenou iteraci.

## Varianta pro vlastní obor

Stejný postup funguje pro jakýkoli obor s veřejnými autoritativními zdroji. Vyměňte weby a roli:

| Agent | Weby |
|---|---|
| GDPR průvodce | `uoou.gov.cz`, `eur-lex.europa.eu` |
| Průvodce DPH | `financnisprava.gov.cz`, `zakonyprolidi.cz` |
| Průvodce BOZP | `suip.gov.cz`, `bozpinfo.cz` |
| Firemní produkty | veřejný web vaší firmy |

## Reflexe

Co agent udělal, když odpověď ve zdrojích nebyla? A co by se změnilo, kdyby místo veřejného webu četl vaši interní směrnici na SharePointu?

## Stav produktu / delta

> [!WARNING] Ověřit k datu běhu — stav k 2026-09.
> - Agent Builder: limit počtu webových zdrojů (dříve 4 URL, max. 2 úrovně cesty) a název přepínače „jen zadané zdroje".
> - Nahrávání souborů bez SharePoint Online / OneDrivu — předpoklad, že nefunguje.
> - Zákon č. 264/2025 Sb. a vyhlášky: aktuální znění a lhůty na portálu NÚKIB.
