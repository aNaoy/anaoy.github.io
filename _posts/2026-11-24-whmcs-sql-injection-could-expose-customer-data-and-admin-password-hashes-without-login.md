---
title: 'WHMCS SQL Injection Could Expose Customer Data and Admin Password Hashes without Login'
date: 2026-11-24
permalink: /posts/2026/11/24/whmcs-sql-injection-could-expose-customer-data-and-admin-password-hashes-without-login/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans WHMCS : Injection SQL et exécution de code

La plateforme de facturation et d'automatisation WHMCS a corrigé trois vulnérabilités majeures permettant l'exposition de données clients, le vol de hashes de mots de passe administrateur et l'exécution de code arbitraire sur le serveur.

#### Points clés
*   **Risque majeur :** La faille la plus critique (CVE-2026-82981) ne nécessite aucune authentification, exposant les installations directement via internet.
*   **Origine :** Les trois vulnérabilités ont été découvertes par le chercheur en sécurité « alakazamspooon ».
*   **Statut :** Aucune preuve d'exploitation active n'a été signalée pour le moment.

#### Vulnérabilités identifiées
1.  **CVE-2026-82981 (CVSS 8.7) :** Injection SQL dans le panier d'achat. Permet à un attaquant non authentifié de récupérer des enregistrements clients et des hashes de mots de passe admin.
2.  **CVE-2026-82979 (CVSS 7.1) :** Injection SQL dans l'espace client. Nécessite qu'un utilisateur possède les permissions « View & Manage Contacts » pour extraire des données sensibles.
3.  **CVE-2026-93700 (CVSS 9.0) :** Faille dans les campagnes d'emailing permettant à un client authentifié de lire des fichiers de configuration (contenant des identifiants de base de données) et d'exécuter du code sur le serveur.

#### Recommandations
*   **Mise à jour immédiate :** Appliquez les correctifs vers les versions **9.0.10**, **8.13.8** ou **9.1.2**. Pour les versions antérieures (8.0 à 8.12), une mise à jour vers une version supportée est impérative.
*   **Action spécifique (CVE-2026-93700) :** Pour sécuriser les campagnes d'emailing, les administrateurs doivent impérativement :
    *   Supprimer toutes les campagnes prévues ou en cours via le menu *Utilities > Email Campaigns*.
    *   Vider le cache des modèles via *Utilities > System > System Cleanup > Empty Template Cache*.
    *   Procéder ensuite à la mise à jour du logiciel.
*   **Cloud vs Self-hosted :** Les instances « WHMCS Cloud » sont mises à jour automatiquement. Les administrateurs d'instances auto-hébergées doivent effectuer les mises à jour manuellement.

---
[Source](https://thehackernews.com/2026/11/whmcs-sql-injection-flaw-could-expose.html){:target="_blank"}
