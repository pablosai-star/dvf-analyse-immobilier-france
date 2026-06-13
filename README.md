dvf-analyse-immobilier-france
Analyse du marché immobilier français (2021–2025) à partir des données DVF — EDA, visualisations et modèle prédictif Random Forest.
🏠 Analyse Immobilier France — DVF (2021–2025)

Exploration et modélisation du marché immobilier français à partir
des Demandes de Valeurs Foncières (DVF) publiées par data.gouv.fr.

🎯 Objectif

Analyser les tendances des prix immobiliers en France sur 4 ans,
identifier les facteurs clés du prix au m², et construire un modèle
prédictif des prix de vente.

📦 Dataset

- Source : [data.gouv.fr — Demandes de Valeurs Foncières](https://www.data.gouv.fr/fr/datasets/demandes-de-valeurs-foncieres/)
- Période : 2021 à 2025
- Volume : ~4 millions de transactions (échantillon aléatoire utilisé)
- Contenu : Type de bien, surface, localisation, prix de vente

🛠️ Stack

- Python : Pandas, Matplotlib, Seaborn
- Machine Learning : Scikit-learn (Random Forest Regressor)
- PowerPoint : Présentation exécutive

📁 Structure du repo

├── projet_immo_step.ipynb          # Notebook principal — EDA + ML
├── dvf_clean.csv                   # Dataset nettoyé
├── dvf_combined.csv                # Dataset combiné multi-années
├── stats_departements.csv          # Statistiques par département
├── visualisations.png              # Graphiques EDA
├── resultats_ml.png                # Résultats du modèle
├── analyse_immobilier_france.pptx  # Présentation PowerPoint
└── README.md

📊 Key Insights

- Prix moyen au m² en forte disparité entre Paris/IDF et le reste
  de la France
- Surface et localisation sont les deux variables les plus
  corrélées au prix de vente
- Appartements vs maisons : dynamiques de prix distinctes
  selon les régions
  -Modèle Random Forest : R² = 0.44 après optimisation
  (target encoding, log transformation, feature surface/pièce)

🤖 Modèle Prédictif

- Algorithme : Random Forest Regressor
- Feature engineering : ratio surface/pièce, target encoding
  des départements, log transformation du prix
- Résultat : R² = 0.44 sur le jeu de test

📥 Données brutes

Les fichiers DVF annuels (500 Mo+ chacun) ne sont pas inclus dans
ce repo. Disponibles directement sur :
👉 https://www.data.gouv.fr/fr/datasets/demandes-de-valeurs-foncieres/
