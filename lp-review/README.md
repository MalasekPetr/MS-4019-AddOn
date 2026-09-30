# M5 · Opakování a závěr

> Typ: povinný · Odhad: 15 + 10 min · Slidy: LP1 deck (Modul 5) + *MS-4019 Conclusion*

## Co jste se dnes naučili

| Modul | Klíčová myšlenka |
|---|---|
| M1 | Agent = instrukce + zdroje (+ schopnosti). **Licence** rozhoduje, jestli funkci máte; **oprávnění**, co vám agent ukáže. |
| M2 | Předpřipravení agenti bez konfigurace: **Analyst** na data, **Researcher** na rešerše, coachové na prompt, nápad a text. |
| M3 | Agent Builder (konverzace, capabilities) vs. SharePoint nástroj (jeden web, co napíšete, to platí). **Testovat podle plánu.** |
| M4 | Sdílení nemění oprávnění zdrojů. Copilot Chat agent sdílí tvůrce, SharePoint agenta schvaluje vlastník webu. |

## Diskuse

1. Co je pro vás nejdůležitější poznatek dne — a proč?
2. Které funkci agentů v Copilot Chatu nebo SharePointu se budete věnovat jako první?
3. Jakého agenta postavíte **příští týden** ve své práci?

## Opakovací otázky

Odpovědi jsou pod otázkami — nejdřív zkuste sami.

1. **Kolega nedostává od vašeho sdíleného agenta odpovědi z firemní směrnice, vy ano. Proč?**
   <details><summary>Odpověď</summary>Nemá oprávnění ke zdroji (knihovně/souboru). Agent odpovídá podle práv tazatele; sdílení agenta práva na zdroje nemění.</details>

2. **Chcete, aby agent spočítal průměry z tabulky a nakreslil graf. Kterého agenta / funkci použijete?**
   <details><summary>Odpověď</summary>Předpřipraveného agenta Analyst, nebo vlastního agenta se zapnutým Code Interpreterem (jen Agent Builder).</details>

3. **Jste Member na webu. Vytvoříte SharePoint agenta. Mohou ho kolegové hned používat?**
   <details><summary>Odpověď</summary>Ne — agenta musí schválit vlastník webu. (Kdyby ho vytvořil vlastník, je schválený automaticky.)</details>

4. **Co je rozdíl mezi popisem (Description) a instrukcemi (Instructions)?**
   <details><summary>Odpověď</summary>Popis říká Copilotu a uživatelům, <i>k čemu</i> agent je a kdy ho použít (max 1 000 znaků). Instrukce řídí, <i>jak</i> se agent chová (max 8 000 znaků).</details>

5. **Upravili jste sdíleného agenta. Proč kolegové změnu nevidí?**
   <details><summary>Odpověď</summary>Změny se projeví až po novém nasdílení agenta.</details>

6. **Přidáte do SharePoint agenta, který čerpá ze tří knihoven, jako zdroj SharePoint list. Co se stane?**
   <details><summary>Odpověď</summary>Ostatní zdroje se odeberou — list musí být jediným zdrojem (stav 2026).</details>

7. **Jaký je rozdíl mezi odinstalací a smazáním Copilot Chat agenta?**
   <details><summary>Odpověď</summary>Odinstalace ho skryje z vašeho seznamu, konfigurace zůstane; smazání je trvalé a řeší se v administraci.</details>

8. **Který agent se nedá upravit ani smazat?**
   <details><summary>Odpověď</summary>Výchozí (ready-made) agent SharePoint webu.</details>

Oficiální kvízy: **Module Assessment** na konci každého modulu na [Microsoft Learn](https://learn.microsoft.com/en-us/training/paths/implement-no-code-copilot-agents-microsoft-365-sharepoint/).

## Co dál

### Microsoft kurzy

| Kurz | Pro koho |
|---|---|
| **MS-4004** Empower your workforce with Microsoft 365 Copilot Use Cases | scénáře podle rolí (HR, Finance, Sales…) |
| **MS-4018** Draft, analyze, and present using Microsoft 365 Copilot | Copilot ve Wordu, Excelu, PowerPointu |
| **MS-4007** Copilot User Enablement Specialist | adopce Copilotu ve firmě |
| **MS-4017** Manage and extend Microsoft 365 Copilot | správci a architekti |

### GOPAS kurzy (navazující, česky)

| Kurz | Pro koho |
|---|---|
| **GOC224** Microsoft 365 — správa SharePoint Copilotu, agentů a obsahových služeb | správci a architekti: licencování, konfigurace, governance, Agent Builder, SharePoint agenti, Copilot Studio (5 dní) |
| **SPO_COPILOT** Microsoft 365 Agents SDK a Copilot Extensions | vývojáři: pokročilí agenti v kódu (5 dní) |

## Feedback

Dotazník přijde e-mailem. Díky, že jste byli.
