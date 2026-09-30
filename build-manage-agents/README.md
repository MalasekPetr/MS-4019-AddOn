# M3 · Tvorba a správa agenta

> Typ: povinný · Odhad: 120 min (2 laby à ~25 min) · Slidy: LP1 deck, Modul 3 · Learn: [Build and manage an agent](https://learn.microsoft.com/en-us/training/modules/build-manage-no-code-copilot-agent-sharepoint/)

## Cíle

- Rozlišíte **dva nástroje**: Agent Builder (Copilot Chat) a nástroj pro agenty v SharePointu.
- Znáte **součásti agenta** a jejich limity.
- Napíšete **instrukce** a **navržené dotazy**, které fungují.
- Agenta **otestujete podle plánu**, upravíte a spravujete (výchozí agent webu, odinstalace, smazání).

## Dva nástroje, jeden princip

| | **Agent Builder** (Copilot Chat) | **Nástroj pro agenty v SharePointu** |
|---|---|---|
| Kde | Copilot → **New agent** | SharePoint web → **+ New → Agent** (nebo z panelu Copilot) |
| Způsob tvorby | **Describe** (konverzace) + **Configure** (formulář), synchronizované | 3 záložky: **Overview · Sources · Behavior** |
| Šablony | ✅ | ❌ |
| Doladí instrukce konverzací | ✅ doptává se, navrhuje | ❌ **co napíšete, to platí** |
| Capabilities (Code Interpreter, Image Generator) | ✅ | ❌ |
| Navržené dotazy | ano | **max 3** (+ uvítací zpráva) |
| Zdroje | SharePoint, soubory, veřejné weby, konektory… | obsah webu / knihoven / souborů (až 20) |
| Kdo smí | uživatel s Copilotem | **Edit** na webu a výš |
| Sdílení | tvůrce sám (M4) | schvaluje **vlastník webu** (M4) |

## Součásti agenta

| Pole | K čemu | Limit |
|---|---|---|
| **Name** | název | 30 znaků |
| **Icon** | ikona | PNG, max 1 MB |
| **Description** | podle popisu Copilot **pozná, kdy agenta použít**; zobrazí se i v katalogu | 1 000 znaků |
| **Instructions** | jak se agent chová, co dělá a jak | 8 000 znaků |
| **Knowledge** | odkud čerpá | viz níže |
| **Capabilities** | Code Interpreter (analýza dat Pythonem), Image Generator | jen Agent Builder |
| **Suggested prompts** | navržené dotazy pro start | SharePoint: max 3 |

> [!IMPORTANT] Slidy vs. realita — SharePoint listy
> Slide 50 tvrdí *„agenti zatím nepoužívají data ze SharePoint listů"*. **Zastaralé.** Od 03–05/2026 (GA, [MC1255409](https://mc.merill.net/message/MC1255409)) umí SharePoint agent čerpat z listu — ale s tvrdým omezením: **jen jeden list a nic jiného**. Kombinovat list se soubory nebo stránkami nejde; když list přidáte k agentovi, který už má zdroje, **ostatní zdroje se odeberou** (UI se zeptá). Agent Builder list jako zdroj také podporuje (1 list) — ověřit k datu běhu.

> [!WARNING] Agent neanalyzuje, agent hledá
> I s listem jako zdrojem agent **dohledává a shrnuje**, ne **počítá nad celou tabulkou**. Dotaz *„Komu propadá certifikát do 30 dnů?"* nedá spolehlivý úplný výčet. Na analytiku nad daty použijte **Analyst** (M2) nebo pokročilé nástroje.

## Instrukce — jak je psát

Instrukce jsou **strukturovaný prompt, který platí pro každou konverzaci**. Pište je v odrážkách, česky, konkrétně.

```text
# Účel
Jsi asistent pro <kdo>. Pomáháš s <co>.

# Jak odpovídáš
- Odpovídej česky, stručně (max 5 odrážek), věcně.
- Vždy uveď odkaz na dokument, ze kterého čerpáš.
- Když odpověď ve zdrojích nenajdeš, řekni to a odkaž na <kontakt>. Nic si nevymýšlej.

# Co neděláš
- Neodpovídáš na dotazy mimo <téma>.
- Neposkytuješ právní / mzdové / osobní informace o konkrétních lidech.

# Postup u typických dotazů
1. Když se uživatel ptá na <X>, nejdřív se zeptej na <Y>.
2. ...
```

Pravidla:

- **Instrukce ≠ znalosti.** Do instrukcí patří *chování* agenta, ne text směrnice. Směrnice patří do zdroje (knihovny, souboru).
- **Popis je důležitý jako instrukce.** Podle popisu Copilot vybírá agenta — pište ho krátce a přesně.
- **V SharePointu nemáte konverzačního pomocníka** — napište instrukce hotové (např. je nechte předem vyladit v Agent Builderu nebo Prompt Coachem).

Vzorové scénáře s instrukcemi: [`scenario-cards.md`](scenario-cards.md).

## Testování — plán místo „zkusím pár dotazů"

Před sdílením agenta projděte **5 testů**:

| # | Typ testu | Příklad (agent pro cestovní směrnici) | Očekávání |
|---|---|---|---|
| 1 | **Přímý dotaz** | „Jaká je sazba stravného pro Německo?" | správná odpověď + odkaz na zdroj |
| 2 | **Stejná otázka jinak** | „Kolik dostanu na jídlo v Mnichově?" | stejná odpověď (konzistence) |
| 3 | **Hraniční / složitý** | „Služebka přes půlnoc, Rakousko i Německo — jak se počítá?" | rozumný postup nebo přiznání nejistoty |
| 4 | **Mimo téma** (negativní) | „Napiš mi báseň o dovolené." | zdvořilé odmítnutí dle instrukcí |
| 5 | **Hranice práv** | kolega bez přístupu ke knihovně se zeptá na totéž | **nedostane** odpověď ze zdroje, na který nemá práva |

Po testu: **jedna úprava** (instrukce, popis, zdroj) → zopakujte nejhorší test → změřte rozdíl.

Dále testujte: **tón** (formální vs. neformální), **aktuálnost** (přidejte nový dokument — odráží ho agent?), **hub web** (pokud je zdrojem hub, čerpá agent i z přidružených webů?).

## Úpravy agenta

- Upravujete **stejným nástrojem**, kterým jste agenta vytvořili.
- Lidé, se kterými jste agenta sdíleli, **změny nevidí, dokud agenta znovu nenasdílíte**. U zdrojů typu soubor/složka doporučuje Microsoft sdílet znovu se stejnou skupinou — tím se znovu nasdílí i soubory.
- **Výchozí agent webu (ready-made)** upravit nejde.

## Správa agentů

| Akce | Copilot Chat agent | SharePoint agent |
|---|---|---|
| **Odinstalovat** (skrýt z mého seznamu, konfigurace zůstane) | ✅ | ❌ (neexistuje) |
| **Smazat** | správa v administraci (není předmětem kurzu) | ✅ tvůrce / vlastník webu |
| **Výchozí agent webu** | — | vlastník webu může nastavit schváleného agenta jako výchozí; ready-made jde vždy vrátit |
| **Historie chatu** | smazat jednu konverzaci nebo celou historii | totéž |

Ready-made agenta webu **nelze smazat**.

## Laby

| Lab | Odhad | Soubor |
|---|---|---|
| 1 · Copilot Chat agent (Agent Builder) | 25 min | [`lab-copilot-chat-agent.md`](lab-copilot-chat-agent.md) |
| 2 · SharePoint agent | 25 min | [`lab-sharepoint-agent.md`](lab-sharepoint-agent.md) |

## Stav produktu / delta

> [!WARNING] Ověřit k datu běhu — stav k 2026-09.
> UI Agent Builderu se mění po měsících (Describe tab není ve všech jazycích/regionech — seznam na Learnu). Podpora listů (MC1255409) a počet zdrojů SharePoint agenta. Terminologie starter → suggested prompts.
