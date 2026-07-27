---
title: 'Coca-Cola confirms data theft in Fairlife ransomware attack'
date: 2026-07-27
permalink: /posts/2026/07/27/coca-cola-confirms-data-theft-in-fairlife-ransomware-attack/
tags:
- veille-cyber
- bleepingcomp
---
### Cyberattaque par ransomware contre Fairlife (filiale de Coca-Cola)

Coca-Cola a confirmé qu'une attaque par ransomware, revendiquée par le groupe « Anubis », a ciblé sa filiale laitière Fairlife, entraînant une interruption temporaire de la production aux États-Unis et le vol d'environ 1 téraoctet de données sensibles. Bien que la production ait repris, les cybercriminels ont mis à exécution leurs menaces en publiant les données dérobées après le refus de l'entreprise de négocier.

**Points clés :**
* **Vecteur d'attaque :** Chiffrement des systèmes Nutanix de l'entreprise par le groupe Anubis.
* **Conséquences opérationnelles :** Suspension temporaire de la production dans quatre usines américaines, partiellement compensée par les stocks existants.
* **Impact sur les données :** Vol confirmé d'environ 1 To de données, désormais accessibles publiquement suite à l'expiration de l'ultimatum des pirates.
* **Réponse de l'entreprise :** Signalement aux autorités compétentes et refus de payer la rançon.

**Vulnérabilités :**
* L'article ne mentionne pas de CVE spécifique, mais souligne une vulnérabilité critique au niveau de l'infrastructure de stockage Nutanix ayant permis aux attaquants de paralyser les opérations et d'exfiltrer les données.

**Recommandations :**
* **Sécurisation des systèmes critiques :** Renforcer la protection des environnements virtualisés (tels que Nutanix) par une segmentation réseau stricte et des accès restreints (Zero Trust).
* **Détection proactive :** Mettre en œuvre des solutions de simulation de brèche et d'attaque pour tester l'efficacité des règles SIEM et EDR afin de détecter les mouvements latéraux avant l'exfiltration.
* **Stratégie de sauvegarde :** Maintenir des sauvegardes immuables et hors ligne pour permettre une restauration rapide sans dépendre de la bonne volonté des attaquants.
* **Gestion de crise :** Préparer un plan de communication et de réponse incident robuste pour limiter les impacts opérationnels et réputationnels en cas de fuite de données avérée.

---
[Source](https://www.bleepingcomputer.com/news/security/coca-cola-confirms-data-theft-in-fairlife-ransomware-attack/){:target="_blank"}
