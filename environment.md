# Prostředí kurzu — BYOS (vlastní předplatné)

Kurz nemá kurzovní tenant. Laby běží ve **vašem vlastním Microsoft 365** (model **Bring Your Own Subscription**, stejně jako MS-4004 a další Copilot kurzy).

> [!IMPORTANT] Pracujete se svými firemními daty
> Laby Researcher a „agent dle výběru" pracují s **vaší poštou, Teams a OneDrive**. Při sdílení obrazovky nebo v diskusi **nesdílejte citlivý obsah** (osobní údaje, zákaznická data, smlouvy). Agenti respektují oprávnění — ale to, co promítnete, uvidí celá třída.

## Co potřebujete

| Položka | Minimum | Ideál |
|---|---|---|
| Účet | pracovní účet Microsoft 365 (ne osobní Microsoft účet) | — |
| Copilot | **Microsoft 365 Copilot Chat** (zdarma k M365) | **Microsoft 365 Copilot** licence |
| Prohlížeč | Microsoft Edge nebo Chrome, aktuální verze | — |
| SharePoint | web, kde máte **Edit** (Member) nebo vyšší | web, kde jste **Owner** |
| Vstupní bod | [`https://m365.cloud.microsoft.com`](https://m365.cloud.microsoft.com) | — |

Ověření předem: [`course-intro/pre-course-check.md`](course-intro/pre-course-check.md).

## Matice labů — co který lab potřebuje

| Lab | Modul | Potřebuje | Bez licence Copilot (jen Copilot Chat) | Fallback |
|---|---|---|---|---|
| [Analyst](prebuilt-agents/lab-analyst.md) | M2 | agent **Analyst** viditelný v Agent Store + vzorový Excel (dodán) | **nedostupný** | dvojice se spolužákem, který agenta má / demo lektora |
| [Researcher](prebuilt-agents/lab-researcher.md) | M2 | agent **Researcher** viditelný v Agent Store + vlastní data za 90 dní (Outlook, Teams, OneDrive) | **nedostupný** | dvojice / demo lektora; nebo odlehčená varianta s web grounding |
| [Agent dle výběru](prebuilt-agents/lab-agent-choice.md) | M2 | libovolný agent z Agent Store | Prompt Coach / Idea Coach / Writing Coach — ověřit v Agent Store | vždy aspoň jeden agent dostupný |
| [Copilot Chat agent](build-manage-agents/lab-copilot-chat-agent.md) | M3 | **Agent Builder** | tvorba jde; grounding na **web** zdarma, na **firemní data** jen s PAYG | agent nad veřejným webem (vždy funguje) |
| [SharePoint agent](build-manage-agents/lab-sharepoint-agent.md) | M3 | SharePoint web s **Edit+** | tvorba vyžaduje licenci nebo PAYG — ověřit | **simulace Fabrikam** z oficiálního labu |

> [!WARNING] Ověřit k datu běhu — stav k 2026-09.
> Kdo má přístup k Researcher/Analyst (licence, měsíční limit dotazů, jazyk) a kdo smí **tvořit** SharePoint agenta, se v posledních měsících měnilo několikrát — viz [`GLOSSARY.md`](GLOSSARY.md). Rozhoduje, zda agenta **vidíte v Agent Store**, ne název licence.

> [!IMPORTANT] Agenti se nesdílí mezi tenanty
> Každý student pracuje ve **svém firemním tenantu**. Agenta lze sdílet **jen uvnitř vlastního tenantu** — spolužákovi z jiné firmy ho nenasdílíte. Cvičení se sdílením (M4) proto dělají ve dvojici jen kolegové ze **stejné firmy**; ostatní postup projdou nanečisto a test dokončí s kolegou v práci.

## Admin nastavení, která vám mohou lab zablokovat

Kurz je pro business uživatele — nastavení **nemusíte** umět měnit, ale měli byste je poznat, když na ně narazíte:

- Admin v tenantu **vypnul tvorbu agentů** nebo konkrétní agenty v Agent Store (Microsoft 365 admin center → Copilot → Agents).
- Není zapnutý **pay-as-you-go** pro Copilot Chat → agent nad SharePointem bez licence neodpoví z firemních dat.
- Sdílení agenta „Anyone in your organization" je politikou omezené.

Když narazíte: zapište si hlášku, pokračujte fallbackem, a po kurzu to řešte se svým IT.

## Náklady (jen pro PAYG tenanty)

> [!WARNING] Ověřit k datu běhu.
> Pokud váš tenant používá **pay-as-you-go**, každý dotaz nad firemními daty čerpá **Copilot Credits** a zaplatí je vaše firma. Pár desítek dotazů v labech je zanedbatelné — ale testujte promyšleně, ne „brute force".
