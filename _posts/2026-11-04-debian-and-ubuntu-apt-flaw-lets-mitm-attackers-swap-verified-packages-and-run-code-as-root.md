---
title: 'Debian and Ubuntu APT Flaw Lets MitM Attackers Swap Verified Packages and Run Code as Root'
date: 2026-11-04
permalink: /posts/2026/11/04/debian-and-ubuntu-apt-flaw-lets-mitm-attackers-swap-verified-packages-and-run-code-as-root/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique dans APT : Exécution de code à distance sur Debian et Ubuntu

Une faille de sécurité critique affecte le gestionnaire de paquets APT sur les systèmes Debian et Ubuntu. Elle permet à un attaquant positionné en "Man-in-the-Middle" (MitM) d'intercepter et de remplacer des paquets légitimes par des paquets malveillants, conduisant à une exécution de code avec les privilèges root.

**Points clés :**
*   **Mécanisme d'attaque :** La vulnérabilité exploite le comportement de réessai automatique des téléchargements (`Acquire::Retries`) activé par défaut depuis Debian 12 et Ubuntu 22.04. L'attaquant utilise des redirections HTTP et des erreurs serveur simulées pour forcer APT à télécharger une version falsifiée du paquet.
*   **Portée :** La faille concerne les versions modernes de Debian et Ubuntu, mais peut également impacter des versions plus anciennes (Debian 11, Ubuntu 20.04) si l'option de réessai automatique a été activée manuellement par l'utilisateur.
*   **Gravité :** Évaluée comme prioritaire avec un score CVSS 4.0 de 7.7.

**Vulnérabilité :**
*   **CVE-2026-109518**

**Recommandations :**
*   **Appliquer les correctifs :** Mettre à jour immédiatement le paquet APT vers les versions corrigées fournies par les dépôts officiels de Debian et Ubuntu.
*   **Vérifier les configurations :** S'assurer que le paramètre `Acquire::Retries` est désactivé si la mise à jour immédiate n'est pas possible sur les systèmes legacy.
*   **Sécuriser les connexions :** Privilégier l'utilisation de sources de paquets chiffrées (HTTPS) bien que le risque lié à cette faille spécifique nécessite une analyse complémentaire sur le transport.

---
[Source](https://thehackernews.com/2026/11/debian-and-ubuntu-apt-flaw-lets-mitm.html){:target="_blank"}
