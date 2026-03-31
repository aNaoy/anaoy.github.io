---
title: 'TeamPCP Supply Chain Campaign: Update 004 - Databricks Investigating Alleged Compromise, TeamPCP Runs Dual Ransomware Operations, and AstraZeneca Data Released, (Mon, Mar 30th)'
date: 2026-03-31
permalink: /posts/2026/03/31/teampcp-supply-chain-campaign-update-004-databricks-investigating-alleged-compromise-teampcp-runs-dual-ransomware-operations-and-astrazeneca-data-released-mon-mar-30th/
tags:
- veille-cyber
- sans-isc
---
### Évolution de la campagne TeamPCP : Transition vers l'exploitation et la monétisation

La campagne TeamPCP a marqué une pause dans ses activités de compromission de la chaîne d'approvisionnement (aucun nouveau paquet corrompu depuis le 27 mars) pour se concentrer sur l'exploitation des 300 Go de données d'identification dérobées. Le groupe déploie désormais trois stratégies de monétisation parallèles.

#### Points clés
*   **Databricks sous investigation :** La plateforme fait l'objet d'une enquête pour une compromission présumée liée aux identifiants récoltés par TeamPCP. Des traces d'artefacts AWS et de jetons STS correspondent au mode opératoire du groupe.
*   **Dualité des opérations de ransomware :** TeamPCP opère via deux canaux distincts : le programme d'affiliation de masse « Vect » et leur propre projet propriétaire, « CipherForce », pour cibler des entreprises à haute valeur ajoutée.
*   **Fuite de données AstraZeneca :** Suite à l'échec de la vente, les données volées (code source, informations développeurs) ont été publiées gratuitement par le groupe LAPSUS$. L'absence de communication officielle d'AstraZeneca accroît les risques réglementaires (RGPD/HIPAA).
*   **Transparence ownCloud :** L'entreprise a confirmé que ses systèmes de build ont été impactés par la faille de la chaîne d'approvisionnement Trivy, sans toutefois subir de vol de données clients ou de modification de code source.

#### Vulnérabilités identifiées
*   **CVE-2026-33634 :** Compromission de l'outil Trivy affectant les infrastructures de build (date limite de remédiation CISA fixée au 8 avril 2026).

#### Recommandations
*   **Databricks :** Si vos pipelines CI/CD exposés aux composants compromis par TeamPCP avaient accès aux identifiants Databricks, considérez ceux-ci comme compromis par précaution et effectuez une rotation immédiate.
*   **Surveillance :** Intégrez les indicateurs de « CipherForce » à vos outils de détection, en utilisant la **clé publique RSA-4096** intégrée aux charges utiles (payloads) comme principal indicateur d'attribution.
*   **Gestion des risques :** Considérez la fuite de données AstraZeneca comme confirmée. Si votre organisation possède des accords de partage de données avec eux, auditez vos systèmes pour détecter toute exposition potentielle de données sensibles (PHI/RGPD).
*   **Remédiation :** Profitez de la pause actuelle dans la campagne pour finaliser les rotations d'identifiants et appliquer les correctifs nécessaires avant l'échéance CISA du 8 avril.

---
[Source](https://isc.sans.edu/diary/rss/32846){:target="_blank"}
