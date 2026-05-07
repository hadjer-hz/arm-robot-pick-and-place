Bras Manipulateur 4DOF - Pick and Place
Simulation d'un bras manipulateur 4 degrés de liberté effectuant une tâche pick and place avec ROS2 Jazzy et Gazebo Harmonic.

Description
Le bras détecte la position d'un objet (cube rouge) à une position fixe connue et effectue les mouvements suivants :

Approche de l'objet
Saisie de l'objet
Levée de l'objet
Déplacement vers la position de dépôt
Dépôt de l'objet
Retour en position initiale

Technologies
ROS2 Jazzy
Gazebo Harmonic
Python 3
Ubuntu 24.04

Lancement
Terminal 1 - Lancer Gazebo
ros2 launch arm_gazebo arm_launch.py

Terminal 2 - Lancer le bridge ROS2-Gazebo
ros2 run ros_gz_bridge parameter_bridge /arm/joint1@std_msgs/msg/Float64@gz.msgs.Double /arm/joint2@std_msgs/msg/Float64@gz.msgs.Double /arm/joint3@std_msgs/msg/Float64@gz.msgs.Double /arm/joint4@std_msgs/msg/Float64@gz.msgs.Double

Terminal 3 - Lancer le noeud de controle
ros2 run arm_gazebo arm_node
