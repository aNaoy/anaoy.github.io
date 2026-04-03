---
title: 'TeamPCP Supply Chain Campaign: Update 006 - CERT-EU Confirms European Commission Cloud Breach, Sportradar Details Emerge, and Mandiant Quantifies Campaign at 1,000&#x2b; SaaS Environments, (Fri, Apr 3rd)'
date: 2026-04-03
permalink: /posts/2026/04/03/teampcp-supply-chain-campaign-update-006-cert-eu-confirms-european-commission-cloud-breach-sportradar-details-emerge-and-mandiant-quantifies-campaign-at-1000x2b-saas-environments-fri-apr-3rd/
tags:
- veille-cyber
- sans-isc
---
### État des lieux de la campagne de cyberattaques TeamPCP

La campagne de compromission de la chaîne d'approvisionnement (supply chain) menée par le groupe TeamPCP a atteint une ampleur critique. Les autorités confirment désormais l'impact sur des institutions gouvernementales majeures et une propagation massive touchant plus de 1 000 environnements SaaS et environ 500 000 machines.

#### Points clés
* **Violation à la Commission européenne :** CERT-EU a confirmé une intrusion sur la plateforme d'hébergement "Europa" via des clés API AWS volées par le scanner Trivy. Environ 340 Go de données ont été exfiltrés, impactant 71 entités, dont 30 organismes de l'Union européenne.
* **Opération conjointe TeamPCP/Vect :** Le piratage de Sportradar AG est confirmé comme une opération hybride entre le groupe TeamPCP et le ransomware Vect (CipherForce), exposant les données de 26 000 utilisateurs et des informations sensibles sur 161 clients (dont Nike, NBA, ESPN).
* **Étendue massive :** Mandiant estime que les secrets volés circulent au sein de 1 000 environnements SaaS. La technique utilise des outils de tunneling (frps, gost) et des failles type "React2Shell" pour persister dans les conteneurs.
* **Volet judiciaire :** Une action collective est en cours contre Mercor AI suite à la fuite de données biométriques et professionnelles, impliquant des clients majeurs comme OpenAI, Anthropic et Meta.

#### Vulnérabilités identifiées
* **CVE-2026-33634 :** Compromission de la chaîne d'approvisionnement via le scanner **Trivy**, point d'entrée initial de la majorité des attaques documentées.

#### Recommandations
* **Mise à jour d'urgence :** Les organisations utilisant Trivy doivent impérativement appliquer les correctifs (version 0.69.2+ pour Trivy, v0.35.0 pour trivy-action, ou v0.2.6 pour setup-trivy) avant la date limite CISA du 8 avril 2026.
* **Rotation des identifiants :** Toute organisation dont les clés AWS ou autres identifiants ont pu être exposés via l'utilisation de Trivy doit procéder immédiatement à une rotation complète des secrets.
* **Surveillance des conteneurs :** Les équipes SOC sont invitées à s'appuyer sur le guide de détection publié par *Elastic Security Labs* pour identifier les indicateurs de compromission (IOC) liés aux outils `frps` et `gost`.
* **Analyse d'exposition :** Les entreprises ayant des relations commerciales avec Sportradar ou les autres victimes identifiées doivent vérifier si leurs données figurent parmi les informations exfiltrées pour prévenir des attaques secondaires.

---
[Source](https://isc.sans.edu/diary/rss/32864){:target="_blank"}
