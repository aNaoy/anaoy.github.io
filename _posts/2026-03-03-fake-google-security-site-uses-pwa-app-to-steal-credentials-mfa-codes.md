---
title: 'Fake Google Security site uses PWA app to steal credentials, MFA codes'
date: 2026-03-03
permalink: /posts/2026/03/03/fake-google-security-site-uses-pwa-app-to-steal-credentials-mfa-codes/
tags:
- veille-cyber
- bleepingcomp
---
**Campagne de Phishing Exploitant des Progressive Web Apps pour Voler des Identifiants et Codes MFA**

Une campagne de phishing trompe les utilisateurs en les dirigeant vers un faux site de sécurité Google, utilisant des Progressive Web Apps (PWA) pour voler des informations sensibles. Le site frauduleux, ressemblant à une page de vérification de sécurité Google, incite les victimes à installer une PWA sous prétexte de renforcer la sécurité.

**Fonctionnalités Malveillantes et Exploitation :**

*   **Vol d'identifiants et de codes MFA :** La PWA peut intercepter les codes à usage unique (OTP) via l'API WebOTP et voler le contenu du presse-papiers, y compris les codes de vérification.
*   **Collecte de données :** La PWA est capable d'exfiltrer les contacts, les données GPS en temps réel et le contenu du presse-papiers.
*   **Proxy d'attaquant :** Elle transforme le navigateur de la victime en un proxy pour acheminer le trafic des attaquants, leur permettant d'exécuter des requêtes comme s'ils étaient sur le réseau de la victime.
*   **Scan de réseau :** La PWA peut effectuer un scan de port interne pour identifier des hôtes actifs sur le réseau de la victime.
*   **Empreinte numérique détaillée :** Le malware crée une empreinte numérique complète de l'appareil.
*   **Notifications pour déclencher des actions :** L'autorisation de notifications est utilisée pour envoyer de fausses alertes de sécurité, incitant l'utilisateur à ouvrir la PWA et à permettre l'exfiltration de données.
*   **Persistance :** L'utilisation de la synchronisation périodique en arrière-plan assure la connexion à l'appareil compromis tant que la PWA est installée.

**Composant Android Malveillant :**

Une application Android compagnon, présentée comme une mise à jour critique de sécurité, est proposée. Elle demande 33 permissions risquées, incluant l'accès aux SMS, journaux d'appels, microphone, contacts et service d'accessibilité. Cette application peut voler des données, compromettre entièrement l'appareil et faciliter la fraude financière, notamment grâce à un clavier personnalisé capturant les frappes, un écouteur de notifications et une interception des identifiants remplis automatiquement. Elle utilise également des techniques de persistance comme l'enregistrement en tant qu'administrateur de périphérique.

**Vulnérabilités Exploités (par l'ingénierie sociale) :**

Il n'y a pas de vulnérabilités techniques classiques exploitées. L'attaque repose entièrement sur l'ingénierie sociale pour tromper l'utilisateur afin qu'il accorde volontairement les permissions nécessaires.

**Recommandations :**

*   **Vigilance accrue :** Google ne procède pas à des vérifications de sécurité via des pop-ups sur des pages web ni ne demande d'installation de logiciel pour des fonctionnalités de protection.
*   **Source des outils de sécurité :** Tous les outils de sécurité légitimes de Google sont accessibles via le compte Google à l'adresse myaccount.google.com.
*   **Désinstallation :** Rechercher et désinstaller les applications nommées "Security Check" ou "System Service" (com.device.sync) si elles ont des accès administrateur.
*   **Révoquer les permissions :** Sur Android, révoquer les accès administrateur des applications suspectes avant de les désinstaller.
*   **Suppression des PWAs :** Suivre les instructions spécifiques pour supprimer les PWA malveillantes des navigateurs basés sur Chromium (Chrome, Edge) et Safari. La protection est moindre sur Firefox et Safari, bien que les notifications push fonctionnent toujours.
*   **Extraction des points clés :**
    *   Utilisation de PWA pour créer des applications web qui s'installent comme des applications natives.
    *   Ingénierie sociale pour obtenir des permissions risquées.
    *   Vol de codes d'authentification multifacteur (MFA) et d'identifiants.
    *   Capacité de transformer le navigateur de la victime en proxy pour le trafic de l'attaquant.
    *   L'application Android compagnon offre un niveau de compromission plus profond.
    *   Pas d'exploitation de vulnérabilités logicielles, mais exploitation de la confiance de l'utilisateur.

---
[Source](https://www.bleepingcomputer.com/news/security/fake-google-security-site-uses-pwa-app-to-steal-credentials-mfa-codes/){:target="_blank"}
