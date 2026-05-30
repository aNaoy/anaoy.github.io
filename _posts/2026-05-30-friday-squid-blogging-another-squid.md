---
title: 'Friday Squid Blogging: Another Squid'
date: 2026-05-30
permalink: /posts/2026/05/30/friday-squid-blogging-another-squid/
tags:
- veille-cyber
- schneier
---
### Veille de sécurité : Persistance et compromission au niveau du BIOS

Cet article de blog sert de plateforme ouverte à la communauté pour discuter de l'actualité de la cybersécurité. Un commentaire spécifique attire l'attention sur des menaces persistantes avancées ciblant les couches matérielles.

**Points clés :**
*   **Menaces sur le firmware :** Mise en évidence de l'existence de rootkits au niveau du BIOS/UEFI, permettant une persistance invisible au système d'exploitation.
*   **Surveillance totale :** Utilisation de techniques de compromission via machine virtuelle (VM) pour intercepter les entrées clavier (keylogging) en temps réel, rendant les mesures de sécurité logicielles classiques inefficaces.

**Vulnérabilités :**
*   Le commentaire mentionne des **Rootkits BIOS sur machines virtuelles**. Aucune CVE spécifique n'est citée dans le texte, mais ces vecteurs d'attaque exploitent généralement des failles dans le processus de démarrage sécurisé (Secure Boot) ou des vulnérabilités de privilèges dans l'hyperviseur.

**Recommandations :**
*   **Vérification de l'intégrité :** Utiliser des outils de contrôle d'intégrité du firmware (ex: CHIPSEC) pour détecter des modifications non autorisées du BIOS/UEFI.
*   **Sécurisation matérielle :** Privilégier l'utilisation de modules de plateforme sécurisée (TPM) et s'assurer que le *Secure Boot* est correctement configuré et verrouillé.
*   **Monitoring comportemental :** Étant donné que ces rootkits opèrent en amont du système d'exploitation, la détection doit se concentrer sur l'analyse réseau (flux anormaux) plutôt que sur les outils antivirus traditionnels.

---
[Source](https://www.schneier.com/blog/archives/2026/05/friday-squid-blogging-another-squid.html){:target="_blank"}
