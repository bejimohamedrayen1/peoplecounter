Ce projet est réalisé dans le cadre du module Communication Sans Fil en Licence 1 à l’Université
Nice Sophia Antipolis.

# Lien vers le slide

**----->** [Slide de la présentation du projet](peoplecounter/PEOPLECOUNTER.pdf)
# peoplecounter
Le projet PeopleCounter est un système intelligent conçu pour comptabiliser en temps réel le nombre de personnes entrant et sortant d'une pièce, en utilisant des capteurs de mouvement. Le système repose sur une plateforme Arduino et utilise principalement des capteurs PIR (Passive InfraRed), un à gauche et un à droite de l'entrée de la pièce. Ces capteurs détectent les mouvements en captant les variations des rayonnements infrarouges émis par les corps humains. Le capteur à gauche est responsable de détecter les personnes entrant dans la pièce, tandis que celui à droite détecte celles qui en sortent.

Lorsque le capteur PIR gauche détecte une entrée, le compteur de personnes est incrémenté, et lorsque le capteur PIR droit détecte une sortie, le compteur est décrémenté. Ce processus assure une gestion précise et en temps réel du nombre de personnes présentes dans la pièce. Une fonctionnalité clé de ce système est sa capacité à transmettre les données de comptage vers une plateforme externe via un module LoRa à 868 MHz. Ce module sans fil permet d’envoyer le nombre de personnes présentes dans la pièce à une unité réceptrice distante, ce qui est particulièrement utile pour une gestion à distance ou dans des environnements de grande taille.

Le système est conçu pour être simple et efficace, avec un délai de 300 ms intégré pour éviter les erreurs de comptage dues aux rebonds des capteurs PIR. Le projet peut être étendu à l'avenir pour intégrer d'autres fonctionnalités telles que l'envoi de notifications ou l'intégration dans des systèmes de gestion de bâtiment intelligents.

Tous les composants du système sont intégrés dans un boîtier personnalisé imprimé en 3D, offrant une solution compacte et esthétique. Le projet PeopleCounter est une application pratique de technologies modernes de détection de mouvement, de communication sans fil et de gestion des espaces, et constitue une excellente opportunité d'apprentissage en programmation Arduino, électronique et développement de prototypes. Ce projet pourrait avoir de nombreuses applications dans des domaines comme la gestion des bâtiments, la surveillance de la fréquentation d’espaces publics, ou encore l’optimisation des espaces de travail.
