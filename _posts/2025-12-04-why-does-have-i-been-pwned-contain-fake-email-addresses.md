---
title: 'Why Does Have I Been Pwned Contain "Fake" Email Addresses?'
date: 2025-12-04
permalink: /posts/2025/12/04/why-does-have-i-been-pwned-contain-fake-email-addresses/
tags:
- veille-cyber
- troyhunt
---
## Comprendre les "fausses" adresses e-mail dans Have I Been Pwned

Le service Have I Been Pwned (HIBP) enregistre les adresses e-mail exposées lors de fuites de données. La confusion concernant la présence d'adresses e-mail "fausses" ou non réelles dans la base de données provient d'une incompréhension de la manière dont ces adresses sont collectées et validées.

**Points clés :**

*   **Extraction des adresses e-mail :** HIBP utilise un outil automatisé pour extraire les adresses e-mail des fichiers de données provenant de fuites. Cet outil se base sur des critères structurels simples : présence d'un "@", longueur des alias et domaines, existence d'un point dans le domaine, et conformité avec les TLD (Top-Level Domains) valides.
*   **Absence de vérification d'existence de boîte aux lettres :** Il est techniquement impossible de vérifier l'existence réelle de chaque adresse e-mail collectée, compte tenu du volume colossal (milliards). Par conséquent, toute chaîne de caractères respectant la structure d'une adresse e-mail valide est considérée comme telle.
*   **Origine des adresses "fausses" :** Ces adresses peuvent apparaître dans des sites web réels pour plusieurs raisons. Par exemple, lors de l'inscription à un service, une adresse e-mail valide structurellement peut être saisie, même si elle n'est pas vérifiée par l'envoi d'un e-mail de confirmation. Si ce service subit une fuite, cette adresse, même non validée ou potentiellement erronée, se retrouve dans les données. Des adresses "placeholder" comme `test@example.com` ou des adresses créées pour des tests peuvent également être utilisées et ensuite exposées.
*   **Vérification par génération :** Les adresses e-mail générées aléatoirement et qui n'ont jamais été utilisées pour s'inscrire à un service ne peuvent pas apparaître dans HIBP, car elles n'auraient pas été exposées lors d'une fuite de données.

**Vulnérabilités :**

Aucune vulnérabilité spécifique avec des identifiants CVE n'est mentionnée dans cet article. La problématique concerne plutôt le processus de collecte et de traitement des données, et la manière dont les services tiers gèrent la validation des adresses e-mail.

**Recommandations :**

*   Pour les services en ligne : Implémenter une vérification plus robuste des adresses e-mail lors des inscriptions, idéalement par un système de confirmation via un lien envoyé à l'adresse fournie, et supprimer les adresses non vérifiées après un délai raisonnable.
*   Pour les utilisateurs : Être conscient que des adresses e-mail structurellement valides mais potentiellement non réelles peuvent apparaître dans des fuites de données.

---
[Source](https://www.troyhunt.com/why-does-have-i-been-pwned-contain-fake-email-addresses/){:target="_blank"}
