---
title: 'Is a $30,000 GPU Good at Password Cracking?'
date: 2026-04-08
permalink: /posts/2026/04/08/is-a-30000-gpu-good-at-password-cracking/
tags:
- veille-cyber
- bleepingcomp
---
### L'inefficacité des GPU spécialisés IA pour le cassage de mots de passe

L'idée que les puissants accélérateurs d'IA (type Nvidia H200 ou AMD MI300X) pourraient révolutionner le cassage de mots de passe par force brute est un mythe. Les tests comparatifs montrent que ces équipements, bien que coûteux, sont moins performants que les cartes graphiques grand public comme la Nvidia RTX 5090 pour des tâches de hachage. Les outils de cracking actuels, utilisant des architectures optimisées pour le calcul parallèle général, ne tirent aucun avantage significatif de l'architecture spécifique aux modèles de langage (LLM).

**Points clés :**
* **Inutilité des GPU IA :** Le rapport prix/performance pour le cassage de mots de passe est très défavorable aux accélérateurs professionnels. Une RTX 5090 surpasse le H200 à une fraction du prix.
* **Stagnation technologique :** La puissance de calcul disponible aujourd'hui pour le cracking n'est pas fondamentalement supérieure aux capacités déjà accessibles via des rigs grand public il y a près d'une décennie.
* **Risque réel :** Le danger ne vient pas de la puissance de calcul brute, mais de la réutilisation de mots de passe ayant fuité lors de violations de données antérieures.

**Vulnérabilités :**
* L'utilisation d'algorithmes de hachage obsolètes ou rapides (MD5, NTLM).
* La faiblesse de la complexité et de la longueur des mots de passe.
* La réutilisation de mots de passe entre comptes personnels et professionnels (exposant l'organisation à des intrusions via des identifiants compromis).

**Recommandations :**
* **Privilégier la longueur :** La longueur est la défense la plus efficace. Une augmentation du nombre de caractères rend le cassage par force brute statistiquement impossible sur le plan temporel (ex: 15 caractères).
* **Détection de compromission :** Implémenter des solutions scannant en continu l'Active Directory pour comparer les mots de passe des utilisateurs aux bases de données de mots de passe connus comme compromis.
* **Gestion des politiques :** Appliquer des politiques de mots de passe granulaires imposant des passphrases.
* **Défense en profondeur :** Généraliser l'authentification multifacteur (MFA) pour sécuriser les accès (Windows, RDP, VPN), rendant le vol de mot de passe seul insuffisant pour un attaquant.

---
[Source](https://www.bleepingcomputer.com/news/security/is-a-30-000-gpu-good-at-password-cracking/){:target="_blank"}
