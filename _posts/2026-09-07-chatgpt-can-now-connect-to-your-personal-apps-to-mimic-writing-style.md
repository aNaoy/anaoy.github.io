---
title: 'ChatGPT can now connect to your personal apps to mimic writing style'
date: 2026-09-07
permalink: /posts/2026/09/07/chatgpt-can-now-connect-to-your-personal-apps-to-mimic-writing-style/
tags:
- veille-cyber
- bleepingcomp
---
### Personnalisation de ChatGPT par l'intégration de données personnelles

OpenAI teste actuellement une nouvelle fonctionnalité permettant à ChatGPT d'adopter le style rédactionnel spécifique d'un utilisateur en analysant ses données provenant d'applications tierces connectées (Slack, Google Drive, Notion, Gmail). Contrairement aux méthodes manuelles, cette approche automatise l'apprentissage du ton et de la structure de l'utilisateur à travers ses messages, documents et courriels.

**Points clés**
* **Automatisation du style :** ChatGPT ajuste son écriture en temps réel en consultant les communications réelles de l'utilisateur.
* **Large périmètre de données :** L'accès direct aux services tiers permet d'analyser des contextes variés, allant de l'instantanéité des messageries à la formalité des documents longs.
* **Phase de test :** La fonctionnalité est en cours de déploiement limité pour évaluation avant une éventuelle généralisation.

**Vulnérabilités et risques**
* **Risque de confidentialité :** L'autorisation accordée à l'IA d'accéder à des documents confidentiels et des échanges privés augmente la surface d'exposition en cas de fuite de données ou de compromission du compte utilisateur.
* **Usurpation d'identité :** Si un compte est compromis, un attaquant pourrait exploiter cette fonctionnalité pour générer des contenus frauduleux (phishing, ingénierie sociale) imitant parfaitement le style de la victime, rendant la détection beaucoup plus difficile.
* *Note : Aucune CVE spécifique n'est associée, car il s'agit d'une évolution fonctionnelle et non d'une faille logicielle connue.*

**Recommandations**
* **Gestion des permissions :** Restreindre strictement les accès accordés aux applications tierces et auditer régulièrement les outils connectés à votre compte OpenAI.
* **Sensibilisation à l'ingénierie sociale :** Rester vigilant face aux messages provenant de collègues ou proches, même si le ton semble naturel, car l'IA peut désormais reproduire fidèlement des styles de communication personnels.
* **Principe du moindre privilège :** Ne connecter à ChatGPT que les services ne contenant pas de données hautement sensibles ou confidentielles.

---
[Source](https://www.bleepingcomputer.com/news/artificial-intelligence/chatgpt-can-now-connect-to-your-personal-apps-to-mimic-writing-style/){:target="_blank"}
