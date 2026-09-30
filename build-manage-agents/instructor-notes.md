# Instructor notes — M3 · Tvorba a správa agenta

## Timing (125 min vč. 10 min přestávky; agenda počítá 130 s rezervou 5 min)

| Min | Slide | Co |
|---|---|---|
| 0–10 | 30–31 | Dva nástroje, součásti agenta (tabulky v README) |
| 10–20 | 32–34 | Agent Builder: Describe vs. Configure — **živé demo** (karta A) |
| 20–30 | — | **Instrukce**: vzor, „instrukce ≠ znalosti", testovací plán |
| 30–55 | 35 | **Lab 1 Copilot Chat agent** |
| 55–65 | — | *Přestávka* |
| 65–75 | 36 | SharePoint nástroj — rozdíly, demo na vlastním webu |
| 75–100 | 37 | **Lab 2 SharePoint agent** |
| 100–105 | 38 | Video *One-click AI Agents* |
| 105–115 | 39 | Diskuse k videu |
| 115–125 | 40–43 | Test/edit, správa, Module Assessment, shrnutí |

> Video (slide 38) záměrně **po** labu — studenti už vědí, co vidí, a diskuse je konkrétnější. Pokud chceš MS pořadí, pusť ho před Lab 2.

## Go/no-go

- Demo web s dokumenty (směrnice / FAQ) připravený na vlastním tenantu.
- Fabrikam simulace ověřená den předem (odkaz v oficiálním labu).
- Seznam, kdo z třídy nemá web s Edit → ti jdou rovnou na simulaci, neztrácet čas hledáním webu.

## Video (slide 38)

[One-click AI Agents](https://www.youtube.com/watch?v=Ca7JYC9MQIU)

Diskuse (10 min):
1. Co vás zaujalo — a proč?
2. Srovnejte s tím, co jste právě postavili: bylo to opravdu „one-click"? Kde to trvalo nejdéle?
3. Které funkce tvorby agentů v SharePointu byste využili hned?

## Tripwires

- **„Agent Builder" vs. „Copilot Studio"** — speaker notes (slide 34, 40) stále píší Copilot Studio. Pro studenty: *Agent Builder v Copilotu*. Copilot Studio = jiný nástroj pro pokročilé agenty. Viz [`../GLOSSARY.md`](../GLOSSARY.md).
- **Slide 50 „agenti nepoužívají listy"** — zastaralé, viz `[!IMPORTANT]` v README. Omezení: 1 list a nic jiného; přidáním listu se ostatní zdroje odeberou (MC1255409).
- **SharePoint nástroj nekonverzuje** — TPG a notes slide 36 to zdůrazňují: *„co napíšete, to platí"*. Proto instrukce připravit předem.
- **Instrukce ≠ znalosti** — studenti rádi vloží celou směrnici do instrukcí. Zarazit: text směrnice patří do zdroje.
- **Agent bez zdrojů** odpovídá obecnými znalostmi modelu — oficiální lab to výslovně zmiňuje. Zkontrolovat u každého.
- **Negativní test** (mimo téma) je povinný — bez něj se agent „vždycky povede".
- **Test hranice práv** se sám dělá těžko → nechat jako predikci, ověřit v M4. **BYOS = každý student ve svém tenantu, agenti se mezi tenanty nesdílí** → reálný test jen dvojice ze stejné firmy; ostatní predikce + demo lektora se dvěma účty.
- **Analytické dotazy** („kolik…", „vypiš všechny…") agent nezvládne spolehlivě — to není chyba labu, to je hranice nástroje. Most na Analyst (M2) a pokročilé agenty.
- **Editace sdíleného agenta** — sdílení uživatelé změny nevidí, dokud se agent znovu nenasdílí; u agenta sdíleného v Teams notes uvádějí, že po úpravě původní instance přestane fungovat. Ověřit k datu běhu.
- **Čerstvě nahrané dokumenty** nemusí být zaindexované — v demu používat obsah nahraný den předem.

## Správa (slide 41) — value-add

- **Odinstalace vs. smazání** (Copilot Chat agent): odinstalace = skrytí, konfigurace zůstane; smazání = trvalé, řeší se v administraci.
- SharePoint agent: jen smazání, žádná odinstalace. Ready-made agent: nejde smazat ani upravit.
- Výchozí agent webu: jen vlastník/admin; ready-made jde vždy vrátit.

## Vazby

- Zpět: M2 anatomie promptu → tady instrukce.
- Dopředu: M4 — sdílení agenta, test hranice práv se spolužákem.
