---
title: 'TeamPCP Supply Chain Campaign: Update 007 - Cisco Source Code Stolen via Trivy-Linked Breach, Google GTIG Tracks TeamPCP as UNC6780, and CISA KEV Deadline Arrives with No Standalone Advisory, (Wed, Apr 8th)'
date: 2026-04-08
permalink: /posts/2026/04/08/teampcp-supply-chain-campaign-update-007-cisco-source-code-stolen-via-trivy-linked-breach-google-gtig-tracks-teampcp-as-unc6780-and-cisa-kev-deadline-arrives-with-no-standalone-advisory-wed-apr-8th/
tags:
- veille-cyber
- sans-isc
---
### Campagne de supply chain TeamPCP (UNC6780) : Analyse et État des Lieux

La campagne TeamPCP, désormais officiellement désignée **UNC6780** par Google (GTIG), se concentre actuellement sur la monétisation des identifiants volés plutôt que sur de nouvelles compromissions de la chaîne d'approvisionnement (pause observée depuis 24 jours). Le groupe utilise le malware **SANDCLOCK** pour exfiltrer des données.

#### Faits marquants
*   **Cisco :** Environnement de développement compromis via le plugin GitHub Action corrompu de Trivy. Plus de 300 dépôts (incluant du code source AI et des données sensibles de clients institutionnels/gouvernementaux) et des clés AWS ont été exfiltrés.
*   **ShinyHunters :** Le groupe poursuit des activités parallèles, notamment une campagne visant Snowflake via des jetons d'authentification Anodot, tout en exploitant les accès issus de la campagne TeamPCP.
*   **CipherForce :** Inactivité prolongée des sites de fuite (44 jours), suggérant soit des troubles internes ("chasse aux taupes"), soit des mesures de sécurité opérationnelle.
*   **CISA :** La date limite du 8 avril pour le correctif CVE-2026-33634 est atteinte, bien qu'aucune directive d'urgence spécifique à la campagne n'ait été publiée par CISA.

#### Vulnérabilités clés
*   **CVE-2026-33634 :** Compromission de la chaîne d'approvisionnement via **Trivy**. Cette vulnérabilité a permis l'accès initial aux environnements de développement et le vol massif d'identifiants.

#### Recommandations stratégiques
*   **Remédiation immédiate :** Les organisations doivent appliquer les correctifs (Trivy v0.69.2+, trivy-action v0.35.0, setup-trivy v0.2.6). 
*   **Rotation des secrets :** Le simple correctif est insuffisant. Il est impératif d'effectuer une rotation complète de tous les secrets et identifiants qui auraient pu être exposés durant la fenêtre de compromission (19-27 mars).
*   **Investigation :** Les entreprises partenaires ou clientes de Cisco doivent contacter l'éditeur pour vérifier si leurs dépôts ou artefacts de build ont été compromis.
*   **Monitoring :** Utiliser les indicateurs de compromission liés à **UNC6780** et **SANDCLOCK** au sein des outils de sécurité (Chronicle, VirusTotal, Mandiant Advantage).
*   **Veille :** Surveiller les fuites de données potentielles, notamment concernant le dossier Sportradar, dont l'échéance de publication est imminente.

---
[Source](https://isc.sans.edu/diary/rss/32880){:target="_blank"}
