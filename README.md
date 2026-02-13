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
<h3>1- Corrélation des variables</h3>
<ul>
  <li>Aucune variable quantitative n’a montré de corrélation significative avec le prix.</li>
  <li>Deux variables qualitatives ont montré une relation significative avec la target (test ANOVA) :
    <ul>
      <li><b>ville</b></li>
      <li><b>type de logement</b></li>
    </ul>
  </li>
</ul>

<p><b>Question :</b> Devons-nous entraîner le modèle uniquement avec ces deux variables ou enrichir le dataset avec d’autres features ?</p>

<hr>

<h3>2- Résultats des modèles</h3>

<p>Nous avons entraîné plusieurs modèles de régression sur <code>df_filtered</code> pour prédire le prix par nuit.</p>

<h4>🔹 RandomForest (version initiale)</h4>

<ul>
  <li><b>R²</b> ≈ 0.826 (82 %)</li>
  <li><b>MAE</b> ≈ 41 DH</li>
  <li><b>RMSE</b> ≈ 93 DH</li>
</ul>

<h4>🔹 RandomForest après optimisation (GridSearchCV)</h4>

<ul>
  <li><b>R²</b> ≈ 0.980 (98 %)</li>
  <li><b>MAE</b> ≈ 12 DH</li>
  <li><b>RMSE</b> ≈ 30 DH</li>
</ul>

<p>L’optimisation des hyperparamètres a considérablement amélioré les performances du modèle.</p>

<hr>

<h3>3- Problème à discuter</h3>

<p>Devons-nous :</p>

<ul>
  <li>Utiliser le modèle optimisé pour la suite du projet ?</li>
  <li><b>OU</b></li>
  <li>Rester sur la version initiale pour éviter un possible surapprentissage (overfitting) ?</li>
</ul>