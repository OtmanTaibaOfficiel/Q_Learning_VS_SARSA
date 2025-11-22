# Q_Learning_VS_SARSA

## Description

Ce projet compare deux algorithmes d'apprentissage par renforcement : **Q-Learning** et **SARSA**, en utilisant un notebook Jupyter (`Q_learning_vs_sarsa.ipynb`) sur l'environnement **FrozenLake 8x8** avec carte personnalisée.

L'objectif est d'analyser :

* Le taux de réussite pour atteindre le **Goal (G)** depuis le **Start (S)**.
* La longueur et la sécurité des chemins calculés par chaque algorithme.
* La performance globale en termes de récompense moyenne et d’efficacité de l’exploration.

---

## Carte 8x8 utilisée

```
F F F F F F F F
S F F F F F F F
F F F F F F F F
F F F F F F F F
F F F F F F F F
F F F F F F F F
F H H H H H F F
F F F F F F F G
```

* **S** : Start (départ)
* **F** : Frozen (case sûre)
* **H** : Hole (trou)
* **G** : Goal (objectif final)

---

## Contenu du projet

* `Q_learning_vs_sarsa.ipynb` : notebook avec implémentations Q-Learning et SARSA, visualisations et analyse comparative.
* `README.md` : ce fichier.

---

## Installation

Assurez-vous d'avoir Python ≥ 3.8 et Jupyter Notebook, puis installez les dépendances :

```bash
pip install numpy matplotlib gymnasium notebook
```

Lancez le notebook :

```bash
jupyter notebook Q_learning_vs_sarsa.ipynb
```

---

## Paramètres principaux

* **Alpha (α)** : 0.1 (taux d’apprentissage)
* **Gamma (γ)** : 0.95 (facteur d’actualisation)
* **Epsilon (ε)** : 1.0 (exploration initiale)
* **Epsilon decay** : 0.998 (décroissance)
* **Epsilon min** : 0.01
* **Episodes** : 2000
* **Max steps** : 200

Ces paramètres assurent un apprentissage stable sur la carte 8x8.

---

## Fonctionnalités du notebook

1. **Entraînement des deux algorithmes** (Q-Learning et SARSA).
2. **Visualisation des performances** :

   * Reward moyen vs épisodes
   * Taux de succès (%) vs épisodes
3. **Tracé des chemins S → G** pour Q-Learning (optimal) et SARSA (safe).
4. **Test final** sur 10 épisodes avec rendu humain pour observer le comportement réel.
5. **Analyse comparative** des performances et des chemins.

---

## Structure du dépôt

```
Q_Learning_VS_SARSA/
│── Q_learning_vs_sarsa.ipynb
│── README.md
```

---

## Auteur

**Otman Taiba**
Étudiant en Master Master Machine Learning Avancé et Intelligence Multimédia
Projet pédagogique sur DEEP REINFORCEMENT LEARNING AND MULTIMODAL GENERATIVE AI.

---

## Licence

Projet libre d'utilisation et modifiable à des fins pédagogiques et de recherche.
