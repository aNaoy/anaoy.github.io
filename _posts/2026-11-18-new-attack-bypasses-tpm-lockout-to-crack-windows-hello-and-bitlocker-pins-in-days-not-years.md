---
title: 'New Attack Bypasses TPM Lockout to Crack Windows Hello and BitLocker PINs in Days, Not Years'
date: 2026-11-18
permalink: /posts/2026/11/18/new-attack-bypasses-tpm-lockout-to-crack-windows-hello-and-bitlocker-pins-in-days-not-years/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité majeure du TPM : Contournement du verrouillage pour le craquage des PIN

Des chercheurs de l'Université technique de Berlin ont mis en évidence une méthode permettant de contourner le verrouillage du module de plateforme sécurisée (TPM) sur de nombreux PC AMD et Intel. Cette faille permet de réaliser des attaques par force brute sur les codes PIN Windows Hello et BitLocker en quelques jours, au lieu de plusieurs années.

**Points clés :**
* **Principe de l'attaque :** La vulnérabilité exploite le fait que le TPM firmware stocke l'état du compteur de tentatives erronées sur la puce flash de la carte mère. En manipulant ou en réinitialisant cet état via un accès physique (ajout d'une carte intermédiaire ou injection de fautes de tension), les attaquants peuvent réinitialiser le compteur de tentatives, rendant la protection contre le blocage inopérante.
* **Impact :** Un PIN à 4 chiffres, normalement protégé par des délais de verrouillage, peut être cassé en environ 40 heures sur certains systèmes AMD. Un PIN à 6 chiffres pour BitLocker peut être compromis en 20 jours.
* **Vulnérabilités identifiées :**
    * **CVE-2026-43613 :** Faille dans le firmware des processeurs AMD liée à la gestion des compteurs RPMC (Replay Protected Memory Block).
    * **Faiblesse matérielle :** Les puces flash Winbond utilisées par certains constructeurs sont vulnérables à des attaques par "glitch" de tension, permettant d'extraire la clé secrète de signature, indépendamment du processeur.

**Recommandations :**
1. **Augmenter la complexité des PIN :** La mesure la plus efficace consiste à allonger les PIN (8 chiffres minimum recommandés). L'utilisation de PIN complexes (lettres et symboles) via l'option "Autoriser les PIN améliorés" pour BitLocker est fortement conseillée.
2. **Gestion des politiques :**
    * Pour **Windows Hello for Business**, configurer la stratégie "Longueur minimale du PIN" (via les modèles d'administration) pour imposer une longueur supérieure à 6 caractères.
    * Pour **BitLocker**, configurer la stratégie "Configurer la longueur minimale du PIN de démarrage".
3. **Mises à jour firmware :** Appliquer les mises à jour du firmware fournies par le constructeur du processeur (particulièrement pour AMD, avec des déploiements prévus entre fin 2024 et début 2027).
4. **Protection physique :** Étant donné que l'attaque nécessite un accès physique à la carte mère, limiter l'exposition des machines dans des environnements non sécurisés et surveiller toute trace d'altération du boîtier.

---
[Source](https://thehackernews.com/2026/11/flash-chip-attack-bypasses-tpm-lockout.html){:target="_blank"}
