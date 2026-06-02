---
title: 'Instagram users locked out after Meta AI abused to steal accounts'
date: 2026-06-02
permalink: /posts/2026/06/02/instagram-users-locked-out-after-meta-ai-abused-to-steal-accounts/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilité des outils de support automatisés d'Instagram

Des attaquants exploitent les outils de support automatisés de Meta pour pirater des comptes Instagram à forte valeur ajoutée, en contournant les mécanismes de sécurité, y compris l'authentification à deux facteurs (2FA). 

**Points clés :**
* **Méthode d'attaque :** Les pirates imitent les propriétaires légitimes en manipulant les outils d'assistance par IA. Ils utilisent des outils de génération vidéo par IA pour créer des « selfies animés » à partir de photos publiques, trompant ainsi le processus de vérification faciale de Meta.
* **Contournement de sécurité :** L'utilisation de VPN permet de simuler la géolocalisation habituelle de la victime, évitant les alertes de sécurité. Une fois l'adresse e-mail associée au compte modifiée via l'IA, le pirate réinitialise le mot de passe et prend le contrôle total du compte.
* **Absence de support humain :** Les victimes se retrouvent bloquées dans des boucles de chatbots inefficaces, sans possibilité d'escalader le problème vers un agent humain, rendant la récupération des comptes extrêmement difficile.

**Vulnérabilités :**
* Absence de CVE spécifique identifiée, il s'agit d'une vulnérabilité logique liée à la **faiblesse des protocoles de vérification d'identité biométrique par IA** (incapacité à distinguer une vidéo générée par IA d'une capture réelle).
* Défaut de conception dans le workflow de récupération de compte automatisé permettant une modification d'identifiants sans supervision humaine.

**Recommandations :**
* **Renforcement de la vérification :** Meta doit impérativement intégrer une vérification humaine pour les processus de récupération de comptes sensibles ou à forte valeur.
* **Amélioration de la détection IA :** Implémenter des outils de détection de "deepfake" plus robustes pour valider les selfies de vérification.
* **Vigilance utilisateur :** Bien que l'attaque soit côté plateforme, les utilisateurs sont invités à limiter la publication de photos haute résolution en ligne, car celles-ci servent de base aux générateurs de vidéos utilisés par les attaquants pour usurper leur identité.

---
[Source](https://www.bleepingcomputer.com/news/security/instagram-users-locked-out-after-meta-ai-abused-to-steal-accounts/){:target="_blank"}
