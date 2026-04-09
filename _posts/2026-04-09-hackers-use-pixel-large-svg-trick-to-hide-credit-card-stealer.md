---
title: 'Hackers use pixel-large SVG trick to hide credit card stealer'
date: 2026-04-09
permalink: /posts/2026/04/09/hackers-use-pixel-large-svg-trick-to-hide-credit-card-stealer/
tags:
- veille-cyber
- bleepingcomp
---
### Dissimulation de skimmers bancaires via vecteurs SVG sur Magento

Une vaste campagne de cyberattaques cible près de 100 boutiques en ligne sous Magento, utilisant une technique d'obfuscation inédite pour dérober des données de cartes bancaires.

**Points clés :**
*   **Mode opératoire :** Les attaquants injectent un élément SVG d'un pixel dans le code HTML. Cet élément contient un gestionnaire `onload` qui exécute un script malveillant encodé en base64.
*   **Détection :** Cette méthode permet d'éviter les scanners de sécurité classiques en évitant les références à des scripts externes.
*   **Action malveillante :** Au moment du paiement, une fausse fenêtre de validation (« Secure Checkout ») apparaît pour intercepter les données bancaires, validées en temps réel par l'algorithme de Luhn avant exfiltration.
*   **Vecteur d'entrée :** Les chercheurs estiment que les attaquants exploitent la faille **PolyShell**, qui permet une exécution de code à distance sans authentification.

**Vulnérabilités :**
*   **PolyShell :** Vulnérabilité critique impactant toutes les versions stables de Magento Open Source et Adobe Commerce. Aucun correctif officiel n'est disponible sur les versions de production à ce jour (disponible uniquement en version alpha).

**Recommandations :**
*   **Nettoyage :** Rechercher et supprimer toute balise SVG contenant un attribut `onload` utilisant la fonction `atob()`.
*   **Audit technique :** Vérifier la présence de la clé `_mgx_cv` dans le `localStorage` du navigateur (témoin d'une compromission).
*   **Filtrage réseau :** Bloquer les requêtes vers `/fb_metrics.php` et les domaines analytiques inconnus.
*   **Blocage IP :** Restreindre le trafic vers l'adresse IP `23.137.249.67`.
*   **Mise à jour :** Si possible, migrer vers la version bêta corrigée fournie par Adobe en attendant un correctif définitif.

---
[Source](https://www.bleepingcomputer.com/news/security/hackers-use-pixel-large-svg-trick-to-hide-credit-card-stealer/){:target="_blank"}
