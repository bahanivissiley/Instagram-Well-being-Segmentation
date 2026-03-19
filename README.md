# Instagram Well-being Segmentation 📱

Segmentation d'utilisateurs Instagram par clustering non supervisé pour analyser le lien entre comportements d'usage et bien-être.

## Contexte

Ce projet explore la question : **l'usage d'Instagram impacte-t-il le bien-être ?**  
À partir de données comportementales (22 variables d'usage) et d'indicateurs de bien-être (stress, sommeil, bonheur, IMC, tension artérielle), 4 profils d'utilisateurs ont été identifiés par K-Means.

---

## Pipeline

```
Chargement → EDA → Matrice de corrélation → Standardisation → PCA → K-Means → Analyse bien-être
```

### Étapes clés
- Catégorisation des variables : démographiques, comportementales Instagram, bien-être, style de vie
- Justification du nombre de composantes PCA par courbe de variance cumulée (seuil 85% → 7 composantes)
- Choix de k=4 par méthode du coude (KElbowVisualizer)
- Clustering sur l'espace PCA complet, visualisation sur PCA 2D séparée
- Analyse des indicateurs de bien-être par cluster + visualisation interactive Plotly

---

## Les 4 Personas identifiés

| Cluster | Nom | Profil |
|---|---|---|
| 0 | 🟢 Les Équilibrés | Usage modéré, bien-être dans la moyenne |
| 1 | 🔴 Les Épuisés | Usage intensif passif, stress et fatigue élevés |
| 2 | 🟡 Les Épanouis | Usage actif (création), bien-être préservé |
| 3 | 🟠 Les Sous Pression | Stress élevé indépendant du temps d'écran |

**Insight clé** : Ce n'est pas le *temps* passé sur Instagram qui prédit le bien-être, mais la *nature* de l'usage (passif vs actif).

---

## Stack

![Python](https://img.shields.io/badge/Python-3.10-blue)
![scikit-learn](https://img.shields.io/badge/scikit--learn-1.x-orange)
![Plotly](https://img.shields.io/badge/Plotly-interactive-blue)
![pandas](https://img.shields.io/badge/pandas-2.x-blue)

```bash
pip install -r requirements.txt
```

---

## Structure

```
instagram-wellbeing-segmentation/
├── instagram_wellbeing_segmentation.ipynb   # Notebook principal
├── instagram_usage_lifestyleSafe.csv        # Dataset comportemental
├── instagram_users_lifestyleSafe.csv        # Dataset utilisateurs
├── instagram_segments.csv                   # Export des clusters (généré)
├── requirements.txt
└── README.md
```

---

## Lancer le projet

```bash
git clone https://github.com/ton-username/instagram-wellbeing-segmentation
cd instagram-wellbeing-segmentation
pip install -r requirements.txt
jupyter notebook instagram_wellbeing_segmentation.ipynb
```

---

## Auteur

**Bahani** — [LinkedIn](https://linkedin.com/in/ton-profil) · [Portfolio](https://ton-portfolio.com)

*Projet académique — Epitech Lyon, MSc Data Science & Business Intelligence*
