---
title: 'ThreatsDay Bulletin: Claude Security Plugin, Azure Priv-Esc, Kali365 MFA Bypass, FIFA Scams +15 More'
date: 2026-05-28
permalink: /posts/2026/05/28/threatsday-bulletin-claude-security-plugin-azure-priv-esc-kali365-mfa-bypass-fifa-scams-15-more/
tags:
- veille-cyber
- hackernews
---
### Panorama des menaces : Campagnes de phishing, vulnérabilités critiques et cybercriminalité en hausse

Le paysage des menaces actuel est marqué par une exploitation croissante de la confiance des utilisateurs, des configurations négligées et des outils légitimes détournés.

#### Points clés
*   **Infrastructure C2 massive :** Plus de 1 350 serveurs de commande et de contrôle (C2) identifiés au Moyen-Orient en trois mois, dominés par des botnets IoT (Hajime, Mozi, Mirai) et des frameworks offensifs comme Cobalt Strike.
*   **Fraude à grande échelle :** Explosion des arnaques liées à la Coupe du Monde FIFA 2026, incluant des sites frauduleux, des ventes de billets factices et des campagnes de phishing sophistiquées (GHOST STADIUM) via les réseaux sociaux.
*   **Phishing-as-a-Service (PhaaS) :** La plateforme Kali365 permet le vol de jetons OAuth Microsoft 365 pour contourner l'authentification multifacteur (MFA).
*   **Détournement d'outils légitimes :** Utilisation de binaires signés (certificats volés/frauduleux) pour déployer des RAT (Remote Access Trojans), comme observé avec les installeurs piégés de DAEMON Tools ou RVTools.
*   **Techniques d'évasion :** La technique « GhostTree » utilise des jonctions NTFS récursives pour neutraliser l'analyse des EDR et outils de sécurité.

#### Vulnérabilités majeures
*   **Azure AKS (Privilege Escalation) :** Une faille (sans CVE, score CVSS 9.9) permettait à un utilisateur avec le rôle "Backup Contributor" d'obtenir les droits `cluster-admin`. Corrigé silencieusement par Microsoft.
*   **DAEMON Tools (CVE-2026-8398) :** Attaque par chaîne d'approvisionnement ayant conduit à la signature de binaires malveillants par le certificat légitime de l'éditeur (Score CVSS 9.3).
*   **Vaultjacking :** Technique permettant d'extraire le code PIN du gestionnaire de mots de passe Google via une attaque de type Adversary-in-the-Middle (AitM), compromettant l'ensemble du coffre-fort de mots de passe et passkeys.

#### Recommandations
*   **Renforcement de la posture :** Ne pas se fier aveuglément aux signatures numériques des logiciels ; vérifier systématiquement la révocation des certificats (OCSP/CRL).
*   **Protection des identités :** Se méfier des sollicitations de support technique par téléphone ou email. Privilégier les méthodes d'authentification résistantes au phishing et surveiller l'octroi d'autorisations OAuth.
*   **Gestion des vulnérabilités :** Auditer les configurations des environnements cloud (notamment Azure/Kubernetes) pour limiter les privilèges excessifs.
*   **Sécurité des postes de travail :** Sensibiliser les utilisateurs aux risques des installateurs provenant de sources tierces (GitHub, SourceForge) et maintenir les agents de sécurité (EDR) à jour pour détecter les techniques de contournement de fichiers.

---
[Source](https://thehackernews.com/2026/05/threatsday-bulletin-claude-security.html){:target="_blank"}
