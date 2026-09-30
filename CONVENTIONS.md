# Konvence

Pravidla pro psaní materiálů. Cíl: konzistence a snadná údržba mezi běhy.

## Jazyk

- **Obsah**: čeština.
- **Názvy produktů a UI prvků**: anglicky, tak jak je student uvidí v UI (viz [`GLOSSARY.md`](GLOSSARY.md)). Česky vysvětlit při prvním výskytu.
- **Cesty a názvy souborů/složek**: angličtina, `kebab-case`.

## Struktura modulu

Jeden modul = jedna složka se slugem (ne číslem). Pořadí drží [`agenda.md`](agenda.md).

## Autorská práva

- Microsoft MCT materiály (PPTX, PDF, speaker notes) **nekopírovat** do repa. Složka `ms/` je v `.gitignore`.
- Z MS materiálů jen **parafrázovat a doplňovat**; oficiální laby **odkazovat**, ne přepisovat.

## Markdown

- Nadpisy `##` / `###`, bez přeskoků úrovní. Krátké odstavce, odrážky.
- Diagramy jako ` ```mermaid ` bloky, výchozí motiv.

## Currency-markery

```md
> [!WARNING] Ověřit k datu běhu — stav k <RRRR-MM>.
> <co se může změnit>
```

```md
> [!IMPORTANT] Slidy vs. realita
> <co říká slide> → <aktuální stav>.
```

## Delta sekce

Každý modul končí sekcí `## Stav produktu / delta` — co ověřit před dalším během.
