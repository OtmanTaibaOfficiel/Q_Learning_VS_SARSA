# Q_Learning_VS_SARSA

## Description

Ce projet compare deux algorithmes d'apprentissage par renforcement : **Q-Learning** et **SARSA**, sur un environnement **FrozenLake 8x8** avec carte personnalisée.

L'objectif est d'analyser la performance de chaque algorithme pour atteindre le **Goal (G)** depuis le **Start (S)** en évitant les trous (Holes).

---

## Carte utilisée (8x8)

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

L'environnement est **slippery**, les déplacements peuvent donc être aléatoires.

---

## Contenu du projet

* `Q_learning_vs_sarsa.py` : code principal avec implémentations Q-Learning et SARSA
* `plots/` : dossier contenant les graphiques générés (reward, succès, chemins)
* `README.md` : ce fichier

---

## Installation

Assurez-vous d’avoir Python ≥ 3.8 et installez les dépendances :

```bash
pip install numpy matplotlib gymnasium
```

---

## Paramètres du projet

* **Alpha (α)** : 0.1 → taux d'apprentissage
* **Gamma (γ)** : 0.95 → facteur d’actualisation
* **Epsilon (ε)** : 1.0 → exploration initiale
* **Epsilon decay** : 0.998 → décroissance progressive
* **Epsilon min** : 0.01 → exploration minimale
* **Episodes** : 2000
* **Max steps** : 200

Ces paramètres assurent une exploration suffisante et un apprentissage stable sur la carte 8x8.

---

## Utilisation

Exécutez le script principal :

```bash
python Q_learning_vs_sarsa.py
```

Le code effectuera :

1. L'entraînement des deux algorithmes sur 2000 épisodes.
2. La génération de graphiques comparatifs :

   * Reward moyen vs épisodes
   * Taux de succès (%) vs épisodes
3. Le tracé des chemins S → G pour Q-Learning et SARSA.
4. Un test final sur 10 épisodes en mode rendu humain.
5. Une analyse comparative détaillée des performances.

---

## Visualisation

* **Graphiques reward/success** : permettent d'observer la convergence et les différences entre Q-Learning et SARSA.
* **Chemins sur la carte** : Q-Learning → chemin optimal, SARSA → chemin safe.
* **Test final** : montre les performances réelles des algorithmes avec visualisation.

---

## Analyse et résultats attendus

* **Q-Learning** : plus rapide, trouve des chemins optimaux mais risque de tomber dans les trous.
* **SARSA** : plus sûr, peut prendre des chemins plus longs mais minimise le risque d’échec.
* Comparaison quantitative :

  * Récompense moyenne sur 100 derniers épisodes
  * Taux de réussite
  * Longueur des chemins S → G
  * Max / moyenne des Q-values

---

## Structure du projet

```
Q_Learning_VS_SARSA/
│── Q_learning_vs_sarsa.py
│── README.md
│── plots/
```

---

## Licence

Ce projet est libre d’utilisation et modifiable pour des fins pédagogiques et de recherche.

---

## Auteur

**Otman Taiba**
Étudiant en Master Intelligence Artificielle
Projet pédagogique et de recherche sur l’apprentissage par renforcement.
