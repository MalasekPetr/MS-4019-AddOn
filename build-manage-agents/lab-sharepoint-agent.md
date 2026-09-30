# Lab 2 · Vytvořte SharePoint agenta

> Modul: M3 · Odhad: 25 min · Režim: vlastní SharePoint web (BYOS) **nebo simulace Fabrikam**
> Oficiální zadání (EN) vč. odkazu na simulaci: [Exercise — Create a SharePoint agent](https://microsoftlearning.github.io/MS-4019-Transform-your-everyday-business-processes-with-agents/Instructions/Labs/M03-build-manage-no-code-agent-sharepoint/8-exercise-create-sharepoint-agent.html) · [Learn unit](https://learn.microsoft.com/en-us/training/modules/build-manage-no-code-copilot-agent-sharepoint/8-exercise-create-sharepoint-agent)

## Cíl

Postavit agenta nad obsahem **jednoho SharePoint webu** a zažít rozdíl oproti Agent Builderu: žádná konverzace, co napíšete, to platí.

## Předpoklady

- SharePoint web, kde máte **Edit** nebo jste **Owner** (týmový, projektový web, web Teams týmu) s aspoň několika dokumenty.
- **Nemáte web?** → spusťte **simulaci Fabrikam** (odkaz v oficiálním zadání výše) a postupujte stejnými kroky.

> [!TIP] Instrukce si připravte předem
> Nástroj v SharePointu instrukce nedolaďuje. Napište je nejdřív (vzor v [`scenario-cards.md`](scenario-cards.md) — karta C je pro SharePoint ideální) nebo je nechte vyladit Prompt Coachem.

## Kroky

1. Otevřete svůj web → **+ New** → **Agent** (případně z panelu Copilot na webu → vytvořit agenta).
2. **Overview**: název, ikona (PNG, max 1 MB), účel.
3. **Sources**: vyberte zdroje — celý web, konkrétní knihovny, složky nebo soubory (až 20).
   - Zkuste záměrně **zúžit** zdroje na to, co agent opravdu potřebuje. Méně = přesnější.
4. **Behavior**:
   - **Welcome message** — co agent uživateli řekne na začátku,
   - **Starter / suggested prompts** — max 3,
   - **Instructions** — vložte připravené instrukce.
5. **Create** / **Save**.
6. Otestujte v panelu chatu: navržené dotazy + vlastní dotazy z plánu (přímý, jinak formulovaný, hraniční, mimo téma).
7. **Upravte**: `…` v panelu agenta → **Edit agent** → změňte jednu věc → otestujte znovu.
8. *(Volitelně)* Zkuste na webu najít soubor agenta (přípona `.agent`, typicky v knihovně webu) — agent je **součást webu** a dědí jeho oprávnění. Umístění se může lišit.

### Volitelně (pokud máte list)

9. Zkuste do **kopie** agenta přidat jako zdroj **SharePoint list**. Co se stane s ostatními zdroji? (Viz `[!IMPORTANT]` o listech v [README](README.md#součásti-agenta).)

## Ověření

- [ ] Agent existuje na webu a odpovídá z jeho obsahu, s odkazy na zdroje.
- [ ] Má uvítací zprávu, max 3 navržené dotazy a instrukce.
- [ ] Provedli jste jednu úpravu přes **Edit agent**.
- [ ] Umíte říct 3 rozdíly oproti Agent Builderu.

## Fallback

- **Nemáte web s Edit** → simulace Fabrikam.
- **Tvorba nejde kvůli licenci / nastavení** → simulace Fabrikam, nebo demo lektora.
- **Agent neodpovídá z obsahu** → dokumenty mohou být čerstvě nahrané a ještě nezaindexované; zkuste starší dokumenty nebo počkejte.
- **Tenant nemá SharePoint Online** → SharePoint agent nejde; postavte [Lab 1-F · agent nad veřejným webem](lab-web-grounded-agent.md).

## Reflexe

Kdy byste zvolili SharePoint agenta a kdy Copilot Chat agenta? (Nápověda: kdo je vlastník obsahu a kde uživatelé pracují.)
