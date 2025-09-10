---
title: 'Hackers left empty-handed after massive NPM supply-chain attack'
date: 2025-09-10
permalink: /posts/2025/09/10/hackers-left-empty-handed-after-massive-npm-supply-chain-attack/
tags:
- veille-cyber
- bleepingcomp
---
### Attaque Majeure sur NPM : Diffusion Rapide, Profit Minimal

Une compromission d'envergure a touché l'écosystème NPM, affectant potentiellement un large pourcentage d'environnements cloud. L'incident, survenu suite à un hameçonnage ciblant un mainteneur de paquets populaires comme `chalk` et `debug-js`, a permis aux attaquants d'injecter du code malveillant. Ce code visait à voler des cryptomonnaies en redirigeant les transactions vers leurs portefeuilles.

Malgré la rapidité de propagation du code malveillant, qui a atteint près de 10% des environnements cloud durant une fenêtre de deux heures, le profit généré par les attaquants est resté dérisoire, s'élevant à quelques centaines de dollars. Le type de charge utile, axé sur le vol de cryptomonnaies dans des environnements de navigateur, a limité les dégâts potentiels qui auraient pu inclure un accès plus profond aux systèmes.

**Points Clés :**

*   **Étendue de l'attaque :** L'une des plus grandes compromissions de la chaîne d'approvisionnement NPM, affectant des paquets utilisés par une majorité de projets JavaScript/Node.
*   **Méthode d'infection :** Hameçonnage du mainteneur d'un compte NPM, menant à la compromission de paquets populaires.
*   **Charge utile :** Code injecté ciblant le vol de cryptomonnaies en détournant les transactions.
*   **Vitesse de propagation :** Le code malveillant a pu contaminer environ 10% des environnements cloud en seulement deux heures.
*   **Impact limité sur le profit :** Les attaquants n'ont réussi à détourner qu'une somme très faible de cryptomonnaies.
*   **Autres paquets touchés :** La même campagne de hameçonnage a également affecté le projet `duckdb`.

**Vulnérabilités :**

*   **Compromission de compte :** Le vecteur initial était un hameçonnage réussi qui a permis à l'attaquant de prendre le contrôle d'un compte mainteneur NPM.
*   **Propagation de code malveillant via la chaîne d'approvisionnement :** La confiance inhérente aux paquets open-source a facilité la diffusion rapide du code préjudiciable.

**Recommandations :**

*   **Vigilance accrue face au hameçonnage :** Renforcer les mesures de sécurité et la sensibilisation des utilisateurs concernant les tentatives de hameçonnage, notamment pour la réinitialisation de mots de passe.
*   **Surveillance de la chaîne d'approvisionnement :** Mettre en place des outils et des processus pour surveiller les dépendances et détecter rapidement les modifications suspectes dans les paquets utilisés.
*   **Audit et nettoyage rapides :** Disposer de procédures d'urgence pour identifier, isoler et supprimer rapidement les composants compromis d'un système.
*   **Isolation des portefeuilles et des transactions sensibles :** Utiliser des configurations de portefeuille et des mécanismes de transaction qui limitent les risques de détournement automatique.

---
[Source](https://www.bleepingcomputer.com/news/security/hackers-left-empty-handed-after-massive-npm-supply-chain-attack/){:target="_blank"}
