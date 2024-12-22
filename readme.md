# 🛒 Walmart Sales Prediction Project

![Python](https://img.shields.io/badge/Python-3.7+-blue.svg)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.0+-orange.svg)
![Pandas](https://img.shields.io/badge/Pandas-2.0+-green.svg)

## 📋 Description
Un projet d'analyse prédictive visant à construire un modèle machine learning capable d'estimer les ventes hebdomadaires de différents magasins Walmart. Ce projet s'inscrit dans une démarche d'optimisation des stratégies commerciales et de gestion des stocks.

## 🎯 Objectifs du Projet
- Analyser en profondeur les facteurs influençant les ventes (économiques, temporels, environnementaux)
- Développer un modèle prédictif robuste pour l'estimation des ventes
- Comparer différentes approches de régularisation (Ridge vs Lasso)
- Fournir des recommandations business actionnables

## 🔍 Exploration des Données
Le dataset contient plusieurs types de variables :
- **Variables Économiques** : CPI, taux de chômage, prix du carburant
- **Variables Temporelles** : dates, périodes de vacances
- **Variables Environnementales** : température
- **Variable Cible** : ventes hebdomadaires en dollars

## 🛠️ Méthodologie
1. **Prétraitement des Données**
   - Nettoyage des valeurs manquantes
   - Suppression des outliers (règle des 3σ)
   - Feature engineering sur les variables temporelles
   - Encodage des variables catégorielles

2. **Modélisation**
   - Régression linéaire (baseline)
   - Régularisation Ridge
   - Régularisation Lasso
   - Optimisation par GridSearch

3. **Évaluation**
   - Métriques : R², MSE
   - Analyse des coefficients

## 📊 Résultats Clés
- R² score de 0.95 sur le jeu de test (Lasso)
- Identification des facteurs clés influençant les ventes :
  * Impact significatif du CPI (-30,097)
  * Fort effet du taux de chômage (-69,813)
  * Variations importantes entre magasins

## 💡 Insights Business
1. **Patterns Saisonniers**
   - Pics de ventes en février et juin
   - Impact des périodes de vacances

2. **Facteurs Économiques**
   - Forte sensibilité aux indicateurs économiques
   - Impact variable selon les magasins

3. **Recommendations**
   - Optimisation des stocks par saison
   - Stratégies pricing adaptatives
   - Plans d'action spécifiques par magasin

## 📁 Structure du Projet
    .
    ├── Walmart_sales_prediction.ipynb
    │
    ├── data/                          # Dossier des données
    │   └── Walmart_Store_sales.csv    # Dataset Walmart
    │
    ├── src/                           # sources
    │   ├── missing_holiday_flag.csv   # csv généré
    │   └── Walmart_Store_sales.csv    # dataset original
    │
    └── README.md                   # Documentation principale

## 📈 Axes d'Amélioration
- Test de modèles plus complexes (XGBoost, Random Forest)
- Analyse plus fine de la saisonnalité