# Analyse bayésienne de la toxicité des sels sur les larves d’éphémères

Ce projet a pour but d’évaluer la toxicité de trois types de sels (NaCl, CaCl₂ et Sel commercial) sur la survie des larves d’éphémères (*mayflies*) à l’aide de **modèles statistiques bayésiens** en **R**.

## 🎯 Objectif

Mesurer et comparer l’impact de différentes concentrations de sels sur la survie des larves afin de déterminer :
- Quel sel est le plus toxique ?
- Quelle est la concentration létale médiane (CL50) pour chaque type de sel ?
- Quels modèles permettent de mieux expliquer la relation dose-réponse ?

## 📁 Contenu du dépôt

- `logistic_regression.Rmd` : code complet d’analyse bayésienne (R Markdown)
- `rapport_mayflies.pdf` : rapport final détaillant la méthodologie, les résultats et les interprétations
- `donnees.csv` : jeu de données utilisé dans les analyses
- `README.md` : ce fichier

## 🧠 Méthodes utilisées

- Analyse descriptive et détection d’anomalies
- Modèles bayésiens :
  - Régression log-logistique
  - Modèle de Weibull
  - Régression logistique bayésienne (via STAN)
  - Modèles de Poisson, Probit et Robit
- Validation MCMC :
  - Traceplots
  - Rhat
  - Taille d’échantillon effectif
- Vérification par données simulées ("Fake Data Check")

## 🔧 Technologies

- **R** et **RStudio**
- **rstan**, **runjags**, **brms**, **tidyverse**
- Visualisations avec `ggplot2`

## 📊 Reproduire l'analyse

1. Ouvrir `logistic_regression.Rmd` dans **RStudio**
2. Vérifier que `donnees.csv` est bien dans le dossier
3. Lancer (`Knit`) vers PDF ou HTML

> 💡 Si STAN est utilisé, assurez-vous que `rstan` est bien installé et que l’environnement R est compatible.

## 🔍 Résultats principaux

- Le **sel commercial** est le moins toxique (CL50 ≈ 55 g/L)
- Le **NaCl** est le plus toxique à haute concentration (CL50 ≈ 40 g/L)
- Le modèle log-logistique donne une estimation fiable des concentrations létales
- La régression logistique bayésienne identifie des effets différenciés selon les types de sel

## 📌 Interprétation

Les résultats suggèrent que le **remplacement de NaCl ou CaCl₂ par un sel commercial** pourrait réduire l'impact environnemental sur les espèces aquatiques sensibles.

## 👨‍🎓 Auteurs

Projet réalisé par :
- Aymane Mimoun
- Alexandre Combeau
- Jaad Belhouari
- Janikson Garcia Brito
- Hajar Lamtaii

M2 Data Science, Université Paris-Saclay — Mars 2024

---

## 📬 Contact

Pour toute question ou collaboration, n’hésitez pas à me contacter via GitHub.

