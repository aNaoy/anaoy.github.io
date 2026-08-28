---
title: 'Two Unitree G1 EDU Humanoid Robot Flaws Enable Root RCE, One Starts Over Bluetooth'
date: 2026-08-28
permalink: /posts/2026/08/28/two-unitree-g1-edu-humanoid-robot-flaws-enable-root-rce-one-starts-over-bluetooth/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques sur le robot humanoïde Unitree G1 EDU

Le chercheur en sécurité Olivier Laflamme a révélé deux chaînes d'exécution de code à distance (RCE) permettant d'obtenir les privilèges root sur le PC de locomotion du robot Unitree G1 EDU.

**Points clés :**
*   **Accès root :** Les deux failles permettent de prendre le contrôle total du système.
*   **Vecteurs d'attaque :** Une vulnérabilité est exploitable via le réseau local, tandis que l'autre peut être initiée via le Bluetooth Low Energy (BLE) à proximité.
*   **Failles Cloud :** Une lacune d'autorisation dans le service cloud de Unitree permettait à des comptes non propriétaires de récupérer les clés de chiffrement de robots tiers, facilitant ainsi l'exploitation via BLE. Bien que Unitree ait corrigé ce point spécifique, les vulnérabilités sous-jacentes sur le robot persistent.

**Vulnérabilités identifiées :**
*   **CVE-2026-76639 :** Exploite une condition de traversée de répertoire dans `chat_go` pour atteindre `bashrunner`, entraînant une RCE avec droits root.
*   **CVE-2026-76640 :** Chaîne d'attaque complexe utilisant une injection BLE sans appairage, suivie d'un dépassement de tampon (buffer overflow) lors de la configuration du Wi-Fi pour obtenir l'exécution de code root.

**Recommandations :**
*   **Mise à jour :** Bien qu'aucune version de firmware spécifique n'ait été officiellement confirmée comme correctrice par le constructeur, les propriétaires sont invités à surveiller les annonces de Unitree pour toute mise à jour de sécurité disponible.
*   **Sécurisation physique et réseau :** En attendant un correctif définitif, restreindre l'exposition du robot aux réseaux Wi-Fi non sécurisés et limiter la portée physique (Bluetooth) autour des unités.
*   **Veille :** Suivre les communications officielles de Unitree concernant la correction des vulnérabilités mentionnées.

---
[Source](https://thehackernews.com/2026/08/two-unitree-g1-edu-humanoid-robot-flaws.html){:target="_blank"}
