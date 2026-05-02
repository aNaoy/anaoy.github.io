---
title: 'Malicious Ad for Homebrew Leads to MacSync Stealer, (Fri, May 1st)'
date: 2026-05-02
permalink: /posts/2026/05/02/malicious-ad-for-homebrew-leads-to-macsync-stealer-fri-may-1st/
tags:
- veille-cyber
- sans-isc
---
### Propagation du logiciel malveillant MacSync via une campagne publicitaire malveillante

Une campagne active cible les utilisateurs de macOS en utilisant des publicités frauduleuses dans les résultats de recherche. Ces publicités redirigent les victimes vers une fausse page se faisant passer pour **Homebrew** (gestionnaire de paquets populaire), incitant les utilisateurs à copier et exécuter un script malveillant dans leur terminal.

**Points clés :**
* **Vecteur d'attaque :** Publicités malveillantes (malvertising) dans les moteurs de recherche.
* **Méthode d'infection :** L'utilisateur est invité à copier un script dans le terminal. L'exécution de ce script déclenche des fenêtres contextuelles (pop-ups) sollicitant le mot de passe de l'utilisateur et des autorisations d'accès système (notamment pour l'application Finder).
* **Charge utile :** Le "MacSync Stealer" collecte des informations sensibles sur la machine, les compresse dans un fichier nommé `/tmp/osalogging.zip` et les transmet à un serveur de commande et de contrôle (C2).
* **Persistance :** L'utilisation de scripts `zsh` permet d'automatiser l'exfiltration des données.

**Vulnérabilités :**
* Il ne s'agit pas d'une vulnérabilité logicielle (CVE) spécifique, mais d'une exploitation de l'**ingénierie sociale** et de la confiance des utilisateurs envers les outils en ligne de commande. Le système est compromis par l'octroi volontaire de privilèges administratifs par l'utilisateur.

**Recommandations :**
* **Vérification des sources :** Téléchargez uniquement des logiciels à partir des sites officiels et vérifiez toujours l'URL dans la barre d'adresse avant toute interaction.
* **Méfiance vis-à-vis des commandes :** Ne copiez et ne collez jamais de scripts provenant de sources non fiables directement dans un terminal système.
* **Gestion des privilèges :** Soyez extrêmement prudent lors de l'octroi d'autorisations d'accès au système ou de saisie de mot de passe administrateur après l'exécution de scripts inconnus.
* **Surveillance réseau :** Surveillez les communications suspectes vers des domaines non identifiés, particulièrement après l'exécution de commandes système inhabituelles.

---
[Source](https://isc.sans.edu/diary/rss/32942){:target="_blank"}
