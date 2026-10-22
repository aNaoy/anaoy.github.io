---
title: 'ThreatsDay: AI Secrets Leak, PingCAP Source Theft, Signal Hang-Up Flaw, Laravel Auth Bypass + 21 More'
date: 2026-10-22
permalink: /posts/2026/10/22/threatsday-ai-secrets-leak-pingcap-source-theft-signal-hang-up-flaw-laravel-auth-bypass-21-more/
tags:
- veille-cyber
- hackernews
---
### Actualités Cybersécurité : Vulnérabilités critiques et incidents majeurs

Cette semaine a été marquée par une série d'incidents allant de fuites de données massives à des vulnérabilités critiques dans des outils largement utilisés.

#### Points clés et incidents notables
*   **Fuites de données et accès non autorisés :**
    *   **Bluesky :** Plus de 4 500 comptes compromis suite à une campagne de phishing promettant de faux paiements gouvernementaux.
    *   **PingCAP :** Accès non autorisé à des systèmes internes, entraînant le vol de code source et de données clients.
    *   **Zeabur :** Fermeture de la plateforme suite au vol de 3,2 millions d'enregistrements d'environnements et de données de 320 000 comptes.
    *   **Genesys :** Accès illégitime à des systèmes internes (CRM/LMS), sans impact sur ses plateformes Cloud.
*   **Malwares et fraudes :**
    *   **Fraude bancaire NFC :** Utilisation de l'IA pour cloner des voix et convaincre des victimes de scanner leurs cartes bancaires via NFC.
    *   **Scam Android :** Des publicités sur les réseaux sociaux incitent à installer des APK malveillants, causant près d'un million de dollars de pertes.
*   **IA et Sécurité :**
    *   **Risque de manipulation par l'IA :** Les modèles LLM d'origine chinoise génèrent du code potentiellement plus vulnérable lorsqu'ils sont sollicités pour des organisations occidentales.
    *   **OpenAI :** Une injection de prompt indirecte dans le connecteur GitHub de ChatGPT permet potentiellement l'exfiltration de secrets via des dépôts publics.

#### Vulnérabilités majeures (CVE)
*   **CVE-2026-65162 (ShadowForge - Score 10.0) :** Faille critique dans NVIDIA AIStore pour Kubernetes permettant une prise de contrôle totale de l'hôte.
*   **CVE-2026-114509 (Score 9.2) :** Contournement d'authentification critique dans **Laravel** (TokenGuard), permettant l'usurpation d'utilisateur.
*   **CVE-2026-113380 (Score 9.3) :** Flaille dans **Signal** (RingRTC) empêchant la déconnexion effective d'un appel audio/vidéo si la file d'attente est saturée par l'attaquant.
*   **Eptura Archibus (CVE-2026-107188 - Score 9.6) :** Vulnérabilité de téléchargement de fichier non sécurisé menant à une exécution de code à distance (RCE) avec privilèges élevés.
*   **GLPI (GHSA-753w-2942-4pxm) :** Injection SQL non authentifiée permettant la lecture de la base de données et une prise de contrôle admin.

#### Recommandations
1.  **Mises à jour urgentes :** Appliquez immédiatement les correctifs pour Laravel, Roundcube, GLPI et Eptura Archibus.
2.  **Gestion des accès :** Auditez les droits des connecteurs IA (ex: ChatGPT/GitHub) pour limiter l'accès aux dépôts privés et secrets.
3.  **Renforcement MFA :** Méfiez-vous des portails SSO frauduleux utilisant des techniques de "downgrade" (incitant à passer de la clé physique YubiKey vers le SMS/Email).
4.  **Hygène numérique :** Ne téléchargez jamais d'applications (APK) hors des stores officiels et restez vigilant face aux appels téléphoniques non sollicités, même si la voix semble familière.
5.  **Sécurisation des environnements :** Ne stockez jamais de secrets ou de variables d'environnement en texte clair dans vos systèmes de développement.

---
[Source](https://thehackernews.com/2026/10/threatsday-ai-secrets-leak-pingcap.html){:target="_blank"}
