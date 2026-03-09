# Arduino Security Alarm System 🔐

Un système de **sécurité et d’alarme basé sur Arduino** permettant de détecter les intrusions à l’aide d’un capteur de mouvement PIR et de déclencher une alarme sonore.
Le système utilise également un **clavier numérique pour saisir un mot de passe** et un **écran LCD pour afficher les informations du système**.

Ce projet peut être utilisé pour sécuriser :

* une maison
* un bureau
* un laboratoire
* tout espace nécessitant une surveillance

Le système repose sur une **carte Arduino Uno comme contrôleur principal**. 

---

# 📷 Aperçu du système

Le système comprend les composants suivants :

* Arduino Uno
* Capteur de mouvement PIR
* Écran LCD 16x2
* Clavier numérique 4x4
* Buzzer
* Breadboard et câbles

Lorsque le capteur PIR détecte un mouvement, le buzzer déclenche une **alarme sonore** et l’utilisateur doit entrer le **mot de passe correct** pour désactiver le système.

---

# ⚙️ Fonctionnalités

✔ Activation de l’alarme avec le clavier
✔ Détection de mouvement avec capteur PIR
✔ Déclenchement d’une alarme sonore
✔ Désactivation avec mot de passe
✔ Possibilité de **changer le mot de passe**
✔ Affichage des informations sur écran LCD

---

# 🔧 Matériel utilisé

| Composant   | Description               |
| ----------- | ------------------------- |
| Arduino Uno | Microcontrôleur principal |
| PIR Sensor  | Détection de mouvement    |
| LCD 16x2    | Affichage des messages    |
| Keypad 4x4  | Entrée du mot de passe    |
| Buzzer      | Alarme sonore             |
| Breadboard  | Montage du circuit        |

---

# 🧠 Principe de fonctionnement

1️⃣ L’utilisateur active l’alarme via le clavier.
2️⃣ Un **compte à rebours de 3 secondes** démarre.
3️⃣ Le capteur PIR surveille les mouvements.
4️⃣ Si un mouvement est détecté :

* le buzzer se déclenche
* le LCD affiche un message d’alerte

5️⃣ L’utilisateur doit entrer le **mot de passe correct** pour arrêter l’alarme.

---

# 🖥️ Installation

1️⃣ Installer **Arduino IDE**

https://www.arduino.cc/en/software

2️⃣ Installer les bibliothèques nécessaires :

* `LiquidCrystal`
* `Keypad`

3️⃣ Connecter l’Arduino à l’ordinateur.

4️⃣ Téléverser le code dans la carte Arduino.

---

# 🔌 Connexion des composants

### PIR Sensor

| PIR | Arduino |
| --- | ------- |
| VCC | 5V      |
| GND | GND     |
| OUT | Pin 10  |

### Buzzer

| Buzzer | Arduino |
| ------ | ------- |
| +      | Pin 11  |
| -      | GND     |

### LCD

| LCD | Arduino |
| --- | ------- |
| RS  | A0      |
| E   | A1      |
| D4  | A2      |
| D5  | A3      |
| D6  | A4      |
| D7  | A5      |

### Keypad

| Keypad | Arduino |
| ------ | ------- |
| Rows   | 9,8,7,6 |
| Cols   | 5,4,3,2 |

---

# 💻 Code

Le programme est écrit en **C++ pour Arduino** et utilise les bibliothèques :

```
LiquidCrystal
Keypad
```

Le code principal gère :

* la détection PIR
* la gestion du mot de passe
* l’activation de l’alarme
* l’affichage sur LCD

---

# 🚀 Améliorations possibles

* envoyer une notification SMS
* connecter le système à Internet (IoT)
* ajouter une caméra
* ajouter une application mobile
* ajouter un module GSM

---

# 🎓 Objectif du projet

Ce projet a été développé pour apprendre :

* les **systèmes embarqués**
* la **programmation Arduino**
* la **sécurité électronique**
* l’intégration de capteurs et actionneurs

---

# 👨‍💻 Auteur

Nom : AHMED EL YAMINI
Projet : Arduino Security Alarm System
Année : 2026
