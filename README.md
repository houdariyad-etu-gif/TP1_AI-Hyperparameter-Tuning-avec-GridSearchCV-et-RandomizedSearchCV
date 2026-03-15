# TP1 : Hyperparameter Tuning avec GridSearchCV et RandomizedSearchCV

## Description
Ce TP explore l'optimisation des hyperparamètres d'un modèle RandomForest sur le dataset Breast Cancer.

## Contenu
- `tp1.ipynb` : Notebook principal

## Parties
1. Préparation des données (80/20)
2. Modèle Baseline
3. GridSearchCV
4. RandomizedSearchCV
5. Comparaison des résultats

## Dataset
- Dataset : Breast Cancer (scikit-learn)
- Total échantillons : 569
- Ensemble d'entraînement : 455 échantillons (80%)
- Ensemble de test : 114 échantillons (20%)

## Résultats et Comparaison

| Modèle             | Accuracy |
|--------------------|----------|
| Baseline           | 96.49%   |
| GridSearchCV       | 96.49%   |
| RandomizedSearchCV | 96.49%   |

Les trois modèles donnent la même accuracy de 96.49%.Cela montre que le modèle Baseline avec ses paramètres par défaut est déjà très bon sur ce dataset.

GridSearchCV teste TOUTES les combinaisons possibles (405 fits), il est exhaustif mais lent. Il est conseillé quand le dataset est petit et l'espace de recherche limité.

RandomizedSearchCV choisit aléatoirement un nombre limité de combinaisons (100 fits), il est plus rapide. Il est conseillé quand le dataset est grand ou quand l'espace de recherche est très large.

Les deux méthodes arrivent au même résultat ici, donc sur ce dataset RandomizedSearchCV est suffisant et moins coûteux.

## Libraries utilisées
- scikit-learn
- numpy
