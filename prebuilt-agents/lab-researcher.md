# Lab 2 · Researcher — rešerše z vlastních dat

> Modul: M2 · Odhad: 20 min · Režim: vlastní tenant (BYOS), **vaše vlastní data**
> Oficiální zadání (EN): [Exercise — Use the Researcher agent](https://microsoftlearning.github.io/MS-4019-Transform-your-everyday-business-processes-with-agents/Instructions/Labs/M02-explore-prebuilt-microsoft-365-copilot-agents/05-exercise-researcher-agent.html)

## Scénář

Researcher propojí informace z **Outlooku, Teams a OneDrive/SharePointu**. Vyberte si **téma X** ze své práce za posledních 90 dní — projekt, zákazníka, interní změnu — a připravte si podklady, jako byste zítra šli na poradu.

> [!IMPORTANT] Soukromí
> Pracujete s **vlastní poštou a chaty**. Výsledky **nepromítejte** třídě, pokud obsahují osobní nebo zákaznická data. V diskusi mluvte o tom, **jak** agent pracoval, ne **co** našel.

## Předpoklady

- Agent **Researcher** vidíte v Agent Store ([pre-course check](../course-intro/pre-course-check.md), krok 3). Může mít **měsíční limit dotazů** — ptejte se promyšleně.
- Téma, ke kterému máte za 90 dní aspoň pár e-mailů, chatů nebo dokumentů.

## Kroky

1. **Copilot** → **Agents** → **Researcher**. (Když chybí: **All agents** / **Agent Store** → Researcher, Built by Microsoft.)
2. Hlavní prompt (doplňte téma):
   `Pomoz mi shromáždit a shrnout všechny nedávné diskuse, dokumenty a e-maily týkající se <téma X> za posledních 90 dní.`
3. Researcher se může **doptat** (rozsah, formát, detail) — odpovězte. Sledujte, jak postupuje.
4. **Počkejte** — odpověď může trvat i několik minut. Mezitím si přečtěte, jaké zdroje prochází.
5. Až přijde (dlouhá) odpověď, navažte:
   - `Shrň to do 5 odrážek.`
   - `Vypiš akční body, které se týkají mě.`
   - `Jaká klíčová rozhodnutí z komunikace vyplývají?`
6. Vytvořte výstup:
   `Napiš koncept e-mailu týmu se shrnutím stavu a dalšími kroky.`
7. **Ověřte citace**: otevřete 2 zdroje, na které Researcher odkazuje. Sedí to?

### Další prompty k vyzkoušení

- `Připrav mě na schůzku k <téma X>: co je otevřené, kdo co řeší, na co se zeptat.`
- `Jaký je aktuální stav a co blokuje <téma X>?`
- `Najdi nejnovější verzi dokumentu k <téma X> a shrň, co se změnilo.`

## Ověření

- [ ] Máte shrnutí tématu s **citacemi zdrojů**.
- [ ] Z dlouhé odpovědi jste si nechali udělat krátkou verzi.
- [ ] Ověřili jste aspoň 2 citace.
- [ ] Umíte říct, **z jakých typů zdrojů** Researcher čerpal (pošta / Teams / soubory / web).

## Fallback

- **Researcher nedostupný** → dvojice se spolužákem s licencí (on vybere nekonfidenční téma), nebo demo lektora.
- **Nemáte data** (nový účet, málo pošty) → téma z veřejného webu: `Připrav rešerši o dopadech směrnice NIS2 na středně velké firmy v Česku, s citacemi.` (vyžaduje povolený web grounding)

## Reflexe

Kolik času by vám tahle rešerše zabrala ručně? Čemu z výsledku byste **nevěřili** bez kontroly?
