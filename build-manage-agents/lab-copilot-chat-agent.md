# Lab 1 · Vytvořte agenta v Copilot Chatu (Agent Builder)

> Modul: M3 · Odhad: 25 min · Režim: vlastní tenant (BYOS)
> Oficiální zadání (EN): [Exercise — Create a Copilot Chat agent](https://microsoftlearning.github.io/MS-4019-Transform-your-everyday-business-processes-with-agents/Instructions/Labs/M03-build-manage-no-code-agent-sharepoint/6-exercise-create-copilot-chat-agent.html)

## Cíl

Postavit agenta, který řeší **váš** reálný problém — a otestovat ho podle plánu, ne od oka.

## Předpoklady

- Přístup do Agent Builderu (Copilot → **New agent**).
- Nápad: váš proces z úvodu / diskuse v M1. Nemáte? Vezměte kartu z [`scenario-cards.md`](scenario-cards.md).
- Zdroje: SharePoint web/knihovna/soubory, ke kterým máte přístup — **nebo** veřejný web (funguje i bez licence).

## Kroky

### Část A — návrh (5 min, na papír / do poznámek)

1. Pro **koho** agent je a **jaký problém** řeší (1 věta)?
2. Z jakých **zdrojů** bude čerpat?
3. Napište **5 testovacích dotazů** podle plánu v [README](README.md#testování--plán-místo-zkusím-pár-dotazů): přímý, jinak formulovaný, hraniční, mimo téma, hranice práv.

### Část B — stavba (10 min)

4. [`https://m365.cloud.microsoft.com`](https://m365.cloud.microsoft.com) → **Copilot** → **New agent**.
5. Na záložce **Describe** popište agenta běžnou řečí — kdo, co, pro koho, z čeho. Příklad:
   `Vytvoř agenta "Cestovní průvodce", který zaměstnancům odpovídá na dotazy ke služebním cestám podle firemní směrnice. Odpovídá česky, stručně a vždy odkazuje na zdroj.`
6. Odpovězte na doplňující otázky Agent Builderu.
7. Přepněte na **Configure** a zkontrolujte:
   - **Name** (max 30 znaků), **Description** (krátce a přesně),
   - **Instructions** — vygenerované z vašeho popisu; doplňte sekce *Jak odpovídáš* / *Co neděláš* (vzor v [README](README.md#instrukce--jak-je-psát)),
   - **Knowledge** — přidejte zdroje,
   - **Capabilities** — zapněte jen to, co agent potřebuje,
   - **Suggested prompts** — 3 dotazy, které uživatele navedou.
8. Otestujte v panelu **Preview**, pak **Create**. Agent je zatím **jen váš** (sdílení v M4).

### Část C — test a iterace (10 min)

9. Spusťte 5 testovacích dotazů z části A. Skóre: ___ / 5.
10. Test 5 (hranice práv) — sami ho neotestujete, zapište **predikci**. V M4 ho ověříte s kolegou ze **stejné firmy** (agenty nelze sdílet mezi firmami), jinak zítra v práci.
11. Nejhorší test: změňte **jednu věc** (instrukce / popis / zdroj) → zopakujte → pomohlo to?

## Ověření

- [ ] Agent existuje a je vidět v seznamu agentů v Copilotu.
- [ ] Má zdroje znalostí (bez nich odpovídá jen obecnými znalostmi modelu).
- [ ] Má instrukce s částí „Co neděláš" a pravidlem „když nevíš, řekni to".
- [ ] Máte skóre 5 testů a jednu změřenou iteraci.

## Fallback

- **Nemáte přístup k firemním datům** (Copilot Chat bez licence a bez PAYG) → jako zdroj použijte **veřejný web** (např. web vaší firmy, [portál veřejné správy](https://portal.gov.cz)). Postup je stejný.
- **Tvorba agentů vypnutá adminem** → sledujte demo lektora, část A (návrh + testy) je plnohodnotný výstup.
- **Describe tab není k dispozici** (jazyk/region) → vše vyplňte v **Configure**.

## Reflexe

Co bylo těžší — napsat instrukce, nebo vybrat zdroje? Co byste potřebovali, aby agent mohl jít kolegům?
