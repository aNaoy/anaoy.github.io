---
title: 'The Gentlemen ransomware now uses SystemBC for bot-powered attacks'
date: 2026-04-21
permalink: /posts/2026/04/21/the-gentlemen-ransomware-now-uses-systembc-for-bot-powered-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Escalade des attaques du ransomware Gentlemen via le botnet SystemBC

Le groupe de ransomware-as-a-service (RaaS) « Gentlemen », actif depuis mi-2025, renforce ses capacités opérationnelles en intégrant le malware proxy **SystemBC**. Des chercheurs de Check Point ont identifié un botnet lié à cette activité comptant plus de 1 570 hôtes, principalement des environnements corporatifs. Cette évolution marque une montée en gamme dans l'utilisation d'infrastructures de serveurs mandataires pour la diffusion furtive de charges utiles malveillantes.

**Points clés :**
*   **Mode opératoire :** Les attaquants obtiennent des privilèges d'administrateur de domaine, utilisent Cobalt Strike pour le mouvement latéral via RPC et exploitent les objets de stratégie de groupe (GPO) pour un chiffrement massif et simultané.
*   **Capacités techniques :** Le ransomware dispose de variantes pour Windows, Linux, NAS, BSD et ESXi (avec arrêt des VM avant chiffrement). Le processus de chiffrement utilise un schéma hybride (X25519 et XChaCha20).
*   **Persistance de SystemBC :** Malgré des opérations policières en 2024, SystemBC reste un outil privilégié pour le tunneling SOCKS5 et l'automatisation de la livraison de charges utiles.

**Vulnérabilités et vecteurs :**
*   Bien que le vecteur d'accès initial ne soit pas déterminé, les attaquants s'appuient sur l'usurpation d'identifiants (via **Mimikatz**) et l'exécution à distance sur des systèmes compromis. Aucune CVE spécifique n'est mentionnée, l'attaque reposant sur l'exploitation des outils d'administration système légitimes.

**Recommandations :**
*   **Surveillance réseau :** Détecter le trafic associé aux serveurs de commande et contrôle (C2) de SystemBC, souvent utilisé pour le tunneling SOCKS5.
*   **Sécurisation des identifiants :** Mettre en œuvre une protection rigoureuse contre le vol de jetons et d'identifiants (Credential Harvesting) et limiter les privilèges d'administration sur les contrôleurs de domaine.
*   **Détection :** Utiliser les règles YARA fournies par les chercheurs pour identifier les signatures du ransomware.
*   **Gestion des GPO :** Surveiller les modifications suspectes apportées aux politiques de groupe, souvent utilisées pour propager des logiciels malveillants à l'échelle d'un parc informatique.

---
[Source](https://www.bleepingcomputer.com/news/security/the-gentlemen-ransomware-now-uses-systembc-for-bot-powered-attacks/){:target="_blank"}
