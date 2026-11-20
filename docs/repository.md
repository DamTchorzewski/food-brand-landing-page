# Repozytorium: opis i tagi

Rzeczy, które ustawia się na GitHubie ręcznie (nie da się ich zapisać w plikach repozytorium). Przegląd projektu: [README](../README.md).

## Nazwa repozytorium: `food-brand-landing-page`

Standard nazw repozytoriów: `reops/standards/repo-names.md`. Repozytorium nazywało się wcześniej `IceCream`, potem `ice-cream`; od 2026-11-20 nazywa się `food-brand-landing-page` (nazwa mówi, czym jest projekt: fraza szukana na GitHubie). GitHub przekierowuje stary adres repozytorium, ale **adres strony (GitHub Pages) zmienił się** na `https://damtchorzewski.github.io/food-brand-landing-page/`, a stary przestał działać. Workflow `deploy.yml` buduje stronę z `--public-url /food-brand-landing-page/` (to jest w `package.json`) i publikuje ją oficjalnymi akcjami Pages; Settings → Pages → Source jest ustawione na **GitHub Actions**. Stary link do strony w `WebCraftStudio` (`project-6.html`) zniknął razem z tą stroną: repozytorium jest teraz szablonem `portfolio-website-template` bez prawdziwych projektów, więc nie ma już czego poprawiać.

## Opis i tagi (About)

GitHub: strona repozytorium → ⚙ obok „About” → pola poniżej. Opis ma limit 350 znaków, tagi (topics) pisze się małymi literami z myślnikami, najwyżej 20.

**Opis (Description):**

```text
Mobile-first static landing page in HTML, SASS and BEM, built with Parcel.
```

**Strona (Website):**

```text
https://damtchorzewski.github.io/food-brand-landing-page/
```

**Tagi (Topics):**

```text
landing-page html5 sass bem parcel swiper responsive-design mobile-first github-pages github-actions javascript front-end
```

Z GitHub CLI (`gh`) to samo jedną komendą:

```bash
gh repo edit DamTchorzewski/food-brand-landing-page --homepage "https://damtchorzewski.github.io/food-brand-landing-page/" --description "Mobile-first static landing page in HTML, SASS and BEM, built with Parcel." --add-topic landing-page --add-topic html5 --add-topic sass --add-topic bem --add-topic parcel --add-topic swiper --add-topic responsive-design --add-topic mobile-first --add-topic github-pages --add-topic github-actions --add-topic javascript --add-topic front-end
```

## Ustawienia do włączenia

| Gdzie (GitHub)                                          | Co ustawić                                          |
| ------------------------------------------------------- | --------------------------------------------------- |
| Settings → Pages                                        | Source: **GitHub Actions** (publikuje `deploy.yml`) |
| Settings → General → Default branch                     | `main` (już jest)                                   |
| Settings → Branches (albo Rulesets) → `main`, `develop` | zablokuj force push i usuwanie gałęzi               |
