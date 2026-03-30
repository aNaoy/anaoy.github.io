---
title: 'TeamPCP Supply Chain Campaign: Update 004 - Databricks Investigating Alleged Compromise, TeamPCP Runs Dual Ransomware Operations, and AstraZeneca Data Released, (Mon, Mar 30th)'
date: 2026-03-30
permalink: /posts/2026/03/30/teampcp-supply-chain-campaign-update-004-databricks-investigating-alleged-compromise-teampcp-runs-dual-ransomware-operations-and-astrazeneca-data-released-mon-mar-30th/
tags:
- veille-cyber
- sans-isc
---
### État des lieux de la campagne TeamPCP : Mutation vers la monétisation

La campagne TeamPCP a marqué une pause dans ses activités de compromission de la chaîne d'approvisionnement (aucun nouveau paquet infecté depuis le 27 mars), pour se concentrer sur l'exploitation des données dérobées et la monétisation.

**Points clés**
*   **Diversification de la monétisation :** Le groupe opère désormais sur trois fronts parallèles : l'exploitation directe de privilèges (cas Databricks), son propre programme de ransomware nommé **CipherForce**, et une distribution de masse via le service **Vect**.
*   **Fuite de données AstraZeneca :** Suite à l'échec de la vente des données volées, LAPSUS$ a publié gratuitement une archive de 3 Go, confirmée comme authentique par des recherches indépendantes.
*   **Transparence d'ownCloud :** L'entreprise a confirmé une intrusion dans ses systèmes de build via la vulnérabilité Trivy, une rare preuve de transparence dans ce cycle d'attaques.
*   **Recherche de nouveaux vecteurs :** Aucun signe de propagation vers RubyGems, crates.io ou Maven Central n'a été détecté pour le moment.

**Vulnérabilités identifiées**
*   **CVE-2026-33634 :** Compromission liée à Trivy, impactant l'infrastructure de build d'ownCloud.

**Recommandations**
*   **Databricks :** Si vos pipelines CI/CD ont été exposés à des composants compromis par TeamPCP et disposaient d'accès aux identifiants Databricks, considérez ces derniers comme compromis et effectuez une rotation immédiate.
*   **CipherForce :** Intégrez les indicateurs de compromission (IOC) liés à CipherForce dans vos outils de surveillance. L'élément de corrélation technique le plus fiable est une clé publique **RSA-4096** intégrée dans les charges utiles.
*   **AstraZeneca :** Les organisations ayant des accords de partage de données avec AstraZeneca doivent évaluer l'exposition potentielle (notamment pour les données de santé PHI/GDPR) et préparer les procédures de notification de violation.
*   **Conformité :** Utilisez la pause actuelle pour finaliser le nettoyage des accès et la rotation des secrets avant la date limite CISA KEV fixée au **8 avril 2026**.

---
[Source](https://isc.sans.edu/diary/rss/32846){:target="_blank"}
