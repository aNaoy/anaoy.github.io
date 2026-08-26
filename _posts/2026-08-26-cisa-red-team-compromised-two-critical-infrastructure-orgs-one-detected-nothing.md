---
title: 'CISA Red Team Compromised Two Critical Infrastructure Orgs, One Detected Nothing'
date: 2026-08-26
permalink: /posts/2026/08/26/cisa-red-team-compromised-two-critical-infrastructure-orgs-one-detected-nothing/
tags:
- veille-cyber
- hackernews
---
### Analyse comparative de CISA : L'efficacité opérationnelle face aux cyberattaques

La CISA a mené des tests d'intrusion simultanés (Red Team) contre deux infrastructures critiques, révélant des disparités majeures dans la capacité de détection et de réponse, malgré l'utilisation de vecteurs d'attaque identiques. Alors que l'Organisation A n'a détecté aucune intrusion, l'Organisation B a neutralisé la menace initiale en quelques minutes, démontrant que l'efficacité repose davantage sur les processus humains que sur les outils de sécurité.

**Points clés :**
*   **Organisation A (Échec total) :** Défaillance systémique due à une surcharge d'alertes (faux positifs), un manque de visibilité centralisée entre les différents SOC, et des procédures d'escalade inexistantes. Une alerte réelle a été ignorée par manque de clarté sur la propriété des actifs.
*   **Organisation B (Succès défensif) :** Détection rapide des tentatives d'hameçonnage, isolement immédiat des postes compromis et segmentation réseau efficace (notamment vers les systèmes OT).

**Vulnérabilités exploitées :**
*   **Configuration AD CS (ESC1) :** Modèles de certificats mal configurés permettant l'usurpation d'identité d'utilisateurs.
*   **Machine Account Quota :** Configuration par défaut permettant à tout utilisateur du domaine d'ajouter des comptes machines.
*   **Gestion des identifiants :** Stockage de mots de passe en clair (fichiers de configuration SCCM/bases de données) et clés AWS statiques sans expiration.
*   **Permissions cloud :** Applications Entra ID sur-privilégiées permettant la lecture des courriels.
*   **Technique "Certighost" :** Abus des modèles de certificats pour une prise de contrôle totale du domaine.

**Recommandations :**
*   **Durcissement de l'Active Directory :** Restreindre le quota de création de comptes machines et auditer les modèles de certificats AD CS.
*   **Gestion des accès :** Supprimer les identifiants en clair et les clés d'accès cloud statiques ; privilégier la rotation des jetons.
*   **Hygiène opérationnelle :** Réduire les faux positifs pour garantir la visibilité des menaces réelles et établir des procédures d'escalade claires.
*   **Segmentation :** Appliquer le principe du moindre privilège aux applications cloud et isoler les environnements critiques (OT) pour empêcher la propagation latérale.
*   **Processus humains :** Mettre l'accent sur la formation des équipes SOC pour assurer une réponse coordonnée plutôt que de se reposer uniquement sur les outils technologiques.

---
[Source](https://thehackernews.com/2026/08/cisa-red-team-compromised-two-critical.html){:target="_blank"}
