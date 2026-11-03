---
title: 'Red Hat Patches 9.8-Rated Linux TCP RCE Flaw While Ubuntu Releases Fixes for Testing'
date: 2026-11-03
permalink: /posts/2026/11/03/red-hat-patches-98-rated-linux-tcp-rce-flaw-while-ubuntu-releases-fixes-for-testing/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité Critique du Noyau Linux : RCE via TCP IPv4

Une faille critique de type « use-after-free » dans le code TCP IPv4 du noyau Linux permet à un attaquant distant non authentifié d'exécuter du code arbitraire (RCE). Cette vulnérabilité, présente depuis la version 4.4 du noyau, survient lors du traitement des options IP lorsqu'une requête de connexion est retransmise.

**Points clés :**
*   **Identifiant :** CVE-2026-98432.
*   **Gravité :** Score CVSS de 9.8 (Critique).
*   **Mécanisme :** Une course (race condition) lors de la gestion des options IP (Record Route ou Timestamp) permet de manipuler une mémoire déjà libérée.
*   **Statut d'exploitation :** Aucune attaque active signalée à ce jour. Cependant, un exploit conceptuel a été démontré par une IA d'Anthropic, et des outils de preuve de concept circulent sur GitHub.
*   **Disponibilité des correctifs :** Red Hat a déjà déployé des correctifs pour RHEL 8, 9 et 10. Ubuntu propose des correctifs via son canal de test « -proposed ». Debian, Oracle Linux, SUSE et Amazon Linux ont déjà corrigé la faille.

**Recommandations :**
1.  **Mise à jour :** Appliquer les correctifs du noyau dès qu'ils sont disponibles dans les canaux de distribution officiels. Un redémarrage du système est nécessaire après l'installation.
2.  **Utilisateurs Ubuntu :** Si le correctif n'est pas encore dans le flux régulier, les administrateurs peuvent utiliser le dépôt `-proposed` pour installer le noyau corrigé, bien que cela soit une procédure de test.
3.  **Atténuation temporaire :** Red Hat propose une règle `nftables` pour bloquer les paquets IPv4 TCP contenant des options IP (`ip protocol tcp ip hdrlength > 5`). Cette mesure est toutefois partielle, peut impacter certaines applications légitimes et ne protège pas contre le trafic entre conteneurs sur une même machine.
4.  **Vérification :** Utiliser la commande `uname -r` et comparer le résultat avec les versions de noyaux corrigés fournies par les éditeurs pour s'assurer que le système est protégé.

---
[Source](https://thehackernews.com/2026/11/red-hat-patches-98-rated-linux-tcp-rce.html){:target="_blank"}
