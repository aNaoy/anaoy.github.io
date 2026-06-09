---
title: 'New FROST Attack Lets Websites Track What Sites and Apps You Open via SSD Timing'
date: 2026-06-09
permalink: /posts/2026/06/09/new-frost-attack-lets-websites-track-what-sites-and-apps-you-open-via-ssd-timing/
tags:
- veille-cyber
- hackernews
---
### FROST : Une nouvelle attaque par canal auxiliaire via SSD

L'attaque **FROST** permet à un site web malveillant de suivre les sites visités et les applications lancées par un utilisateur sans nécessiter de code natif, d'extension ou d'interaction spécifique. Cette technique exploite la contention des accès au disque SSD pour identifier les activités de l'utilisateur par simple analyse temporelle.

**Points clés :**
*   **Mécanisme :** L'attaquant utilise l'API **Origin Private File System (OPFS)** pour créer un fichier volumineux qui dépasse la capacité de la mémoire vive (RAM). Cela force le système d'exploitation à effectuer des lectures constantes sur le SSD.
*   **Analyse temporelle :** En mesurant la latence des lectures via JavaScript (avec une résolution haute précision obtenue grâce à l'isolation *cross-origin*), le script détecte des variations de performance causées par l'activité concurrente d'autres processus sur le disque.
*   **Efficacité :** Un réseau de neurones permet d'identifier les sites web ou les applications avec une précision élevée (jusqu'à 95,83 % pour les applications macOS natives dans les tests de recherche).
*   **Portée :** Fonctionne sur les navigateurs modernes (Chrome, Safari, Firefox) sous macOS et Linux.

**Vulnérabilités :**
*   Il n'existe actuellement aucun identifiant **CVE** pour cette attaque, car les éditeurs de navigateurs (Google, Apple, Mozilla) considèrent généralement le *fingerprinting* (empreinte numérique) comme un problème de confidentialité plutôt que comme une vulnérabilité critique.

**Recommandations :**
*   **Pour les utilisateurs :** Fermer les onglets suspects dès que possible pour stopper le script de surveillance. Bien que difficile à détecter, une utilisation inhabituelle de l'espace de stockage par le navigateur peut être un indicateur.
*   **Pour les utilisateurs Linux :** Utiliser des outils comme `profile-sync-daemon` pour maintenir le profil du navigateur en RAM, ce qui empêche l'attaquant de mesurer la contention du SSD.
*   **Mesures correctives attendues (côté éditeurs) :** Les chercheurs préconisent de limiter la taille de l'OPFS pour qu'elle puisse résider en cache mémoire, de limiter la précision des temporisateurs JavaScript lorsque l'OPFS est actif, ou d'introduire des invites de permission avant l'accès au stockage.

---
[Source](https://thehackernews.com/2026/06/new-frost-attack-lets-websites-track.html){:target="_blank"}
