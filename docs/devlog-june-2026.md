## [14 Juin 2026] - Système de Transformation (TF2) et URDF

### Objectifs
- Comprendre le fonctionnement des arbres de transformation (TF2) via la vidéo #6 d'Articulated Robotics.
- Créer un package Python propre et charger un modèle de robot basique (`.urdf.xacro`).

### Ce que j'ai appris & Difficultés résolues
- **C++ vs Python :** Choix de continuer en Python pour le prototypage rapide des concepts, avant de passer au C++ pour le contrôle temps réel en Master.
- **Évolution de ROS 2 :** Attention aux syntaxes obsolètes des vidéos. `static_transform_publisher` utilise désormais des flags explicites (`--x`, `--yaw`) et non plus des arguments positionnels.
- **WSL2 / WSLg :** En cas de blocage graphique d'RViz2 (`warn:copy mode`), un reset complet via `wsl --shutdown` dans le CMD Windows règle le problème.

### Commandes clés à retenir
```bash
# Lancer un transform statique (Nouvelle syntaxe)
ros2 run tf2_ros static_transform_publisher --x 2 --y 1 --z 0 --yaw 0.785 --frame-id world --child-frame-id robot1

# Générer le graphe de l'arbre TF
ros2 run tf2_tools view_frames