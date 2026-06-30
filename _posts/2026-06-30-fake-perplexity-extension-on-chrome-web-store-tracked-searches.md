---
title: 'Fake Perplexity extension on Chrome Web Store tracked searches'
date: 2026-06-30
permalink: /posts/2026/06/30/fake-perplexity-extension-on-chrome-web-store-tracked-searches/
tags:
- veille-cyber
- bleepingcomp
---
### Espionnage des recherches : L'extension malveillante "Search for perplexity ai"

Une extension malveillante, se faisant passer pour l'outil de recherche Perplexity AI, a été identifiée sur le Chrome Web Store. Elle intercepte et redirige l'intégralité des requêtes saisies dans la barre d'adresse des utilisateurs vers une infrastructure tierce contrôlée par des attaquants, avant de les renvoyer vers les moteurs de recherche légitimes.

**Points clés :**
*   **Usurpation d'identité :** L'extension utilise une image de marque trompeuse et un domaine frauduleux (`perplexity-ai[.]online`) pour duper les utilisateurs.
*   **Modification des paramètres :** Elle exploite `chrome_settings_overrides` pour remplacer le moteur de recherche par défaut du navigateur.
*   **Collecte de données :** Bien qu'aucun vol de mots de passe n'ait été constaté, les permissions accordées permettent techniquement une exfiltration de données sensibles et un profilage approfondi des habitudes de navigation.
*   **Technique malicieuse :** L'extension abuse des permissions *Declarative Net Request* (DNR) pour filtrer, réécrire les URLs et rediriger le trafic réseau, ce qui est anormal pour une extension de type assistant IA.

**Vulnérabilités :**
*   Aucune CVE n'est associée, car l'incident repose sur l'exploitation abusive des fonctionnalités légitimes du moteur Chromium et des permissions excessives accordées par les utilisateurs lors de l'installation.

**Recommandations :**
*   **Suppression immédiate :** Désinstaller l'extension identifiée sous l'ID : `flkebkiofojicogddingbdmcmkpbplcd`.
*   **Sécurisation des accès :** Par mesure de précaution, modifier les mots de passe des comptes critiques utilisés sur le navigateur.
*   **Vigilance :** Vérifier systématiquement l'éditeur officiel d'une extension et comparer le domaine de support avec le site officiel avant toute installation. Privilégier l'extension officielle nommée « Perplexity – AI Search ».

---
[Source](https://www.bleepingcomputer.com/news/security/fake-perplexity-extension-on-chrome-web-store-tracked-searches/){:target="_blank"}
