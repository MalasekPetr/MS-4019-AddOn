# Lab 1 · Analyst — průzkum Project Nexus

> Modul: M2 · Odhad: 20 min · Režim: vlastní tenant (BYOS)
> Oficiální zadání (EN): [Exercise — Use the Analyst agent](https://microsoftlearning.github.io/MS-4019-Transform-your-everyday-business-processes-with-agents/Instructions/Labs/M02-explore-prebuilt-microsoft-365-copilot-agents/03-exercise-analyst-agent.html)

## Scénář

Vaše firma 6 týdnů pilotovala novou digitální pracovní platformu — interní projekt **Project Nexus** — v odděleních IT, HR, Marketing a Operations. Máte výsledky průzkumu spokojenosti a do zítřka potřebujete pro vedení **trendy, anomálie a graf**.

## Předpoklady

- Agent **Analyst** vidíte v Agent Store ([pre-course check](../course-intro/pre-course-check.md), krok 3).

> [!NOTE] Jazyk
> Analyst podporuje omezený počet jazyků. Když na český prompt neodpoví nebo odpoví špatně, použijte anglickou verzi promptu z [oficiálního zadání](https://microsoftlearning.github.io/MS-4019-Transform-your-everyday-business-processes-with-agents/Instructions/Labs/M02-explore-prebuilt-microsoft-365-copilot-agents/03-exercise-analyst-agent.html) — a zapište si to jako zjištění.
- Soubor: [Project_Nexus_survey_results.xlsx](https://github.com/MicrosoftLearning/MS-4004-Empower-workforce-copilot-use-cases/raw/refs/heads/master/ResourceFiles/Project_Nexus_survey_results.xlsx) (fiktivní data, anglicky).

## Kroky

1. Stáhněte soubor Project Nexus do počítače.
2. Otevřete [`https://m365.cloud.microsoft.com`](https://m365.cloud.microsoft.com) → **Copilot** → **Agents** → **Analyst**.
3. Nahrajte soubor (ikona přílohy / **+** v poli pro prompt).
4. **Trendy:**
   `Analyzuj tuto tabulku a řekni mi tři hlavní trendy.`
5. **Čísla po kategoriích:**
   `Jaké je průměrné hodnocení v každé kategorii průzkumu?`
6. **Graf:**
   `Vytvoř sloupcový graf, který porovná průměrné hodnocení kategorií Project Satisfaction, Communication Effectiveness, Timeline Adherence a Overall Experience.`
7. **Zkontrolujte práci agenta:** rozbalte zobrazení kódu (Python), který Analyst spustil. Rozumíte, co spočítal?
8. **Vyberte si aspoň 2 další prompty** podle zájmu:
   - `Která kategorie má nejvyšší a která nejnižší průměrné hodnocení?`
   - `Liší se spokojenost mezi odděleními? Které oddělení je nejkritičtější?`
   - `Najdi v datech odlehlé hodnoty nebo podezřelé odpovědi.`
   - `Shrň nejčastější témata v textových komentářích.`
   - `Na základě dat navrhni 3 doporučení pro vedení, zda projekt rozšířit.`
9. **Plná anatomie promptu** (viz [README](README.md#anatomie-dobrého-promptu)): napište jeden prompt s cílem, kontextem, očekáváním a zdrojem — a porovnejte s krokem 4.

## Ověření

- [ ] Máte 3 trendy a průměry po kategoriích.
- [ ] Máte graf.
- [ ] Viděli jste kód, který Analyst spustil, a umíte jednou větou říct, co dělá.
- [ ] Porovnali jste krátký prompt vs. prompt s plnou anatomií — **co konkrétně** se zlepšilo?

## Fallback

- **Analyst nedostupný** → pracujte ve dvojici se spolužákem s licencí, nebo sledujte demo lektora a pište si predikce („co agent odpoví?").
- **Copilot Chat bez licence**: nahrajte soubor do běžného Copilot Chatu a zkuste kroky 4–6. Porovnejte s Analystem u souseda — kde je rozdíl?

## Reflexe

Kde byste Analyst použili ve své práci? Jaká data máte, na kterých byste ho zítra pustili?
