# Projet Prédiction des Loyers Airbnb au Maroc

## Description
Ce projet a pour objectif de prédire les loyers des logements Airbnb au Maroc en utilisant des données collectées via web scraping et en appliquant des techniques de Machine Learning.

## Structure du projet
- `Codes/` : Dossier contenant les codes
    - `EDA+Nettoyage+Prétraitement.ipynb` : notebook pour l’EDA, le nettoyage et le prétraitement
    - `Scraping.ipynb` : notebook pour la récupération des données depuis Airbnb
- `Datasets/` : Dossier contenant les données
    - `data_scraped.csv` : données brutes collectées
    - `data_nettoyee.csv` : données nettoyées et prêtes pour le modèle
- `requirements.txt` : liste des bibliothèques nécessaires

## Instructions pour exécuter le projet

1. **Cloner le projet**
```bash
git clone https://github.com/Bahriilhame/Airbnb-price-prediction.git
cd Airbnb-price-prediction
```

## Gaps identifiés
Lors de notre exploration et préparation des données, nous avons identifié les points suivants :
<ul>
    <li>Aucune variable quantitative n'a montré de corrélation significative avec le loyer.</li>
    <li>Seules deux variables qualitatives ont montré une relation avec la target après test ANOVA :
        <ul>
            <li>ville</li>
            <li>type de logement</li>
        </ul>
    </li>
</li>
</ul>

## Problème : 
On ne sait pas encore si l'entraînement du modèle doit se faire uniquement avec ces deux colonnes ou si d'autres techniques/features doivent être envisagées.