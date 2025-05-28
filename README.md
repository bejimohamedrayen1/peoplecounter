Ce projet est réalisé dans le cadre du module Communication Sans Fil en Licence 1 à l’Université
Nice Sophia Antipolis.

# Lien vers le slide

**----->** [Slide de la présentation du projet](peoplecounter/PEOPLECOUNTER.pdf)
PeopleCounter – Compteur de personnes avec boutons poussoirs
Le projet PeopleCounter est un système simple et interactif conçu pour comptabiliser en temps réel le nombre de personnes entrant et sortant d'une pièce. Contrairement à la version initiale utilisant des capteurs PIR (détection de mouvement), ce projet repose désormais sur deux boutons poussoirs pour une détection manuelle et contrôlée.

Le système est basé sur une plateforme Arduino. Il utilise deux boutons :

Bouton gauche : utilisé lorsqu'une personne entre dans la pièce.

Bouton droit : utilisé lorsqu'une personne sort de la pièce.

Chaque appui sur l’un des boutons modifie le compteur de personnes :

L’appui sur le bouton gauche incrémente le compteur.

L’appui sur le bouton droit décrémente le compteur.

Ce fonctionnement permet une gestion fiable et maîtrisée du comptage, notamment dans des contextes où une détection automatique n’est pas nécessaire ou souhaitée.

Une fonctionnalité clé du système est la transmission sans fil des données à une unité distante via un module LoRa à 868 MHz. Cela permet d'envoyer régulièrement le nombre de personnes présentes dans la pièce à une plateforme externe, ce qui est particulièrement utile pour des applications de surveillance à distance.

Un délai de 300 ms est intégré après chaque appui pour éviter les doubles comptages liés aux rebonds mécaniques des boutons.

L’ensemble des composants est intégré dans un boîtier personnalisé imprimé en 3D, offrant une solution compacte, fonctionnelle et esthétique.

Points forts du projet :
Compteur de personnes manuel et fiable

Communication sans fil longue portée via LoRa

Conception simple et pédagogique

Boîtier imprimé en 3D pour un rendu propre

Idéal pour des projets éducatifs ou de prototypage rapide

Ce projet constitue une excellente introduction à l’Arduino, à la communication LoRa, à la gestion d’entrées utilisateur, et à la prototypage électronique. Il peut être adapté à divers contextes comme la gestion des accès dans des petites salles, des événements ou des espaces partagés.
