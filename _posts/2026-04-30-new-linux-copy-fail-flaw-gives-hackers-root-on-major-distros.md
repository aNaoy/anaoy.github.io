---
title: 'New Linux ‘Copy Fail’ flaw gives hackers root on major distros'
date: 2026-04-30
permalink: /posts/2026/04/30/new-linux-copy-fail-flaw-gives-hackers-root-on-major-distros/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilité "Copy Fail" : Escalade de privilèges critique sur Linux

Une faille de sécurité majeure, baptisée « Copy Fail », permet à un utilisateur local non privilégié d'obtenir les droits d'administration (root) sur la quasi-totalité des distributions Linux publiées depuis 2017.

**Points clés :**
*   **Origine :** Découverte par la société Theori via une plateforme de pentesting basée sur l'IA, la faille exploite un bug logique dans le sous-système cryptographique du noyau Linux.
*   **Mécanisme :** En combinant l'interface `AF_ALG` (accès aux fonctions cryptographiques) et l'appel système `splice()`, un attaquant peut écrire 4 octets dans le cache de page d'un fichier. En ciblant un binaire `setuid-root`, cette modification altère son exécution pour élever les privilèges.
*   **Portabilité :** Contrairement à d'autres vulnérabilités similaires (comme "Dirty Pipe"), l'exploit est extrêmement stable (taux de réussite de 100 %) et ne nécessite aucune adaptation spécifique par distribution.

**Vulnérabilité identifiée :**
*   **CVE-2026-31431 :** Bug logique dans le modèle cryptographique `authencesn` du noyau Linux, introduit en 2017 par une optimisation "in-place".

**Recommandations :**
*   **Mise à jour :** Appliquer les correctifs du noyau dès qu'ils sont disponibles (présents dans les versions 6.18.22, 6.19.12 et 7.0).
*   **Atténuation immédiate :** Pour les systèmes non patchés, désactiver le module vulnérable `algif_aead` pour bloquer la création de sockets `AF_ALG` :
    1. Créer le fichier de configuration : `echo "install algif_aead /bin/false" > /etc/modprobe.d/disable-algif.conf`
    2. Décharger le module : `rmmod algif_aead`
*   **Priorisation :** Les environnements multi-utilisateurs (serveurs cloud, clusters Kubernetes, environnements CI/CD) doivent être mis à jour en priorité.

---
[Source](https://www.bleepingcomputer.com/news/security/new-linux-copy-fail-flaw-gives-hackers-root-on-major-distros/){:target="_blank"}
