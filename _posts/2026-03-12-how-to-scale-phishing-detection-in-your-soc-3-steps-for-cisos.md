---
title: 'How to Scale Phishing Detection in Your SOC: 3 Steps for CISOs'
date: 2026-03-12
permalink: /posts/2026/03/12/how-to-scale-phishing-detection-in-your-soc-3-steps-for-cisos/
tags:
- veille-cyber
- hackernews
---
### Optimiser la détection du phishing en entreprise : Stratégie pour les SOC

La recrudescence des campagnes de phishing modernes, qui exploitent des infrastructures légitimes et des flux chiffrés, rend les approches traditionnelles de détection obsolètes. Pour les CISO, l'enjeu est de faire évoluer le SOC vers un modèle capable de valider les menaces à la vitesse de la machine afin de prévenir le vol d'identités et les compromissions de comptes.

**Points clés**
*   **Limites du modèle classique :** L'analyse statique échoue face aux redirections multiples et aux pages de phishing dynamiques.
*   **Risques métiers :** Vol d'identifiants, mouvements latéraux dans les environnements SaaS/Cloud et délais de détection critiques.
*   **Performance opérationnelle :** Une automatisation intelligente permet de réduire significativement le temps moyen de traitement (MTTR) et la charge de travail des analystes (Tier 1).

**Vulnérabilités exploitées**
L'article souligne l'usage détourné de services légitimes (ex: Microsoft Azure Blob Storage) et l'exploitation de protocoles de sécurité pour dissimuler des activités malveillantes :
*   **Moyens de contournement :** Utilisation de CAPTCHAs, codes QR, et chaînes de redirection complexes pour tromper l'automatisation classique.
*   **Chiffrement HTTPS :** L'utilisation de sessions chiffrées (SSL/TLS) rend les flux de phishing indiscernables du trafic légitime pour les outils de monitoring standards.
*   **Menaces identifiées :** Tycoon2FA, Salty2FA.

**Recommandations pour les CISO**
Pour scaler la détection, trois changements structurels sont préconisés :
1.  **Adopter l'analyse interactive :** Utiliser des bacs à sable (sandboxes) permettant aux analystes (ou à l'automatisation) d'interagir réellement avec les liens suspects (clics, saisie de formulaires) pour révéler le comportement malveillant en temps réel.
2.  **Combiner automatisation et interactivité :** Déployer des solutions capables de résoudre automatiquement les défis (CAPTCHAs, etc.) pour traiter les alertes sans saturer les équipes.
3.  **Implémenter le déchiffrement SSL :** Automatiser le déchiffrement du trafic HTTPS au sein de l'environnement d'analyse pour exposer les charges utiles et les mécanismes de vol de sessions dissimulés derrière un masque de légitimité.

---
[Source](https://thehackernews.com/2026/03/how-to-scale-phishing-detection-in-your.html){:target="_blank"}
