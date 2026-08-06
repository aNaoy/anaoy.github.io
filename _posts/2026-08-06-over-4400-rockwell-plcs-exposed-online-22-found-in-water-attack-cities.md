---
title: 'Over 4,400 Rockwell PLCs Exposed Online, 22 Found in Water Attack Cities'
date: 2026-08-06
permalink: /posts/2026/08/06/over-4400-rockwell-plcs-exposed-online-22-found-in-water-attack-cities/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques des automates Rockwell dans le secteur de l'eau

Des recherches récentes ont mis en lumière l'exposition critique de milliers d'automates programmables industriels (PLC) Rockwell Automation sur Internet. Cette vulnérabilité infrastructurelle a été exploitée dans le cadre de cyberattaques ciblant des services publics de distribution d'eau aux États-Unis.

**Points clés :**
* **Exposition mondiale :** Plus de 4 400 contrôleurs Rockwell sont accessibles directement via Internet, dont une majorité via des réseaux cellulaires mobiles.
* **Méthode d'attaque :** Les attaquants ne nécessitent pas nécessairement l'exploitation d'une faille logicielle. L'accès direct via le port 44818 (EtherNet/IP) permet de modifier les configurations, de définir de nouveaux mots de passe et de prendre le contrôle des équipements.
* **Impact opérationnel :** Les incidents signalés ont conduit à une perte de visibilité et de contrôle sur les infrastructures critiques, avec des modifications non autorisées du code logique (ladder logic).

**Vulnérabilités identifiées :**
* **CVE-2017-16740 :** Un dépassement de tampon (buffer overflow) dans le protocole Modbus TCP affectant les séries MicroLogix 1400. Bien que corrigée, elle reste présente sur de nombreux appareils non mis à jour.
* **Exposition native :** L'utilisation du port 44818 sans authentification robuste constitue la faille primaire, facilitant l'identification et la manipulation des appareils.

**Recommandations de sécurité :**
* **Déconnexion immédiate :** Retirer impérativement tous les PLC de l'Internet public.
* **Sécurisation des accès :** Isoler l'accès distant via des réseaux privés (APN), des VPN ou des architectures sécurisées.
* **Mise à jour :** Appliquer les correctifs de firmware pour les appareils vulnérables (ex: passer à la version 21.003 ou supérieure pour les MicroLogix 1400).
* **Gestion des accès :** Implémenter une authentification forte sur les modems cellulaires et maintenir des sauvegardes hors ligne de la logique des contrôleurs pour permettre une récupération rapide en cas de compromission (réinitialisation aux paramètres d'usine).
* **Obsolescence :** Pour les modèles abandonnés (comme le MicroLogix 1100), une stratégie de remplacement par des équipements plus récents est préconisée.

---
[Source](https://thehackernews.com/2026/08/over-4400-rockwell-plcs-exposed-online.html){:target="_blank"}
