# CalcEquation

> Calculateur d'équations du second et troisième degré — discriminant, racines réelles et complexes, forme canonique  
> Domaine : https://equations.wecalc.fr · Langue : fr · Catégorie : Éducation · Accent : `#0F766E`

## Fonctionnalités

- Résolution d'équations du second degré ax² + bx + c = 0 : calcul du discriminant Δ, racines réelles (Δ > 0), racine double (Δ = 0) ou racines complexes conjuguées (Δ < 0)
- Résolution d'équations du troisième degré : méthode de Cardan, racines réelles et complexes, forme trigonométrique si Δ < 0
- Affichage de la forme canonique (forme sommet) et de la factorisation de l'équation
- Saisie des coefficients a, b, c (et d pour le 3ème degré) avec validation en temps réel et affichage de toutes les étapes intermédiaires
- Partage de résultat par URL encodée, dark mode, cookie banner RGPD, responsive mobile
- 4 blocs JSON-LD : `WebApplication`, `WebSite`, `BreadcrumbList`, `FAQPage` — rich results Google activés

## Structure des fichiers

```
CSEC/
├── index.html
├── confidentialite.html
├── 404.html
├── _headers
├── robots.txt
├── sitemap.xml
├── readme.md
├── favicon.png
├── apple-touch-icon.png
├── og-image.png
└── assets/
    └── icons/
        ├── logo-fibo4.svg
        ├── bonus.svg
        ├── calc.svg
        ├── egal.svg
        ├── error.svg
        ├── europe.svg
        ├── exam.svg
        ├── france.svg
        ├── monitor.svg
        ├── op.svg
        ├── pdf.svg
        ├── share.svg
        ├── sources.svg
        ├── sources-dark.svg
        ├── success.svg
        ├── swap.svg
        ├── theme-dark.svg
        ├── theme-light.svg
        └── warning.svg
```

## Icônes SVG requises

Installer dans `/assets/icons/` : `logo-fibo4.svg`, `bonus.svg`, `calc.svg`, `egal.svg`, `error.svg`, `europe.svg`, `exam.svg`, `france.svg`, `monitor.svg`, `op.svg`, `pdf.svg`, `share.svg`, `sources.svg`, `sources-dark.svg`, `success.svg`, `swap.svg`, `theme-dark.svg`, `theme-light.svg`, `warning.svg`

## Sources des données

| Source | Organisme | URL | Vérifié le |
|--------|-----------|-----|------------|
| Formule du discriminant et résolution ax² + bx + c = 0 | Programme officiel de mathématiques — Terminale | https://eduscol.education.fr | 2026-03-19 |
| Méthode de Cardan — résolution du 3ème degré | Programme de mathématiques — Classes préparatoires | https://eduscol.education.fr | 2026-03-19 |
| Forme trigonométrique des racines complexes | MPSI/PCSI — Cours officiels | https://eduscol.education.fr | 2026-03-19 |

## Déploiement

Push GitHub → Cloudflare Pages. Aucun outil de build. Le dossier `CSEC/` est la racine du site.

```bash
git add .
git commit -m "update: [description courte]"
git push origin main
```

Cloudflare Pages détecte le push et redéploie automatiquement en ~30 secondes.

## Mise à jour des données

- Fréquence recommandée : lors de réformes des programmes de mathématiques (rare — tous les 5–10 ans)
- Prochaine vérification : septembre 2028
- Fichiers à mettre à jour : `index.html` (formules dans le code, année dans le title), `sitemap.xml` (`lastmod`)

## Assets graphiques à produire manuellement

| Fichier | Dimensions | Contenu |
|---------|------------|---------|
| `favicon.png` | 32×32 px | Fond `#0F766E`, caractères **Δx** en blanc, bold, centré |
| `apple-touch-icon.png` | 180×180 px | Même design — iOS arrondit automatiquement les coins |
| `og-image.png` | 1200×630 px | Fond `#dde6ef`, card blanche centrée : logo + "Calculateur Équation du Second Degré 2026 — Discriminant, Racines, Factorisation" |
