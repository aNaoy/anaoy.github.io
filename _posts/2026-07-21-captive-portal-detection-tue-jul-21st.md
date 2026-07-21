---
title: 'Captive Portal Detection, (Tue, Jul 21st)'
date: 2026-07-21
permalink: /posts/2026/07/21/captive-portal-detection-tue-jul-21st/
tags:
- veille-cyber
- sans-isc
---
### Détection des portails captifs et trafic réseau

Les honeypots détectent fréquemment du trafic lié à la vérification des portails captifs (pages de connexion WiFi publiques). Pour contourner la sécurisation généralisée par le protocole TLS, qui empêche les redirections forcées vers ces portails, les systèmes d'exploitation et navigateurs utilisent des requêtes HTTP non chiffrées vers des serveurs spécifiques pour tester la connectivité.

**Points clés :**
*   **Fonctionnement :** Lorsqu'un appareil rejoint un réseau, il tente de charger une URL HTTP spécifique. Si la requête est redirigée vers une page de connexion, le système identifie la présence d'un portail captif et ouvre l'interface d'authentification.
*   **Signatures logicielles :** Chaque système utilise une URL de test dédiée, permettant d'identifier le système d'exploitation ou le navigateur de l'utilisateur via les logs réseau :
    *   **Windows :** `http://www.msftconnecttest.com/connecttest.txt`
    *   **Apple :** `http://captive.apple.com/hotspot-detect.html`
    *   **Android :** `http://connectivitycheck.android.com/generate_204`
    *   **Chrome/Chromium :** `http://www.gstatic.com/generate_204` ou `http://clients3.google.com/generate_204`
    *   **Firefox :** `http://detectportal.firefox.com/canonical.html`

**Vulnérabilités :**
*   Aucune CVE associée : il s'agit d'un mécanisme de conception légitime et non d'une faille de sécurité. Cependant, ce trafic peut parfois être confondu avec des activités malveillantes lors de l'analyse des journaux (logs).

**Recommandations :**
*   **Diagnostic réseau :** Si un utilisateur est bloqué par un portail captif qui ne s'affiche pas automatiquement, il est recommandé de naviguer manuellement vers l'une des URLs listées ci-dessus. Cela forcera le déclenchement de la redirection vers la page d'authentification.
*   **Analyse des logs :** Les administrateurs de sécurité doivent reconnaître ces requêtes comme du trafic système standard afin d'éviter les faux positifs lors de la surveillance des menaces.

---
[Source](https://isc.sans.edu/diary/rss/33172){:target="_blank"}
