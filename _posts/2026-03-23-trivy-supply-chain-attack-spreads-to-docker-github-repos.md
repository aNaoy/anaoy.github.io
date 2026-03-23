---
title: 'Trivy supply-chain attack spreads to Docker, GitHub repos'
date: 2026-03-23
permalink: /posts/2026/03/23/trivy-supply-chain-attack-spreads-to-docker-github-repos/
tags:
- veille-cyber
- bleepingcomp
---
### Compromission de la chaîne d'approvisionnement d'Aqua Security par TeamPCP

Le groupe de pirates « TeamPCP » a orchestré une attaque persistante contre Aqua Security, compromettant les pipelines de build GitHub et publiant des images Docker malveillantes pour l'outil de scan Trivy. Malgré les efforts de remédiation, les attaquants ont réitéré leur intrusion en exploitant un compte de service sur-privilégié.

**Points clés :**
* **Propagation de l'attaque :** Utilisation de versions malveillantes de Trivy (tags 0.69.5 et 0.69.6) non officielles pour distribuer un infostealer (« TeamPCP Cloud stealer »).
* **Sabotage des dépôts :** Altération de 44 dépôts GitHub (renommage et modification des descriptions) pour revendiquer l'intrusion.
* **Vecteur d'accès :** Compromission d'un compte de service (`Argon-DevOps-Mgt`) utilisant un jeton d'accès personnel (PAT) permanent, dépourvu d'authentification multifacteur (MFA).
* **Persistence :** Les attaquants ont exploité une procédure de rotation des secrets incomplète, leur permettant de récupérer des jetons rafraîchis.

**Vulnérabilités exploitées :**
* **Absence d'immuabilité :** Utilisation abusive des tags Docker Hub, qui ne sont pas immuables, permettant aux attaquants de remplacer des images légitimes.
* **Gestion des identités (IAM) :** Utilisation de PAT (Personal Access Tokens) pour des comptes de service automatisés, une pratique moins sécurisée que l'usage des GitHub Apps.
* **Exfiltration de secrets :** Le malware a ciblé les environnements CI pour dérober des jetons GitHub, des clés SSH et des variables d'environnement.

**Recommandations :**
* **Sécurisation des accès :** Privilégier les « GitHub Apps » aux PAT pour les comptes de service et activer systématiquement le MFA.
* **Gestion des secrets :** Mettre en œuvre une rotation des jetons atomique et révoquer immédiatement tout jeton exposé ou potentiellement compromis lors d'un incident.
* **Intégrité de la chaîne d'approvisionnement :** Ne pas se fier uniquement aux tags Docker pour vérifier l'intégrité des images ; privilégier le hachage (digest) des images.
* **Audit des pipelines :** Surveiller étroitement les environnements CI/CD pour détecter toute activité anormale liée aux comptes de service et restreindre leurs permissions au strict nécessaire (principe du moindre privilège).

---
[Source](https://www.bleepingcomputer.com/news/security/trivy-supply-chain-attack-spreads-to-docker-github-repos/){:target="_blank"}
