---
title: 'Sneaky 2FA Phishing Kit Adds BitB Pop-ups Designed to Mimic the Browser Address Bar'
date: 2025-11-19
permalink: /posts/2025/11/19/sneaky-2fa-phishing-kit-adds-bitb-pop-ups-designed-to-mimic-the-browser-address-bar/
tags:
- veille-cyber
- hackernews
---
**Les Kits de Phishing "Sneaky 2FA" Évoluent avec des Fausses Fenêtres de Navigation**

Des acteurs malveillants utilisant le kit de phishing "Sneaky 2FA" intègrent désormais des pop-ups "Browser-in-the-Browser" (BitB) pour tromper les utilisateurs. Cette technique permet de créer de fausses fenêtres de connexion qui imitent parfaitement celles des services légitimes, rendant le vol d'identifiants plus facile, même pour des attaquants moins expérimentés.

**Points Clés :**

*   **Technique BitB :** Utilisation de code HTML et CSS pour créer de fausses fenêtres de navigateur simulant des pop-ups de connexion légitimes.
*   **Objectif :** Voler les identifiants de connexion des victimes, notamment pour les comptes Microsoft.
*   **Mécanisme :** La fausse fenêtre affiche une URL légitime et intercepte les informations saisies par l'utilisateur.
*   **Évasion des Défenses :** Utilisation de protections anti-bots (Cloudflare Turnstile), de techniques de chargement conditionnel pour cibler uniquement les victimes et de rotation rapide des noms de domaine.
*   **Résistance à l'Analyse :** Obfuscation du code et désactivation des outils de développement du navigateur.
*   **Écosystème PhaaS :** L'évolution de ces kits s'inscrit dans un marché de phishing professionnelisé.

**Vulnérabilités :**

*   **Manipulation de la Connexion Passkey (CVE non spécifié) :** Des extensions de navigateur malveillantes peuvent falsifier l'enregistrement et la connexion aux passkeys, permettant l'accès aux applications d'entreprise sans le consentement de l'utilisateur ou ses données biométriques. Cette attaque exploite l'absence de canal de communication sécurisé entre l'appareil et le service, en manipulant le navigateur via injection de JavaScript.
*   **Attaques par Dégra d'Adaptation (Downgrade Attacks) (CVE non spécifié) :** Des kits de phishing "Adversary-in-the-Middle" (AitM) peuvent inciter les victimes à choisir une méthode d'authentification moins sécurisée et vulnérable au phishing, même si une option plus résistante comme les passkeys est disponible.

**Recommandations :**

*   **Vigilance des Utilisateurs :** Faire preuve de prudence avant d'ouvrir des messages suspects ou d'installer des extensions de navigateur.
*   **Politiques d'Accès Conditionnel :** Les organisations devraient restreindre les connexions ne répondant pas à certains critères pour prévenir le détournement de comptes.
*   **Ne jamais faire confiance aux pop-ups de connexion :** Vérifiez toujours l'URL dans la barre d'adresse principale du navigateur, pas dans une fenêtre pop-up qui pourrait être une imitation.
*   **Éviter les extensions de navigateur non vérifiées :** Limitez l'installation d'extensions aux sources de confiance et aux fonctions strictement nécessaires.

---
[Source](https://thehackernews.com/2025/11/sneaky-2fa-phishing-kit-adds-bitb-pop.html){:target="_blank"}
