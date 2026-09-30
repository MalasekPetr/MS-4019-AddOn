# Glosář — názvosloví a přejmenování

Jediný zdroj pravdy pro názvy. Microsoft agenty přejmenovává často — ve slidech, na Learnu a v UI se proto můžete setkat s různými názvy pro tutéž věc.

> [!WARNING] Ověřit k datu běhu — stav k 2026-09.

## Základní pojmy

| Pojem (UI / EN) | Česky | Význam |
|---|---|---|
| **Agent** | agent | AI asistent s vlastními instrukcemi a zdroji znalostí, běžící v Microsoft 365 Copilotu. Tvoří ho běžný uživatel bez programování. |
| **Advanced agent** | pokročilý agent | agent stavěný vývojáři / makery (Copilot Studio, Microsoft 365 Agents Toolkit) — akce, workflow, integrace. **Mimo rozsah kurzu.** |
| **Prebuilt agent** | předpřipravený agent | agent od Microsoftu nebo schváleného partnera v Agent Store (Researcher, Analyst, Prompt Coach…). |
| **Ready-made agent** | výchozí agent webu | automaticky vytvořený agent každého SharePoint webu, scopovaný na obsah webu. Nejde upravit ani smazat. |
| **SharePoint agent** | agent SharePointu | agent vytvořený na konkrétním SharePoint webu, nad jeho obsahem. |
| **Copilot Chat agent** | agent v Copilot Chatu | agent vytvořený v Agent Builderu přímo v Microsoft 365 Copilot appce. |
| **Declarative agent** | deklarativní agent | agent definovaný jen konfigurací (instrukce, znalosti, schopnosti, příp. akce), který běží na modelu a orchestrátoru Microsoft 365 Copilotu. Všichni agenti tvoření v kurzu jsou deklarativní. |
| **Custom engine agent** | agent s vlastním enginem | agent s vlastním modelem a orchestrací (Copilot Studio, Agents SDK, Azure AI Foundry). **Mimo rozsah kurzu.** |
| **Agent Builder** | — | jednoduchý editor agentů uvnitř Microsoft 365 Copilot (záložky **Describe** a **Configure**). |
| **Agent Store** | obchod agentů | katalog agentů v Copilotu (Microsoft, partneři, „Built by your org"). |
| **Knowledge (sources)** | zdroje znalostí | weby, knihovny, soubory, (listy), weby na internetu, konektory — odkud agent čerpá. |
| **Instructions** | instrukce | jak se má agent chovat (max 8 000 znaků). |
| **Suggested prompts** | navržené dotazy | předpřipravené dotazy pro start konverzace. |
| **Grounding** | ukotvení | dohledání podkladů pro odpověď — z webu (Bing) nebo z firemních dat (Microsoft Graph). |
| **Copilot Credits** | kredity | jednotka pay-as-you-go (PAYG) účtování práce s firemními daty pro uživatele bez Copilot licence. |

## Přejmenování (co v materiálech potkáte)

| Starší název | Aktuální název | Poznámka |
|---|---|---|
| no-code agent | **agent** | od 03/2025; low-code/pro-code → **advanced agents** |
| starter prompts | **suggested prompts** | od 01/2026 v Agent Builderu; SharePoint UI může stále ukazovat „starter prompts" |
| Knowledge Check | **Module Assessment** | kvíz na konci modulu na Learnu |
| „Who can create and use agents?" | **Agents and Access in Microsoft 365 Copilot** | název jednotky v Modulu 1 |
| Agent Builder → „Agent Builder in Copilot Studio" → „Copilot Studio" | **Agent Builder** (v Microsoft 365 Copilot) | Microsoft branding otočil několikrát; dnes je **Agent Builder** zážitek uvnitř Copilot appky, **Copilot Studio** samostatná low-code platforma. Speaker notes MS decku místy stále píší „Copilot Studio" tam, kde je myšlen Agent Builder. |
| Visual Creator agent | **Copilot Create** | agent retirován 10/2025 |
| Writing agent / Writing Coach | **Writing Coach** | slidy používají oba názvy |

> [!IMPORTANT] Agent Builder ≠ Copilot Studio
> V kurzu tvoříme agenty v **Agent Builderu** (Copilot Chat) a v **nástroji pro agenty v SharePointu**. **Copilot Studio** je jiný nástroj pro pokročilé agenty — v tomto kurzu ho jen zmíníme jako „další krok".

## Licence — tři úrovně

| Úroveň | Co dává | Agenti |
|---|---|---|
| **Microsoft 365 Copilot Chat** (zdarma k M365) | chat s grounding na **web** | agenty lze tvořit i používat; firemní data jen s **PAYG** (Copilot Credits) |
| **Copilot Chat + PAYG** | navíc práce s firemními daty (účtuje se v kreditech) | agenti nad SharePointem, použití SharePoint agentů |
| **Microsoft 365 Copilot** (licence — Business nebo Enterprise) | plný zážitek, firemní data, Copilot v Office appkách, bez měření | všechno výše + prémioví předpřipravení agenti (Researcher, Analyst) |

> [!WARNING] Ověřit k datu běhu — stav k 2026-09.
> - **Researcher / Analyst**: Microsoft je uvádí jako součást licence Microsoft 365 Copilot ([Copilot Business pricing](https://www.microsoft.com/en-us/copilot/pricing/business)); starší zdroje je uváděly jen pro Enterprise. Při GA (06/2025) platil **limit ~25 dotazů/měsíc** dohromady. **Analyst podporoval jen 8 jazyků** — čeština nemusí fungovat. Admin je navíc může v tenantu skrýt.
> - **Rozhodující test** proto není typ licence, ale: *vidím agenta v Agent Store?* (viz [pre-course check](course-intro/pre-course-check.md), krok 3).
> - Licenční požadavek na **tvorbu** SharePoint agenta: [Get started with SharePoint agents](https://learn.microsoft.com/en-us/sharepoint/get-started-sharepoint-agents).

## Licence vs. oprávnění (nosný princip dne)

- **Licence** rozhoduje, **jestli funkci máte**.
- **Oprávnění v Microsoft 365** rozhodují, **co agent danému člověku ukáže**. Agent nikdy neobejde práva uživatele — odpovídá jen z toho, co tazatel sám smí otevřít.
