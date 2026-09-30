# Instructor notes — M4 · Sdílení a používání agentů

## Timing (45 min)

| Min | Slide | Co |
|---|---|---|
| 0–8 | 45–46 | Dva modely sdílení, **pravidlo oprávnění** (diagram) |
| 8–13 | 47–48 | Agenti v Teams |
| 13–23 | — | **Mini-lab ve dvojici** (sdílení + test hranice práv z M3) |
| 23–35 | 49 | Diskuse: kdy sdílet a kdy ne |
| 35–40 | 50–51 | Používání, historie chatu |
| 40–45 | 52–55 | Video (zkráceně) + shrnutí |

> Mini-lab není v MS decku — přidán, protože test hranice práv z M3 bez druhé osoby nejde. Když nestíháš, obětuj video (slide 52) — dej odkaz za domácí úkol.

## Go/no-go mini-labu (cross-tenant!)

- **Agenti se nesdílí mezi tenanty.** Pod BYOS je každý student ve svém tenantu → dvojice (varianta A) **jen ze stejné firmy** (pole „Firma" z pre-course checku). Ostatní varianta B (nanečisto + predikce).
- **Demo na vlastním tenantu se dvěma účty** (tvůrce + uživatel bez přístupu k jedné knihovně) připravit den předem — je to jediná jistá ukázka testu č. 5 pro celou třídu.
- Nepouštět studenty do pokusů přidávat hosty (B2B) do svých tenantů kvůli labu — mimo rozsah a mimo jejich pravomoc.

## Video (slide 52)

[A real-life use case of using agents in SharePoint](https://www.youtube.com/watch?v=zwl-EHELi-s)

Diskuse (slide 53, 5–10 min): Co vás na reálném příběhu zaujalo? Šlo by to u vás — a co by tomu bránilo?

## Diskuse: kdy sdílet (slide 49) — 12 min

**Téma 1 — Kdy agenta sdílet a kdy ne?**
1. Jaké úkoly nebo procesy ospravedlňují sdílení agenta?
2. Kdy může sdílení škodit? (citlivá data, nejasný účel agenta)
3. Jak vyvážit spolupráci a ochranu dat?

Kam diskusi dovést:
- Test „**tři otázky**": Ptá se na totéž víc než pár lidí? Mají všichni přístup ke zdrojům? Snesl by obsah zdrojů zveřejnění v celé skupině? Tři ano → sdílet.
- Červené vlajky: osobní údaje ve zdrojích (GDPR), agent postavený „pro sebe" s osobními zkratkami, nejasný vlastník, který agenta nebude udržovat.

**Téma 2 — Agenti v Teams: pomocník, nebo šum?**
1. Zlepší agent v kanálu spolupráci, nebo přidá šum?
2. Jak zajistit, aby agent pomáhal a nerušil?
3. Jaká pravidla byste pro tým nastavili?

Kam diskusi dovést: agent v Teams je „nový kolega" — potřebuje představení (k čemu je, k čemu ne), jasného vlastníka a pravidlo, že jeho odpověď je podklad, ne rozhodnutí.

Facilitační tip: *„Jak byste nového sdíleného agenta představili svému týmu? Napište tři pravidla."*

## Tripwires

- **„Sdílel jsem agenta, ale kolega nedostává odpovědi"** — nejčastější dotaz. Odpověď: práva na zdroje, ne na agenta. Opakovat klíčovou větu z M1.
- **SharePoint agent — tvůrce nemůže sdílet**: schvaluje vlastník webu. Když je tvůrce sám vlastníkem, schválení je automatické.
- **Automatické sdílení souborů** (Copilot Chat agent) — je to feature i riziko. Zmínit GDPR: agent se soubory osobních údajů nasdílený celé firmě = incident.
- **Odebrání přístupu k agentovi neodebere přístup k souborům** — notes to uvádějí; zdůraznit.
- **Slide 50 — listy** — zastaralé, viz M3.

## Vazby

- Zpět: M1 (licence vs. oprávnění), M3 (test hranice práv).
- Dopředu: LP review.
