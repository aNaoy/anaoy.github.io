---
title: 'Axios npm hack used fake Teams error fix to hijack maintainer account'
date: 2026-04-05
permalink: /posts/2026/04/05/axios-npm-hack-used-fake-teams-error-fix-to-hijack-maintainer-account/
tags:
- veille-cyber
- bleepingcomp
---
### Compromission de la supply chain npm : L'attaque par ingénierie sociale contre Axios

Le projet Axios a été victime d'une attaque sophistiquée sur sa chaîne d'approvisionnement via le registre npm. Des attaquants, liés au groupe nord-coréen UNC1069, ont compromis le compte d'un mainteneur pour publier deux versions malveillantes (1.14.1 et 0.30.4) intégrant un cheval de Troie d'accès à distance (RAT).

**Points clés :**
*   **Mode opératoire :** Les attaquants ont utilisé une campagne d'ingénierie sociale complexe (imposture d'entreprise, espaces Slack réalistes).
*   **Technique "ClickFix" :** Lors d'un appel vidéo simulé sur une fausse plateforme Teams, la victime a été incitée à installer une mise à jour corrective fictive, qui a déployé le malware sur son système.
*   **Impact :** Le malware a permis aux attaquants de dérober des jetons de session, contournant ainsi l'authentification multifacteur (MFA). 
*   **Envergure :** Il s'agit d'une campagne coordonnée visant plusieurs mainteneurs de projets Node.js à fort impact pour maximiser la portée de la compromission.

**Vulnérabilités :**
*   L'attaque n'a pas exploité une vulnérabilité logicielle classique (CVE), mais une faille humaine et opérationnelle. Le vecteur d'infection repose sur l'exécution de code malveillant déguisé en mise à jour logicielle sur le poste de travail du développeur.

**Recommandations :**
*   **Audit immédiat :** Si vous avez installé Axios entre le 10 et le 13 décembre 2024, considérez votre environnement comme compromis.
*   **Rotation des secrets :** Réinitialisez impérativement toutes les informations d'identification, clés API, jetons de session et mots de passe présents sur les machines affectées.
*   **Hygiène logicielle :** Ne jamais installer de mises à jour ou exécuter de commandes (type `curl`) suggérées lors d'un appel technique improvisé ou suspect, même si l'interlocuteur semble légitime.
*   **Vigilance accrue :** Les mainteneurs de projets Open Source doivent appliquer une politique de "Zero Trust" lors de leurs interactions professionnelles, même au sein de communautés connues.

---
[Source](https://www.bleepingcomputer.com/news/security/axios-npm-hack-used-fake-teams-error-fix-to-hijack-maintainer-account/){:target="_blank"}
