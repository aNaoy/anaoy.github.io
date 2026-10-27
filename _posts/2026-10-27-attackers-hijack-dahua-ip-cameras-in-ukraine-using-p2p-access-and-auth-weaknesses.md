---
title: 'Attackers Hijack Dahua IP Cameras in Ukraine Using P2P Access and Auth Weaknesses'
date: 2026-10-27
permalink: /posts/2026/10/27/attackers-hijack-dahua-ip-cameras-in-ukraine-using-p2p-access-and-auth-weaknesses/
tags:
- veille-cyber
- hackernews
---
### Compromission massive des caméras IP Dahua via le protocole P2P

Le CERT-UA a alerté sur une campagne de piratage visant les systèmes de vidéosurveillance Dahua en Ukraine. Les attaquants exploitent les faiblesses du service P2P (Easy4IP) et des vulnérabilités logicielles pour prendre le contrôle total des appareils, modifier leurs configurations et installer des accès persistants.

**Points clés :**
*   **Vecteur principal :** Utilisation de la plateforme P2P Easy4IP, accessible via le numéro de série de l'appareil. La structure prévisible de ces numéros permet aux attaquants de scanner et d'identifier des cibles à grande échelle.
*   **Techniques d'intrusion :** Attaques par force brute sur les mots de passe et exploitation de failles d'authentification sur des firmwares obsolètes.
*   **Persistance :** Installation de comptes dérobés (backdoors) survivant aux réinitialisations d'usine sur certains modèles.
*   **Objectifs :** Espionnage systématique pour collecter des renseignements militaires (mouvements de troupes, transports de matériel) afin de cibler des infrastructures et du personnel.

**Vulnérabilités exploitées :**
*   **CVE-2021-33044 & CVE-2021-33045 :** Contournement d'authentification sur les produits Dahua permettant une connexion sans mot de passe.
*   Autres failles couramment utilisées dans des campagnes similaires : CVE-2017-7921 (Hikvision), CVE-2020-25078 (D-Link), CVE-2020-25169 (Reolink), CVE-2021-36260 (Hikvision), CVE-2024-53375 & CVE-2024-57049 (TP-Link/MikroTik).

**Recommandations :**
*   **Désactiver la fonctionnalité P2P** si elle n'est pas strictement nécessaire au fonctionnement.
*   **Restreindre l'exposition :** Ne jamais exposer directement les caméras ou les enregistreurs (NVR/DVR) sur Internet ; privilégier l'accès via un VPN.
*   **Mise à jour :** Installer les derniers correctifs de firmware fournis par le constructeur.
*   **Audit de sécurité :** Vérifier régulièrement les journaux d'audit pour détecter des connexions suspectes via le protocole `DVRIP` ou la présence de comptes administrateurs non autorisés.

---
[Source](https://thehackernews.com/2026/10/attackers-hijack-dahua-ip-cameras-in.html){:target="_blank"}
