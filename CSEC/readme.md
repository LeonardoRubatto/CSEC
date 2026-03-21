# CalcEquation — Calculateur d'équation du second degré

| Champ | Valeur |
|---|---|
| **Domaine** | calculateur-marge.fr |
| **Langue** | Français |
| **Catégorie** | Éducation / Mathématiques |
| **Couleur accent** | `#0F766E` (teal) |
| **Logo mark** | `Δx` |

---

## Description

- Résolution d'équations du second degré `ax² + bx + c = 0` : discriminant Δ, racines réelles ou complexes, forme canonique, factorisation.
- Mode troisième degré `ax³ + bx² + cx + d = 0` via formule de Cardano + polish Newton-Raphson.
- Affichage pédagogique des étapes de calcul (optionnel).
- Vérification des racines par substitution (résidu numérique).
- Partage d'état via URL query params. Sauvegarde locale (`localStorage`).
- Mode sombre / clair, responsive mobile.

---

## Structure

```
calculateur-marge/
├── index.html
├── confidentialite.html
├── 404.html
├── robots.txt
├── sitemap.xml
├── _headers
├── readme.md
├── assets/
│   └── icons/
│       ├── warning.svg
│       ├── info.svg
│       ├── error.svg
│       ├── success.svg
│       ├── share.svg
│       ├── pdf.svg
│       ├── sources.svg
│       ├── theme-dark.svg
│       ├── theme-light.svg
│       └── france.svg
├── favicon.png          (32×32 — à produire manuellement)
├── apple-touch-icon.png (180×180 — à produire manuellement)
└── og-image.png         (1200×630 — à produire manuellement)
```

---

## Icônes

Tous les SVG doivent être installés dans `/assets/icons/` avant le déploiement.

`warning.svg, info.svg, error.svg, success.svg, share.svg, pdf.svg, sources.svg, theme-dark.svg, theme-light.svg, france.svg`

---

## Assets graphiques

| Fichier | Dimensions | Contenu |
|---|---|---|
| `favicon.png` | 32×32 px | Fond `#0F766E`, lettres **Δx** en blanc, bold, centré |
| `apple-touch-icon.png` | 180×180 px | Même design que favicon — iOS ajoute automatiquement les coins arrondis |
| `og-image.png` | 1200×630 px | Fond `#dde6ef`, card blanche centrée avec logo + « CalcEquation » + sous-titre « Calculateur d'équation du second degré » |

---

## Sources des données

| Donnée | Source | Date de vérification |
|---|---|---|
| Équation du second degré — définition | Programme de mathématiques de première générale (MEN) | 19/03/2026 |
| Discriminant Δ = b²-4ac | Programme officiel + Eduscol | 19/03/2026 |
| Interprétation du discriminant | OpenStax College Algebra 2e | 19/03/2026 |
| Formule quadratique | OpenStax College Algebra | 19/03/2026 |
| Forme canonique et sommet | Programme français + OpenStax | 19/03/2026 |
| Troisième degré — cubique réduit | NIST DLMF §4.43 | 19/03/2026 |
| Méthode numérique de Newton | NIST DLMF §3.8 | 19/03/2026 |

---

## Déploiement

1. Push le dossier sur GitHub
2. Cloudflare Pages détecte le push et déploie automatiquement
3. Pas d'outil de build — fichiers statiques purs

---

## Mise à jour des données

**Fréquence recommandée :** Annuelle (les formules mathématiques ne changent pas, mais vérifier si le programme officiel a été révisé).  
**Prochaine vérification :** mars 2027.
