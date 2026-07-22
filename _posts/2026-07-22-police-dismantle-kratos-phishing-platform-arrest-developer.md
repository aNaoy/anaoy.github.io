---
title: 'Police dismantle Kratos phishing platform, arrest developer'
date: 2026-07-22
permalink: /posts/2026/07/22/police-dismantle-kratos-phishing-platform-arrest-developer/
tags:
- veille-cyber
- bleepingcomp
---
### Démantèlement de la plateforme de phishing Kratos

Les autorités allemandes et américaines ont neutralisé l’infrastructure centrale de « Kratos », l’un des services de phishing-as-a-service (PhaaS) les plus utilisés mondialement, et arrêté son développeur en Indonésie lors de l’opération *Olympus Blade*.

**Points clés :**
* **Impact massif :** Plus de 1 800 cybercriminels utilisaient Kratos pour mener environ 15 000 campagnes de phishing par mois, touchant des victimes dans 35 pays.
* **Opération technique :** Saisie de plus de 200 serveurs et transfert des noms de domaine sous contrôle du FBI.
* **Modèle économique :** La plateforme générait des revenus via des abonnements, permettant aux attaquants de créer de fausses pages d’authentification Microsoft pour voler des identifiants.
* **Conséquences post-compromission :** Les comptes piratés étaient utilisés pour des compromissions d'emails professionnels (BEC), du vol de données et la propagation d'attaques supplémentaires.

**Vulnérabilités exploitées :**
L'article ne mentionne pas de CVE spécifique, car le service reposait sur l'ingénierie sociale (pages de connexion contrefaites) plutôt que sur l'exploitation directe de failles logicielles.

**Recommandations :**
* **Authentification multi-facteurs (MFA) :** Renforcer les accès aux comptes Microsoft avec des solutions MFA robustes (clés FIDO2 ou applications d'authentification) pour limiter l'impact des vols de mots de passe.
* **Veille et détection :** Utiliser des outils de simulation de brèches et d'attaques (BAS) pour tester l'efficacité des règles SIEM et EDR face aux techniques actuelles de phishing.
* **Formation :** Sensibiliser les utilisateurs aux tactiques de phishing ciblant spécifiquement les portails d'authentification Microsoft 365.
* **Réponse aux incidents :** Surveiller les accès anormaux après une compromission initiale, conformément au schéma de persistance identifié chez les victimes de Kratos.

---
[Source](https://www.bleepingcomputer.com/news/security/police-dismantle-kratos-phishing-platform-arrest-developer/){:target="_blank"}
