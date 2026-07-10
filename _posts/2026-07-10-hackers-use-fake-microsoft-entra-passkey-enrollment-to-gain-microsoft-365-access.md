---
title: 'Hackers Use Fake Microsoft Entra Passkey Enrollment to Gain Microsoft 365 Access'
date: 2026-07-10
permalink: /posts/2026/07/10/hackers-use-fake-microsoft-entra-passkey-enrollment-to-gain-microsoft-365-access/
tags:
- veille-cyber
- hackernews
---
### Campagne de vishing ciblant l'inscription aux clés d'accès Microsoft Entra

Le groupe cybercriminel **O-UNC-066** (lié au collectif *The Com*) déploie une campagne de phishing vocal sophistiquée visant à compromettre des comptes Microsoft 365. En se faisant passer pour une assistance technique, les attaquants persuadent les utilisateurs d'enregistrer une « nouvelle clé d'accès » (passkey) via un portail malveillant, leur permettant de prendre le contrôle total du compte.

**Points clés :**
*   **Mode opératoire :** Utilisation du « vishing » (phishing vocal) pour instaurer un climat de confiance.
*   **Technique en temps réel :** Contrairement aux méthodes classiques, un opérateur humain pilote le kit de phishing en direct, adaptant les défis d'authentification (MFA) selon les besoins du compte visé.
*   **Détournement de processus :** Les attaquants exploitent les campagnes officielles d'incitation à l'usage des clés d'accès de Microsoft pour rendre leur demande crédible.
*   **Leurre de récupération :** La demande de saisie d'une phrase de récupération (similaire à un portefeuille crypto) sert de distraction pour maintenir l'utilisateur occupé pendant que l'attaquant enregistre sa propre clé d'accès sur le compte de la victime.
*   **Impact :** Accès complet aux comptes Microsoft 365 à des fins d'extorsion de données.

**Vulnérabilités :**
*   Il ne s'agit pas d'une vulnérabilité logicielle (CVE) spécifique, mais d'une **vulnérabilité humaine et procédurale** exploitant l'ingénierie sociale et le manque de familiarité des utilisateurs avec les nouveaux protocoles d'authentification sans mot de passe (FIDO2/passkeys).

**Recommandations :**
*   **Formation des utilisateurs :** Sensibiliser les employés au fait que Microsoft ne sollicitera jamais par téléphone l'enregistrement d'une clé d'accès ou d'une phrase de récupération.
*   **Vérification des canaux :** Rappeler aux utilisateurs de ne jamais suivre des instructions de sécurité reçues par appel téléphonique non sollicité ; inciter à valider toute demande via les canaux internes officiels de l'entreprise.
*   **Surveillance des logs :** Surveiller les inscriptions suspectes de nouvelles méthodes d'authentification MFA et les accès inhabituels dans le portail Microsoft Entra.
*   **Authentification robuste :** Imposer l'utilisation de clés de sécurité physiques (clés matérielles) plutôt que les méthodes de push notification ou OTP, plus vulnérables au phishing en temps réel.

---
[Source](https://thehackernews.com/2026/07/hackers-use-fake-microsoft-entra.html){:target="_blank"}
