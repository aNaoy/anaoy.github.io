---
title: 'Poland busts SIM-swapping gang tied to millions in crypto theft'
date: 2026-06-26
permalink: /posts/2026/06/26/poland-busts-sim-swapping-gang-tied-to-millions-in-crypto-theft/
tags:
- veille-cyber
- bleepingcomp
---
### Démantèlement d'un réseau international de SIM-swapping en Pologne

La police polonaise (CBZC), en collaboration avec le FBI et le HSI américain, a arrêté quatre membres d'un groupe criminel organisé spécialisé dans le vol de cryptomonnaies par usurpation d'identité mobile (SIM-swapping). Le préjudice est estimé à plus de 5 millions de dollars.

**Points clés :**
* **Mode opératoire :** Les assaillants ont utilisé une combinaison d'ingénierie sociale et de logiciels spécialisés pour infiltrer les infrastructures des partenaires des opérateurs télécoms et compromettre des comptes de messagerie professionnels.
* **Technique de vol :** L'accès aux données des victimes a permis d'effectuer des transferts de numéros (SIM-swapping) pour intercepter les codes de double authentification (2FA) par SMS, facilitant ainsi la prise de contrôle de comptes sur des plateformes d'échange de cryptomonnaies.
* **Blanchiment :** Les fonds volés étaient transférés via un réseau financier distribué utilisant de multiples portefeuilles numériques et comptes bancaires internationaux.

**Vulnérabilités exploitées :**
* L'article ne mentionne pas de CVE spécifique, car les attaques reposaient sur l'exploitation humaine (ingénierie sociale) et l'accès non autorisé aux systèmes d'information tiers plutôt que sur une vulnérabilité logicielle logicielle identifiée.

**Recommandations :**
* **Renforcement de l'authentification :** Délaisser les méthodes d'authentification par SMS au profit de clés de sécurité matérielles (type FIDO2/YubiKey) ou d'applications d'authentification basées sur des jetons TOTP, qui ne peuvent pas être détournées par un SIM-swapping.
* **Sécurisation des accès tiers :** Appliquer le principe du moindre privilège aux partenaires et sous-traitants ayant accès aux infrastructures critiques des opérateurs télécoms.
* **Protection des comptes :** Sensibiliser les employés aux techniques d'ingénierie sociale et renforcer la surveillance des accès aux messageries professionnelles via des mécanismes de détection d'anomalies (EDR/SIEM).

---
[Source](https://www.bleepingcomputer.com/news/security/poland-busts-sim-swapping-gang-tied-to-millions-in-crypto-theft/){:target="_blank"}
