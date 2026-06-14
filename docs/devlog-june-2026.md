## [14 Juin 2026] - Système de Transformation (TF2) et URDF

### Objectifs
- Comprendre le fonctionnement des arbres de transformation (TF2) via la vidéo #6 d'Articulated Robotics.
- Créer un package Python propre et charger un modèle de robot basique (`.urdf.xacro`).

### Ce que j'ai appris & Difficultés résolues
- **C++ vs Python :** Choix de continuer en Python pour le prototypage rapide des concepts, j'imagine que C++ est utilisé plus souvent dans le monde academique, il faudra l'apprendre apres.
- **Évolution de ROS 2 :** Attention aux syntaxes obsolètes des vidéos. `static_transform_publisher` utilise désormais des flags explicites (`--x`, `--yaw`) et non plus des arguments positionnels.
- **WSL2 / WSLg :** En cas de blocage graphique d'RViz2 (`warn:copy mode`), un reset complet via `wsl --shutdown` dans le CMD Windows règle le problème.

### Commandes clés à retenir
```bash
# Lancer un transform statique (Nouvelle syntaxe)
ros2 run tf2_ros static_transform_publisher --x 2 --y 1 --z 0 --yaw 0.785 --frame-id world --child-frame-id robot1

#Pour faire un push sur git
cd ~/ros2_ws

# 1. Sélectionner toutes les modifications (nouveaux packages, fichiers modifiés, devlog...)
git add .

# 2. Enregistrer la "photo" avec un message décrivant ce que vous avez fait
git commit -m "Feat: Ajout du robot de la vidéo 7 et mise à jour du devlog"

# 3. Envoyer le tout sur GitHub
git push

# Générer le graphe de l'arbre TF
ros2 run tf2_tools view_frames



## [14 Juin 2026] - Système de Transformation (TF2) et URDF

### Objectifs
- Texte.
- Texte.

### Ce que j'ai appris & Difficultés résolues
- **Titre1 :** Texte.
- **Titre2 :** Texte.

### Commandes clés à retenir