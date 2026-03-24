---
title: 'Using Markov Models for Password Complexity Estimation in Microsoft Edge'
date: 2026-03-24
permalink: /posts/2026/03/24/using-markov-models-for-password-complexity-estimation-in-microsoft-edge/
tags:
- veille-cyber
- zerodaysfans
---
### Amélioration de l’estimation de la robustesse des mots de passe dans Microsoft Edge

Microsoft Edge fait évoluer son moteur d'estimation de la force des mots de passe en remplaçant la bibliothèque « zxcvbn » (basée sur des dictionnaires et des règles manuelles) par un modèle probabiliste basé sur les chaînes de Markov. Cette transition vise à mieux modéliser le comportement des attaquants modernes, qui utilisent des techniques statistiques plutôt que des listes prédéfinies pour deviner les mots de passe.

**Points clés :**
*   **Limites de l'approche par dictionnaire :** Les outils comme *zxcvbn* souffrent d'un biais culturel et linguistique (prédominance de l'anglais), d'une maintenance lourde et d'une obsolescence rapide des références culturelles.
*   **Approche probabiliste (Modèles de Markov) :** Au lieu de reconnaître des mots, le modèle analyse la fréquence des transitions entre caractères (n-grams). Cela permet de détecter des séquences prévisibles indépendamment de la langue utilisée.
*   **Efficacité technique :** Le nouveau modèle, développé en Rust, réduit considérablement l'empreinte mémoire et le poids de stockage par rapport aux volumineuses listes de mots.
*   **Conformité avec les menaces réelles :** Les attaquants utilisant des outils comme *Hashcat* ou *John the Ripper* privilégient les probabilités statistiques. Le modèle de Markov s'aligne davantage sur cette réalité opérationnelle.

**Vulnérabilités associées :**
*   Aucune CVE spécifique n'est mentionnée, mais l'article souligne une faille conceptuelle : la surestimation de la sécurité de mots de passe longs composés de séquences prévisibles dans les outils basés sur des règles fixes.

**Recommandations :**
*   **Utilisation locale :** Privilégier des estimateurs qui effectuent les calculs sur l'appareil de l'utilisateur pour garantir la confidentialité des données (zéro transmission de mot de passe).
*   **Sécurisation du développement :** Utiliser des langages à sécurité mémoire comme **Rust** pour implémenter des composants critiques de sécurité afin de prévenir les vulnérabilités de bas niveau.
*   **Modernisation des outils :** Les concepteurs de navigateurs et d'applications doivent s'éloigner des listes de mots fixes pour adopter des modèles statistiques capables d'évoluer avec les nouvelles méthodes de devinette de mots de passe.

---
[Source](https://microsoftedge.github.io/edgevr/posts/Using-Markov-model-for-password-complexity-estimation-in-microsoft-edge/){:target="_blank"}
