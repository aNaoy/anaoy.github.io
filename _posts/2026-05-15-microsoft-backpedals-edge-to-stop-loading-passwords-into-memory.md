---
title: 'Microsoft backpedals: Edge to stop loading passwords into memory'
date: 2026-05-15
permalink: /posts/2026/05/15/microsoft-backpedals-edge-to-stop-loading-passwords-into-memory/
tags:
- veille-cyber
- bleepingcomp
---
### Microsoft renforce la sécurité des mots de passe dans Edge

Microsoft a annoncé une mise à jour corrective pour le navigateur Edge afin de corriger une vulnérabilité liée au stockage des mots de passe en mémoire. Initialement classé comme un comportement « par conception » par l'éditeur, ce mécanisme permettait de déchiffrer et de charger l'ensemble des identifiants en texte clair dès le lancement du navigateur.

**Points clés :**
* **Découverte :** Le chercheur en sécurité Tom Jøran Sønstebyseter Rønning a démontré qu'Edge maintenait les mots de passe déchiffrés en mémoire vive en permanence, contrairement aux autres navigateurs basés sur Chromium.
* **Vecteur d'attaque :** Un attaquant disposant de privilèges d'administrateur sur la machine peut extraire ces identifiants directement depuis la mémoire du processus. Un outil de démonstration (PoC) a été publié pour illustrer cette vulnérabilité.
* **Réponse de Microsoft :** Sous la pression et dans le cadre de sa « Secure Future Initiative », Microsoft a revu sa position et déploie une mesure de défense en profondeur pour empêcher ce chargement systématique en mémoire.

**Vulnérabilité :**
* Aucune CVE n'a été attribuée à ce jour, Microsoft ayant initialement nié le caractère critique de ce comportement.

**Recommandations :**
* **Mise à jour :** Les utilisateurs et administrateurs doivent s'assurer que leur navigateur Edge est mis à jour vers la version 148 ou supérieure.
* **Sécurité système :** Étant donné que l'attaque nécessite des droits d'administrateur, il est crucial de restreindre les privilèges des utilisateurs sur les postes de travail et de maintenir une politique de moindre privilège pour limiter l'impact en cas de compromission locale.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-edge-to-stop-loading-cleartext-passwords-in-memory-on-startup/){:target="_blank"}
