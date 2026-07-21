---
title: 'Anubis ransomware claims Coca-Cola Fairlife attack, threatens data leak'
date: 2026-07-21
permalink: /posts/2026/07/21/anubis-ransomware-claims-coca-cola-fairlife-attack-threatens-data-leak/
tags:
- veille-cyber
- bleepingcomp
---
### Attaque par ransomware Anubis contre la filiale Fairlife de Coca-Cola

Le groupe de cybercriminels Anubis a revendiqué une attaque par ransomware ayant paralysé les systèmes de production de Fairlife, filiale laitière de Coca-Cola, aux États-Unis. Les attaquants affirment avoir exfiltré près d'un téraoctet de données corporatives et menacent de les divulguer si une rançon n'est pas versée.

**Points clés :**
* **Nature de l'attaque :** Chiffrement de l'infrastructure Nutanix de Fairlife et vol présumé de 1 To de données.
* **Impact opérationnel :** Suspension temporaire de la production aux États-Unis, bien que la sécurité des produits ait été confirmée comme intacte.
* **Chronologie :** L'intrusion a eu lieu environ une semaine avant la divulgation publique par l'entreprise le 16 juillet.
* **Mode opératoire :** Le groupe Anubis, actif depuis décembre 2024, utilise un modèle de *Ransomware-as-a-Service* (RaaS) combinant double extorsion (vol de données et chiffrement) et dispose potentiellement d'outils de type « wiper » pour détruire irrémédiablement les fichiers.

**Vulnérabilités :**
* Aucune CVE spécifique n'a été identifiée ou rendue publique dans le cadre de cet incident. L'attaque semble cibler les vulnérabilités de l'infrastructure Nutanix.

**Recommandations :**
* **Renforcement de l'infrastructure Nutanix :** Appliquer immédiatement les correctifs de sécurité fournis par l'éditeur et auditer les vecteurs d'accès aux systèmes critiques.
* **Plan de continuité :** Maintenir et tester régulièrement des sauvegardes hors ligne, immuables, pour garantir une restauration sans dépendre des clés des attaquants.
* **Surveillance proactive :** Déployer des solutions de détection et de réponse (EDR/XDR) pour identifier les mouvements latéraux et les exfiltrations de données massives avant que le chiffrement ne soit déclenché.
* **Gestion des accès :** Imposer une authentification multifacteur (MFA) rigoureuse et le principe du moindre privilège sur l'ensemble du réseau, notamment sur les environnements de production.

---
[Source](https://www.bleepingcomputer.com/news/security/anubis-ransomware-claims-coca-cola-fairlife-attack-threatens-data-leak/){:target="_blank"}
