# Dijkstra Path Planning Algorithm

## Description

L'algorithme de Dijkstra est utilisé pour trouver le chemin le plus court entre un point de départ et un point d'arrivée sur une carte de coût (généralement une grille). Il fonctionne en explorant les nœuds voisins, en les triant par coût de parcours, et en s'assurant de trouver le chemin optimal, tout en minimisant le coût total.

Cet algorithme est couramment utilisé dans des applications de robotique pour la planification de trajectoires, notamment dans des environnements à coût variable (par exemple, obstacles ou zones à éviter).

## Installation

vérifier si vous avez la version 3 de python 
bash
```
sudo apt update
```
télécharger si non:

sudo apt install python3


### Prérequis
Avant de pouvoir utiliser l'algorithme, assurez-vous que les outils suivants sont installés sur votre machine :

- **ROS Noetic** (ou une version compatible)
- **Python 3** et les packages nécessaires
- **`gridviz`** : Pour la visualisation de la grille
- **Les modules d'algorithmes** (Dijkstra, A*, etc.)

### Étapes d'installation

1. Clonez le dépôt :
   ```bash
   git clone https://github.com/ton-utilisateur/dijkstra-path-planning.git
