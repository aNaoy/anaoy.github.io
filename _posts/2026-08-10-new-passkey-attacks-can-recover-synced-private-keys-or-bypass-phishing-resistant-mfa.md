---
title: 'New Passkey Attacks Can Recover Synced Private Keys or Bypass Phishing-Resistant MFA'
date: 2026-08-10
permalink: /posts/2026/08/10/new-passkey-attacks-can-recover-synced-private-keys-or-bypass-phishing-resistant-mfa/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités des passkeys : entre contournements MFA et vol de clés

Des recherches récentes ont mis en lumière trois méthodes permettant de compromettre l'authentification par « passkey », non pas en brisant le chiffrement FIDO2, mais en exploitant des failles dans l'implémentation logicielle et la gestion des sessions utilisateur.

**Points clés :**
*   **SpecterOps (Pass-the-Passkey) :** Exploitation du service de journalisation des événements Windows (CVE-2026-34348) pour récupérer des signatures réutilisables. Ces dernières permettent d'usurper l'identité d'utilisateurs privilégiés sur Microsoft Entra ID malgré l'exigence de MFA résistante au phishing.
*   **Unit 42 (Google Password Manager) :** Démonstration que des logiciels malveillants peuvent manipuler le gestionnaire de mots de passe de Chrome pour récupérer des clés privées synchronisées ou forcer l'authentification sans interaction utilisateur. La clé maîtresse (*Security Domain Secret*) peut être extraite de la mémoire vive du processus.
*   **Dirk-jan Mollema (Windows Hello) :** Un processus malveillant dans une session active peut solliciter Windows Hello for Business sans demander de PIN ou de biométrie, permettant de générer de nouveaux jetons d'authentification valides pour Entra ID.

**Vulnérabilités identifiées :**
*   **CVE-2026-34348 :** Divulgation d'informations dans le service de journalisation des événements Windows permettant la fuite de signatures d'authentification.
*   **Failles Entra ID / WebAuthn :** Défauts de validation des assertions de type « relay » et absence de liaison session/appareil pour certains défis WebAuthn.
*   **Gestion mémoire :** Persistance de clés de sécurité sensibles (Security Domain Secret) dans la mémoire des processus Chrome.

**Recommandations :**
*   **Correctifs :** Appliquer immédiatement les mises à jour de sécurité Microsoft pour la vulnérabilité **CVE-2026-34348**.
*   **Sécurité des terminaux :** Protéger les zones sensibles (mémoire des navigateurs, coffres-forts de passkeys) via des solutions EDR/XDR, car les attaques nécessitent une présence initiale sur la machine.
*   **Surveillance :** Monitorer les authentifications Windows Hello for Business suspectes (absence d'identifiant d'appareil) et les enregistrements d'appareils inhabituels au sein d'Entra ID.
*   **Application rigoureuse :** Les services acceptant les assertions WebAuthn doivent strictement valider les exigences de vérification utilisateur et ne pas se reposer uniquement sur la présence du jeton.

---
[Source](https://thehackernews.com/2026/08/new-passkey-attacks-can-recover-synced.html){:target="_blank"}
