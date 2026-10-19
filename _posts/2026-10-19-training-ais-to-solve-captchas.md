---
title: 'Training AIs to Solve CAPTCHAs'
date: 2026-10-19
permalink: /posts/2026/10/19/training-ais-to-solve-captchas/
tags:
- veille-cyber
- schneier
---
### L'obsolescence des CAPTCHA face aux IA apprenantes

Des chercheurs ont mis au point un système capable de résoudre les CAPTCHA visuels en combinant un modèle de vision (VLM) et un détecteur spécialisé (YOLOv8) travaillant en boucle fermée. Contrairement aux outils actuels, ce système apprend de chaque interaction : le VLM génère des étiquettes d'entraînement en temps réel, permettant au détecteur d'intégrer de nouvelles catégories ou de s'adapter aux perturbations malveillantes sans intervention humaine.

**Points clés :**
*   **Système hybride :** Utilisation d'un routeur basé sur la confiance pour alterner entre la rapidité du détecteur et l'intelligence du VLM.
*   **Apprentissage continu :** Le système améliore sa précision au fil des tentatives (atteignant 85,4 % de réussite globale).
*   **Résilience adaptative :** Même face à des tentatives de brouillage délibérées par l'opérateur du CAPTCHA, le modèle récupère systématiquement ses capacités grâce à son mécanisme d'auto-entraînement.
*   **Indépendance technique :** L'outil fonctionne uniquement par capture d'écran et simulation d'entrées utilisateur, contournant les protections basées sur l'analyse du DOM ou l'automatisation de navigateur.

**Vulnérabilités :**
*   L'article n'identifie pas de CVE spécifique, mais met en évidence une vulnérabilité structurelle des CAPTCHA visuels : l'hypothèse erronée qu'un bot déjoué restera inefficace face à de nouvelles perturbations.

**Recommandations :**
*   **Abandonner la dépendance aux CAPTCHA visuels :** La capacité d'apprentissage rapide des IA modernes rend obsolète la stratégie de "perturbation" des images pour bloquer les bots.
*   **Diversifier les méthodes d'authentification :** Privilégier des mécanismes basés sur le comportement (analyse de signaux), la cryptographie (WebAuthn/Passkeys) ou d'autres facteurs ne reposant pas sur la reconnaissance d'images, domaine où l'IA surpasse désormais largement les capacités humaines.

---
[Source](https://www.schneier.com/blog/archives/2026/10/training-ais-to-solve-captchas.html){:target="_blank"}
