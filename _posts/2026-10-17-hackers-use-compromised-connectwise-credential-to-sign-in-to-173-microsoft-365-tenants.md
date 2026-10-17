---
title: 'Hackers Use Compromised ConnectWise Credential to Sign In to 173 Microsoft 365 Tenants'
date: 2026-10-17
permalink: /posts/2026/10/17/hackers-use-compromised-connectwise-credential-to-sign-in-to-173-microsoft-365-tenants/
tags:
- veille-cyber
- hackernews
---
### Compromission de la chaîne d'approvisionnement : ConnectWise Cloud Backup

Une campagne malveillante exploite actuellement les identifiants compromis de l'application **ConnectWise Cloud Backup** (anciennement SkyKick) pour obtenir un accès non autorisé à 173 environnements Microsoft 365 (M365) de clients. En usurpant les privilèges étendus accordés à cet outil de sauvegarde, les attaquants peuvent lire les emails, les fichiers OneDrive/SharePoint et les données Teams, tout en tentant de créer des portes dérobées persistantes.

**Points clés :**
*   **Vecteur d'attaque :** Utilisation de jetons d'accès légitimes (Microsoft Graph) détournés via des identifiants ConnectWise compromis.
*   **Impact :** Accès illimité aux données des locataires M365 (mailboxes, stockage cloud, annuaires).
*   **Escalade de privilèges :** Dans certains cas, l'attaquant a ajouté ses propres applications avec des rôles d'administrateur global, permettant de compromettre d'autres outils de gestion MSP de confiance.
*   **Modus Operandi :** Utilisation de scripts automatisés pour parcourir les locataires (par ordre alphabétique) et exécution de requêtes via l'adresse IP suspecte `144.172.64.128`.

**Vulnérabilités :**
*   Il ne s'agit pas d'une vulnérabilité logicielle classique (CVE), mais d'une **compromission d'identifiants de service (Service Principal)**. 
*   Identifiants d'applications abusées :
    *   `506e08f9-6e9a-4da4-942b-a099a03644ae` (ConnectWise Cloud Backup)
    *   `24205314-2b89-4e07-a2a4-579e898a5640` (ConnectWise Cloud Management - MS Teams)
    *   *(Plusieurs autres IDs d'applications ConnectWise Cloud Management sont également concernés).*

**Recommandations :**
*   **Désactivation immédiate :** Désactiver l'application ConnectWise Cloud Backup dans le centre d'administration Entra jusqu'à ce que ConnectWise confirme la rotation des clés.
*   **Audit :** 
    *   Vérifier les journaux de connexion (*Sign-in logs*) dans le portail Entra pour les activités liées aux IDs mentionnés ci-dessus.
    *   Rechercher des anomalies dans les adresses IP (l'activité normale s'effectue via des plages IPv6 Azure privées).
    *   Auditer les changements de privilèges et l'ajout de nouvelles clés/secrets sur les applications au sein des locataires depuis le 13 octobre.
*   **Surveillance :** Activer les journaux d'activité Microsoft Graph pour détecter toute requête inhabituelle.

---
[Source](https://thehackernews.com/2026/10/hackers-use-compromised-connectwise.html){:target="_blank"}
