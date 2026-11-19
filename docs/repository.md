# Repozytorium: opis i tagi

Rzeczy, które ustawia się na GitHubie ręcznie (nie da się ich zapisać w plikach repozytorium). Przegląd projektu: [README](../README.md).

## Zmiana nazwy na `ice-cream`

Standard nazw repozytoriów: `reops/standards/repo-names.md`. Kolejność:

1. GitHub: Settings → General → Repository name → `ice-cream`. Adres repozytorium GitHub przekieruje, ale **adres strony (GitHub Pages) zmieni się** z `.../IceCream/` na `.../ice-cream/`, a stary przestanie działać.
2. Lokalnie: folder `ice-cream` i `git remote set-url origin https://github.com/DamTchorzewski/ice-cream.git`.
3. Wypchnij `main`: workflow `deploy.yml` zbuduje stronę z `--public-url /ice-cream/` (to już jest w `package.json`) i opublikuje ją w `gh-pages`. Settings → Pages powinno wskazywać `gh-pages` / root.
4. Linki do strony w innych repozytoriach (`WebCraftStudio`: `project-6.html`) wskazują już nowy adres.

## Opis i tagi (About)

GitHub: strona repozytorium → ⚙ obok „About” → pola poniżej. Opis ma limit 350 znaków, tagi (topics) pisze się małymi literami z myślnikami, najwyżej 20.

**Opis (Description):**

```text
Landing page of an ice-cream brand: product range with detail windows, brand story, gallery, a customer-reviews slider, shops with opening hours and a mobile menu. Mobile-first and fast (static, Parcel), deployed to GitHub Pages on every push, so the brand is easy to find and read on any device.
```

**Strona (Website):**

```text
https://damtchorzewski.github.io/ice-cream/
```

**Tagi (Topics):**

```text
landing-page html5 sass scss bem parcel swiper responsive-design mobile-first github-pages github-actions javascript front-end
```

Z GitHub CLI (`gh`) to samo jedną komendą:

```bash
gh repo edit DamTchorzewski/ice-cream --homepage "https://damtchorzewski.github.io/ice-cream/" --description "Landing page of an ice-cream brand: product range with detail windows, brand story, gallery, a customer-reviews slider, shops with opening hours and a mobile menu. Mobile-first and fast (static, Parcel), deployed to GitHub Pages on every push, so the brand is easy to find and read on any device." --add-topic landing-page,html5,sass,scss,bem,parcel,swiper,responsive-design,mobile-first,github-pages,github-actions,javascript,front-end
```

## Ustawienia do włączenia

| Gdzie (GitHub)                                          | Co ustawić                                                              |
| ------------------------------------------------------- | ----------------------------------------------------------------------- |
| Settings → Pages                                        | źródło: gałąź `gh-pages`, folder `/ (root)` (publikuje ją `deploy.yml`) |
| Settings → General → Default branch                     | `main` (już jest)                                                       |
| Settings → Branches (albo Rulesets) → `main`, `develop` | zablokuj force push i usuwanie gałęzi                                   |
