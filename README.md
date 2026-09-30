# MS-4019 AddOn — Agenti pro každodenní business procesy (česká vrstva)

Doplňkové materiály ke kurzu **MS-4019: Transform your everyday business processes with agents** (GOPAS, 1 den, výuka v češtině). Vše v Markdownu, renderovatelné přímo na GitHubu.

> [!IMPORTANT] Co tohle repo je — a co není
> Oficiální obsah kurzu tvoří **Microsoft slidy + Microsoft Learn + oficiální laby**. Tohle repo je **česká nadstavba**: výklad v češtině, zadání labů s českým kontextem, otázky do diskusí, opravy míst, kde MS materiál zastaral, a lektorské poznámky. Oficiální MCT materiály (PPTX/PDF) v repu **nejsou a nebudou** (licence MCT).

## Jak repo číst

- **Pořadí a časy bloků** drží [`agenda.md`](agenda.md) — jediný zdroj pravdy.
- **Závazné názvosloví** (produkty, přejmenování) je v [`GLOSSARY.md`](GLOSSARY.md).
- **Prostředí** (BYOS — vlastní předplatné) a co který lab potřebuje: [`environment.md`](environment.md).
- **Než přijdete na kurz:** projděte [`course-intro/pre-course-check.md`](course-intro/pre-course-check.md) (10 minut).
- **Konvence** psaní materiálů: [`CONVENTIONS.md`](CONVENTIONS.md).

## Struktura

```text
MS-4019-AddOn/
├─ README.md               # tento soubor
├─ agenda.md               # časový plán dne
├─ GLOSSARY.md             # názvosloví a přejmenování
├─ environment.md          # BYOS, požadavky per lab, fallbacky
├─ CONVENTIONS.md          # jak psát materiály
├─ course-intro/           # úvod kurzu + pre-course check
├─ get-started-agents/     # Modul 1 — Začínáme s agenty
├─ prebuilt-agents/        # Modul 2 — Předpřipravení agenti (3 laby)
├─ build-manage-agents/    # Modul 3 — Tvorba a správa agenta (2 laby)
├─ share-use-agents/       # Modul 4 — Sdílení a používání agentů
└─ lp-review/              # Modul 5 — Opakování, závěr, další kroky
```

Každý modul = složka:

| Soubor | Pro koho | Obsah |
|---|---|---|
| `README.md` | student | výklad modulu v češtině |
| `lab-*.md` | student | zadání labu (česky, s odkazem na oficiální MS lab) |
| `instructor-notes.md` | lektor | timing, diskusní otázky, tripwires, fallbacky |

## Legenda

- `> [!WARNING] Ověřit k datu běhu` — rychle se měnící fakt (UI, licence, dostupnost agentů).
- `> [!IMPORTANT]` — přejmenování nebo místo, kde se oficiální slidy **rozcházejí** s aktuálním stavem.
- `> [!TIP]` — praktická rada lektora navíc.

## Oficiální zdroje (Microsoft)

- Kurz: [MS-4019 na Microsoft Learn](https://learn.microsoft.com/en-us/training/courses/ms-4019)
- Learning Path: [Transform your everyday business processes with agents](https://learn.microsoft.com/en-us/training/paths/implement-no-code-copilot-agents-microsoft-365-sharepoint/)
- Laby: [MicrosoftLearning / MS-4019 (GitHub)](https://github.com/MicrosoftLearning/MS-4019-Transform-your-everyday-business-processes-with-agents)

## Stav

Obsah kompletní pro běh 2026-10. Vychází z MS materiálů verze **January 2026** (Change Log / TPG) a ze stavu produktu k **2026-09**.
