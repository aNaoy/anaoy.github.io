---
title: 'N-able Says Attackers Take Over N-central Servers After Initial Fix Proves Incomplete'
date: 2026-08-03
permalink: /posts/2026/08/03/n-able-says-attackers-take-over-n-central-servers-after-initial-fix-proves-incomplete/
tags:
- veille-cyber
- hackernews
---
### Compromission des serveurs N-central : Vulnérabilités persistantes et maintien d'accès

Des attaquants ont exploité une vulnérabilité de contournement d'authentification dans la plateforme de gestion N-central de N-able pour prendre le contrôle administratif de serveurs et accéder aux systèmes clients gérés. La première correction apportée par l'éditeur s'est révélée incomplète, permettant aux attaquants de maintenir une persistance sur les terminaux via des tunnels Cloudflare, même après la mise à jour des serveurs.

**Points clés :**
*   **Technique de persistance :** Les attaquants ont utilisé l'outil « Take Control » pour installer des tunnels Cloudflare sous forme de services sur les terminaux, contournant ainsi le besoin d'ouverture de ports entrants et conservant un accès après la correction du serveur.
*   **Indicateurs de compromission :** Présence de `svchost.exe` dans les dossiers « Documents » des utilisateurs, service nommé « Cloudflared », et trafic lié à des adresses IP suspectes ou à des domaines de type *QuickConnect/Synology*.
*   **Scope :** La portée exacte de l'attaque et le nombre d'organisations touchées restent indéterminés.

**Vulnérabilités :**
*   **CVE-2026-18556 :** Contournement de l'authentification (CWE-288) affectant les versions 2026.1 et antérieures.
*   **CVE-2026-18577 :** Variante d'exploitation contournant le premier correctif. Affecte toutes les versions antérieures à la **2026.3.1.7**.

**Recommandations :**
*   **Mise à jour urgente :** Déployer impérativement la version **2026.3.1.7**.
*   **Nettoyage post-compromission :** La mise à jour du serveur ne supprime pas les services malveillants installés sur les terminaux. Une recherche manuelle et une suppression des services « Cloudflared » sur chaque poste géré sont indispensables.
*   **Audit des logs :** Analyser les logs `ui_access_control.log` et `BASupSrvc_*.log.gz` pour détecter des sessions « Take Control » suspectes.
*   **Surveillance :** Surveiller les connexions sortantes vers les adresses IP suspectes (ex: 173.249.252.200, 87.249.138.34, etc.) et vérifier les identités de support inhabituelles (ex: `mspsupport@n-able.com`).

---
[Source](https://thehackernews.com/2026/08/n-able-says-attackers-take-over-n.html){:target="_blank"}
