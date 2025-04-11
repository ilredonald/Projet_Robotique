#Path Planning Algorithm

## Description

ce dépôt contient des algorithmes de A*, dijkstra, greedy qui permet de planifier la trajectoire du robot pour atteindre un but.

### Prérequis
Avant de pouvoir utiliser l'algorithme, assurez-vous que les outils suivants sont installés sur votre machine :

- **ROS Noetic** (ou une version compatible)
- **Python 3** et les packages nécessaires
- **`gridviz`** : Pour la visualisation de la grille
- **Les modules d'algorithmes** (Dijkstra, A*, etc.)

### Étapes d'installation

Clonez le dépôt :
```bash
   git clone https://github.com/ilredonald/Projet_Robotique.git
```
vérifier si vous avez la version 3 de python 
bash
```
sudo apt update
```
télécharger la, si non:
bash
```
sudo apt install python3
```

## Procédure :

dézippez le fichier `workspace` et sourcez les fichiers :
bash
```
cd ~/workspace
catkin_make
source ~/workspace/devel/setup.bash
```

Lancez la simulation TurtleBot3, et laissez le terminal ouvert. Une fenêtre Gazebo affichant le robot
 TurtleBot3 dans son environnement s’ouvrira.
 bash
```
 roslaunch ros_world turtlebot3_world.launch
```
 En gardant le terminal précédent ouvert, ouvrez un nouveau terminal. Sourcez à nouveau les fichiers
 , puis démarrez le nœud de planification de chemin pour TurtleBot3. Une fenêtre RViz
 s’ouvrira montrant le robot dans le même environnement sous format grille.
 bash
```
 roslaunch global_path_planning turtlebot3_ros_world.launch
```
 En gardant le terminal précédent ouvert, ouvrez un nouveau terminal. Sourcez encore une fois les
 fichiers . D´emarrez ensuite le serveur de planification de chemin. V´erifiez le second
 terminal (celui du nœud de planification) pour valider le bon fonctionnement.
 bash
```
 rosrun global_path_planning path_planning_server.py
```
 Dans la fenêtre RViz, sélectionnez le bouton 2D Nav Goal et indiquez la position cible sur la carte.
 L’orientation peut être définie en maintenant et déplaçant le curseur. Après avoir défini la position,
 la visualisation de l’algorithme de planification de chemin choisi démarrera.
 
Par défaut, l’algorithme astar est actif. Pour changer d’algorithme de planification (choix entre
 astar, dijkstra, greedy), modifiez le fichier :
 bash
```
 src/global_path_planning/src/path_planning_server.py
```
