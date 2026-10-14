---
title: 'OpenAI engineer arrested for allegedly planting spy device in office'
date: 2026-10-14
permalink: /posts/2026/10/14/openai-engineer-arrested-for-allegedly-planting-spy-device-in-office/
tags:
- veille-cyber
- bleepingcomp
---
### Espionnage interne chez OpenAI : Arrestation d'un ingénieur

Un ingénieur d'OpenAI, Abdulrahman Alfozan, a été arrêté et inculpé par le département de la Justice des États-Unis pour avoir dissimulé des dispositifs d'enregistrement audio dans les salles de conférence de l'entreprise à San Francisco. L'individu, en poste depuis juillet 2025, cherchait à intercepter des conversations confidentielles portant sur la recherche, les plans de produits et les relations stratégiques de la firme.

**Points clés :**
* **Détection :** La sécurité d'OpenAI a découvert le premier dispositif connecté à un port USB derrière une télévision le 30 septembre. Un second appareil a été retrouvé dans un sac appartenant au suspect le 5 octobre.
* **Preuves :** Des images de vidéosurveillance ont placé l'ingénieur à proximité des salles concernées. De plus, son historique de recherche (via un chatbot lié à son épouse) révélait des requêtes sur la fabrication de dispositifs d'écoute et le chiffrement de données.
* **Réaction :** OpenAI a utilisé ses propres modèles d'IA pour analyser les dispositifs et identifier le responsable. L'employé a été licencié et le FBI a été saisi de l'affaire.
* **Impact :** Aucune preuve d'exfiltration de code source, de poids de modèles ou de données clients n'a été constatée à ce stade.

**Vulnérabilités :**
* Il n'existe pas de CVE spécifique, car il s'agit d'une menace physique (insider threat) plutôt que numérique. La faille réside dans l'accès physique non contrôlé aux ports USB des équipements de visioconférence.

**Recommandations :**
* **Sécurisation physique :** Bloquer physiquement ou désactiver les ports USB inutilisés sur tous les appareils dans les salles de réunion confidentielles.
* **Surveillance d'accès :** Restreindre et auditer strictement l'accès aux salles de conférence exécutives par badge et caméra.
* **Détection comportementale :** Surveiller les accès anormaux aux systèmes d'information internes (recherches sur les plans de bureaux ou horaires de réunions par des employés non concernés).
* **Politique d'entreprise :** Appliquer une politique stricte de sécurité physique pour prévenir l'introduction de matériel non autorisé (dispositifs "espions" matériels).

---
[Source](https://www.bleepingcomputer.com/news/artificial-intelligence/openai-engineer-arrested-for-allegedly-planting-spy-device-in-office/){:target="_blank"}
