Ce projet est réalisé dans le cadre du module Communication Sans Fil en Licence 1 à l’Université
Nice Sophia Antipolis.

# Lien vers le slide

**----->** [Slide de la présentation du projet](peoplecounter/PEOPLECOUNTER.pdf)
# 🧮 PeopleCounter – Compteur de personnes avec boutons poussoirs

**PeopleCounter** est un système simple et interactif conçu pour comptabiliser en temps réel le nombre de personnes **entrant** et **sortant** d'une pièce.  
Contrairement à la version initiale utilisant des capteurs PIR, cette version repose sur **deux boutons poussoirs** pour une détection manuelle et contrôlée.

---

## ⚙️ Matériel utilisé

- 1x Carte Arduino (Uno, Nano, ESP32, etc.)
- 2x **Boutons poussoirs**
  - **Gauche** : pour signaler une **entrée**
  - **Droite** : pour signaler une **sortie**
- 1x Module **LoRa 868 MHz**
- Câblage / Breadboard

---

## 🧠 Fonctionnement

- Lorsqu'on **appuie sur le bouton gauche**, le compteur de personnes est **incrémenté**.
- Lorsqu'on **appuie sur le bouton droit**, le compteur est **décrémenté**.
- Un **délai de 300 ms** est appliqué après chaque appui pour éviter les rebonds mécaniques.
- Le nombre total de personnes est **envoyé par LoRa** à une unité distante.

---


## ✅ Avantages du projet

- 🧩 Simplicité d’utilisation
- 📡 Transmission sans fil longue portée
- 🛠️ Facile à fabriquer et à personnaliser
- 👨‍🏫 Idéal pour l’apprentissage Arduino / LoRa / prototypage
- 🏢 Applicable à la gestion d'espaces physiques (bureaux, salles, événements)

---

## 🚀 Possibilités d’amélioration

- Ajout d’un **écran OLED** pour afficher le compteur en temps réel
- Intégration dans un **système de gestion de bâtiment**
- Envoi de **notifications** ou journalisation des données

---



