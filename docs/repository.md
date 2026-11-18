# Repozytorium: opis i tagi

Rzeczy, które ustawia się na GitHubie ręcznie (nie da się ich zapisać w plikach repozytorium). Przegląd projektu: [README](../README.md).

## Opis i tagi (About)

GitHub: strona repozytorium → ⚙ obok „About” → pola poniżej. Opis ma limit 350 znaków, tagi (topics) pisze się małymi literami z myślnikami, najwyżej 20.

**Opis (Description):**

```text
Responsive, mobile-first landing page for an ice-cream brand: hero, products with modals, gallery, reviews slider (Swiper), contacts and mobile menu. Semantic HTML5, BEM, SASS, Parcel; deployed to GitHub Pages by GitHub Actions.
```

**Strona (Website):**

```text
https://damtchorzewski.github.io/IceCream/
```

**Tagi (Topics):**

```text
html5 sass scss bem parcel swiper landing-page responsive-design mobile-first github-pages github-actions javascript front-end
```

Z GitHub CLI (`gh`) to samo jedną komendą:

```bash
gh repo edit DamTchorzewski/IceCream --homepage "https://damtchorzewski.github.io/IceCream/" --description "Responsive, mobile-first landing page for an ice-cream brand: hero, products with modals, gallery, reviews slider (Swiper), contacts and mobile menu. Semantic HTML5, BEM, SASS, Parcel; deployed to GitHub Pages by GitHub Actions." --add-topic html5,sass,scss,bem,parcel,swiper,landing-page,responsive-design,mobile-first,github-pages,github-actions,javascript,front-end
```

## Ustawienia do włączenia

| Gdzie (GitHub)                                          | Co ustawić                                                              |
| ------------------------------------------------------- | ----------------------------------------------------------------------- |
| Settings → Pages                                        | źródło: gałąź `gh-pages`, folder `/ (root)` (publikuje ją `deploy.yml`) |
| Settings → General → Default branch                     | `main` (już jest)                                                       |
| Settings → Branches (albo Rulesets) → `main`, `develop` | zablokuj force push i usuwanie gałęzi                                   |
