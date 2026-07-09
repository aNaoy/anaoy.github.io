---
title: 'Fake 7-Zip Installers Turn Devices Into Residential Proxy Nodes'
date: 2026-07-09
permalink: /posts/2026/07/09/fake-7-zip-installers-turn-devices-into-residential-proxy-nodes/
tags:
- veille-cyber
- hackernews
---
### Lurking Lizard : Un réseau mondial de proxys résidentiels malveillants

Le groupe cybercriminel « Lurking Lizard », identifié comme opérant depuis la Chine, orchestre une vaste infrastructure de proxys résidentiels illégaux en transformant les appareils de victimes en nœuds de sortie. Actif depuis août 2022, ce réseau utilise plus de 230 domaines frauduleux et des techniques de marketing sophistiquées pour monétiser les connexions IP des utilisateurs à leur insu.

**Points clés :**
* **Modus Operandi :** Le groupe utilise le « drop-catching » (rachat de domaines expirés) et le cybersquatting (ex: `7zip[.]com`) pour diffuser des installateurs piégés (7-Zip, WireVPN, outils de téléchargement TikTok/YouTube).
* **Écosystème complet :** Lurking Lizard contrôle toute la chaîne, du recrutement des appareils via des logiciels malveillants à la vente d'accès proxy sous de fausses enseignes (usurpant l'identité de fournisseurs légitimes comme IPIDEA ou SmartProxy), soutenus par de faux sites d'avis.
* **Impact multi-plateforme :** La menace touche Windows, macOS et Android. Une application mobile suspecte, « wirevpn », a déjà été téléchargée plus d'un million de fois.
* **Risques pour les victimes :** Les utilisateurs deviennent des relais pour des activités malveillantes, ce qui peut entraîner le blocage de leur adresse IP par les fournisseurs d'accès ou les services en ligne.

**Vulnérabilités :**
* Aucune CVE spécifique n'est mentionnée, car l'attaque repose sur l'**ingénierie sociale** et le téléchargement de logiciels contrefaits (trojanisés) plutôt que sur l'exploitation de failles techniques logicielles.

**Recommandations :**
* **Vérification des sources :** Téléchargez uniquement les logiciels sur les sites officiels des éditeurs (ex: `7-zip.org` et non `7zip.com`).
* **Scepticisme face aux outils gratuits :** Méfiez-vous des applications de VPN ou d'utilitaires "gratuits" dont le modèle économique n'est pas transparent, particulièrement sur les stores mobiles.
* **Vigilance DNS :** Soyez attentif aux erreurs de saisie dans les noms de domaine (typosquatting).
* **Hygiène numérique :** Utilisez des solutions de sécurité capables de détecter les comportements de botnet et les connexions vers des domaines malveillants connus.

---
[Source](https://thehackernews.com/2026/07/fake-7-zip-installers-turn-devices-into.html){:target="_blank"}
