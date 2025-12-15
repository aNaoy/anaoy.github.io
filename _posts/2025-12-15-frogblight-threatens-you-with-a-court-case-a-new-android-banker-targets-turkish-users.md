---
title: 'Frogblight threatens you with a court case: a new Android banker targets Turkish users'
date: 2025-12-15
permalink: /posts/2025/12/15/frogblight-threatens-you-with-a-court-case-a-new-android-banker-targets-turkish-users/
tags:
- veille-cyber
- securelist
---
**Frogblight : Un nouveau cheval de Troie bancaire Android cible les utilisateurs turcs**

Une campagne malveillante a été découverte visant principalement les utilisateurs en Turquie, utilisant un nouveau logiciel malveillant Android nommé "Frogblight". Initialement déguisé en application pour accéder aux dossiers judiciaires via un site web gouvernemental officiel, il a ensuite adopté des identités plus génériques comme le navigateur Chrome.

**Points Clés :**

*   **Distribution par Smishing :** Les victimes sont incitées à télécharger le logiciel malveillant via des SMS frauduleux qui les font croire qu'elles sont impliquées dans une affaire judiciaire.
*   **Vol d'identifiants bancaires :** Le malware utilise les sites web officiels comme intermédiaires pour dérober les informations de connexion bancaires des utilisateurs.
*   **Fonctionnalités d'espionnage :** Frogblight collecte les SMS, la liste des applications installées, et des informations sur le système de fichiers, tout en étant capable d'envoyer des SMS arbitraires.
*   **Développement continu :** Le malware a été mis à jour avec de nouvelles fonctionnalités en septembre, suggérant un développement actif et une potentielle distribution via un modèle "Malware as a Service" (MaaS).
*   **Évasion et persistance :** Il intègre des mécanismes pour éviter les émulateurs, contourner la détection géographique (États-Unis) et assurer sa persistance sur l'appareil compromis, tout en se protégeant contre la désinstallation.
*   **Communication C2 évolutive :** Initialement via une API REST, la communication avec le serveur de commande et de contrôle (C2) est passée à l'utilisation de WebSockets, sécurisée par une clé d'authentification.

**Vulnérabilités (sans CVE spécifique identifiée dans l'article) :**

*   Le malware exploite la confiance des utilisateurs envers les applications gouvernementales et les navigateurs courants.
*   Il abuse des permissions accordées par l'utilisateur (lecture/envoi de SMS, accès au stockage, accessibilité) pour mener ses actions malveillantes.
*   Le mécanisme d'injection JavaScript dans les WebViews permet de capturer les données saisies par l'utilisateur.

**Recommandations :**

*   **Prudence avec les SMS et liens suspects :** Ne pas cliquer sur les liens provenant de SMS inconnus ou suspects, même s'ils semblent provenir d'une source officielle.
*   **Téléchargement d'applications depuis des sources sûres :** Télécharger uniquement des applications depuis les magasins d'applications officiels (Google Play Store).
*   **Vérification des permissions :** Examiner attentivement les permissions demandées par les applications et les refuser si elles ne semblent pas nécessaires au fonctionnement de l'application.
*   **Mise à jour du système et des applications :** Maintenir le système d'exploitation Android et toutes les applications à jour pour corriger les vulnérabilités connues.
*   **Utilisation d'une solution de sécurité mobile :** Installer et maintenir à jour un logiciel antivirus et anti-malware fiable sur les appareils Android.
*   **Méfiance envers les applications déguisées :** Être particulièrement vigilant face aux applications qui se font passer pour des applications système ou des navigateurs connus.

---
[Source](https://securelist.com/frogblight-banker/118440/){:target="_blank"}
