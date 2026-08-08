---
title: 'N-able Issues N-central Hotfix 2 as Attackers Reach Managed Systems and Persist'
date: 2026-08-08
permalink: /posts/2026/08/08/n-able-issues-n-central-hotfix-2-as-attackers-reach-managed-systems-and-persist/
tags:
- veille-cyber
- hackernews
---
### Sécurisation critique de N-able N-central : Hotfix 2 obligatoire

N-able a publié un correctif d'urgence (Hotfix 2) pour son logiciel N-central afin de contrer l'exploitation active d'une vulnérabilité critique. Cette mise à jour est indispensable, même pour les clients ayant déjà appliqué le premier correctif, car elle renforce les mesures de protection contre des attaquants cherchant à maintenir une persistance sur les systèmes gérés.

**Points clés :**
* **Nature de l'attaque :** Les attaquants exploitent une faille pour obtenir un accès administrateur, puis utilisent la fonction "Take Control" pour compromettre les appareils gérés.
* **Méthode de persistance :** Une fois l'accès obtenu, les attaquants enregistrent un service via "Cloudflare Tunnel" pour conserver leur accès même après la sécurisation du serveur N-central.
* **État de la menace :** CISA a confirmé que ces vulnérabilités font l'objet d'une exploitation active.

**Vulnérabilités :**
* **CVE-2026-18577 (Score CVSS : 8.2) :** Permet le contournement de l'authentification et la prise de contrôle de compte. Il s'agit d'un correctif incomplet pour la **CVE-2026-18556**.

**Recommandations :**
* **Mise à jour immédiate :** Les déploiements sur site doivent impérativement être mis à jour vers la version **2026.3.1.10**.
* **Détection :** Utiliser le modèle de service personnalisé fourni par N-able pour scanner les terminaux Windows à la recherche d'indicateurs de compromission (IoC).
* **Vigilance :** Une analyse des journaux, des activités de comptes et de l'environnement est recommandée, car l'absence d'IoC détectés ne garantit pas l'absence d'intrusion.
* **Surveillance :** Surveiller les communications réseau liées aux adresses IP suspectes identifiées dans l'article (ex: 173.249.252.176, 185.156.46.150, etc.).

---
[Source](https://thehackernews.com/2026/08/n-central-attackers-reach-managed.html){:target="_blank"}
