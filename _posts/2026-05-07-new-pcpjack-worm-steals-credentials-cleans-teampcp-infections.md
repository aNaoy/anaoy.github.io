---
title: 'New PCPJack worm steals credentials, cleans TeamPCP infections'
date: 2026-05-07
permalink: /posts/2026/05/07/new-pcpjack-worm-steals-credentials-cleans-teampcp-infections/
tags:
- veille-cyber
- bleepingcomp
---
### PCPJack : Un nouveau ver ciblant les infrastructures Cloud

PCPJack est un framework malveillant sophistiqué conçu pour le vol massif d'identifiants au sein d'environnements Cloud (Docker, Kubernetes, bases de données, etc.). Le malware se distingue par sa capacité à évincer le groupe TeamPCP en supprimant activement ses outils, processus et accès sur les systèmes compromis.

**Points clés :**
*   **Propagation :** Le ver scanne les infrastructures exposées et utilise les données de *Common Crawl* pour identifier de nouvelles cibles.
*   **Fonctionnement :** Une fois déployé via un script `bootstrap.sh`, il installe des dépendances Python, assure sa persistance (systemd, cron, conteneurs privilégiés) et exécute des modules de vol d'identifiants (clés SSH, tokens Slack, accès OpenAI, etc.).
*   **Exfiltration :** Les données volées sont chiffrées (AES/ChaCha20-Poly1305) et envoyées vers des canaux Telegram.
*   **Origine supposée :** Les chercheurs soupçonnent qu'il s'agit d'un ancien membre ou affilié du groupe TeamPCP, connaissant parfaitement leurs méthodes et leur infrastructure.

**Vulnérabilités exploitées :**
*   **CVE-2025-29927 :** Contournement d'authentification dans le middleware Next.js.
*   **CVE-2025-55182 (React2Shell) :** Faille de désérialisation dans React/Next.js.
*   **CVE-2026-1357 :** Téléchargement de fichiers non authentifié dans WPVivid Backup.
*   **CVE-2025-9501 :** Injection PHP dans W3 Total Cache.
*   **CVE-2025-48703 :** Injection de commandes shell dans CentOS Web Panel.

**Recommandations de sécurité :**
*   **Durcissement des accès :** Imposer l'authentification multifacteur (MFA) partout où cela est possible.
*   **Configuration Cloud :** Utiliser IMDSv2 sur AWS pour sécuriser l'accès aux métadonnées des instances.
*   **Sécurisation des services :** Garantir une authentification forte pour les API Docker et Kubernetes.
*   **Principe du moindre privilège :** Restreindre les droits des conteneurs et des services exécutés.
*   **Gestion des secrets :** Ne jamais stocker de secrets (clés API, mots de passe) en texte clair.

---
[Source](https://www.bleepingcomputer.com/news/security/new-pcpjack-worm-steals-credentials-cleans-teampcp-infections/){:target="_blank"}
