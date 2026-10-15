---
title: 'ThreatsDay: Adobe RCE, DNS Wallet Theft, NVIDIA Container Escape, Self-Healing Backdoor + 23 More'
date: 2026-10-15
permalink: /posts/2026/10/15/threatsday-adobe-rce-dns-wallet-theft-nvidia-container-escape-self-healing-backdoor-23-more/
tags:
- veille-cyber
- hackernews
---
### Panorama des menaces cyber : Vulnérabilités critiques et vecteurs d'attaque

Cette semaine a été marquée par une recrudescence d'attaques utilisant des techniques variées, allant de l'exploitation de failles critiques de type RCE (exécution de code à distance) au vol de cryptomonnaies par DNS, en passant par des menaces persistantes et le ciblage des outils d'IA.

#### Points clés
*   **Ciblage des outils d'IA :** Les infosteleurs (comme *Aoki* et *Warden*) se concentrent désormais sur le vol des identifiants et jetons d'API liés aux assistants de codage IA, permettant aux attaquants d'usurper l'identité des développeurs et d'accéder à des pipelines CI/CD.
*   **Escalade de la cyberguerre :** La Russie intensifie ses opérations asymétriques en Europe via des tactiques psychologiques et cyber pour dégrader les infrastructures critiques sans conflit cinétique direct.
*   **Persistance malveillante :** Des malwares, comme les backdoors WordPress, intègrent des mécanismes "auto-réparateurs" et utilisent des smart contracts blockchain (EtherHiding) pour masquer leurs serveurs de commande (C2).
*   **Protection Android :** Google renforce la lutte contre les arnaques bancaires par téléphone grâce à une vérification en temps réel des appels entrants.

#### Vulnérabilités majeures
*   **CVE-2026-0257 (PAN-OS GlobalProtect) :** Contournement d'authentification activement exploité par les groupes *Qilin* et *Settra*.
*   **CVE-2026-47595 (NVIDIA GPU Driver) :** Vulnérabilité "Bad UVM" permettant une élévation de privilèges (LPE) jusqu'au niveau root et une évasion de conteneur.
*   **CVE-2026-110392 (Samsung QA-Board) :** RCE non authentifiée (Score CVSS 9.8) due à une injection de commande shell.
*   **CVE-2026-108065 (Channel Software WebAlliance) :** Injection SQL critique permettant la lecture de données sensibles ou l'exécution de commandes système.
*   **GHSA-2phj-cp9f-qq6w (Harbor) :** Faille SSRF permettant à un utilisateur enregistré de voler des identifiants IAM.
*   **CVE-2026-79610 (Xen) :** Condition de course dans le mécanisme de table de subvention permettant une évasion de VM vers l'hôte.

#### Recommandations
1.  **Correctifs et inventaire :** Appliquez immédiatement les patchs pour les vulnérabilités critiques citées. Pour PAN-OS, la simple mise à jour ne suffit pas : révoquez les sessions actives et inspectez les connexions suspectes.
2.  **Sécurisation des outils IA :** Appliquez le principe du moindre privilège aux clés d'API et jetons d'accès utilisés dans les environnements de développement et outils d'IA.
3.  **Gestion de la PKI :** Commencez dès maintenant l'inventaire des dépendances liées aux certificats pour préparer la transition vers l'authentification post-quantique.
4.  **Défense contre les accès :** Désactivez les cookies de contournement d'authentification sur les VPN si non requis et renforcez la surveillance des comptes administrateurs sur les sites WordPress.
5.  **Atténuation Xen :** Pour le risque d'évasion VM, utilisez l'option de configuration `max_grant_version=1` si la mise à jour n'est pas immédiate.

---
[Source](https://thehackernews.com/2026/10/threatsday-adobe-rce-dns-wallet-theft.html){:target="_blank"}
