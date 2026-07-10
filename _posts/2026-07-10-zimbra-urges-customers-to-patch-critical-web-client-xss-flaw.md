---
title: 'Zimbra urges customers to patch critical web client XSS flaw'
date: 2026-07-10
permalink: /posts/2026/07/10/zimbra-urges-customers-to-patch-critical-web-client-xss-flaw/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilité critique dans l'interface Classic Web Client de Zimbra

Zimbra a publié une mise à jour de sécurité pour corriger une faille de type Cross-Site Scripting (XSS) stocké au sein de son interface « Classic Web Client ». Bien que cette vulnérabilité ne dispose pas encore d'identifiant CVE, elle est jugée critique car elle permet à des attaquants d'exécuter du code malveillant via des emails spécialement conçus.

**Points clés :**
*   **Risques :** L'exploitation de cette faille peut mener au vol de données de session, de paramètres de compte et d'informations contenues dans les boîtes mail.
*   **Contexte :** La vulnérabilité a été signalée par le *Threat Analysis Group* de Google, une entité qui identifie régulièrement des attaques menées par des groupes étatiques visant des cibles à haut risque (journalistes, diplomates, gouvernements).
*   **Historique :** Les solutions Zimbra sont une cible privilégiée des groupes de hackers russes (notamment APT29 et APT28), qui exploitent fréquemment les failles XSS pour infiltrer des serveurs à grande échelle.

**Vulnérabilités :**
*   **Type :** XSS (Cross-Site Scripting) stocké dans le « Classic Web Client ».
*   **CVE :** Non attribué à ce jour.

**Recommandations :**
*   **Mise à jour immédiate :** Tous les clients utilisant le « Classic Web Client » doivent impérativement installer la version **ZCS v10.1.19**.
*   **Sécurisation :** Appliquer ce correctif sans délai pour prévenir toute compromission de l'environnement, les vecteurs d'attaque sur ce type de logiciel étant activement surveillés par des groupes de cyberespionnage.

---
[Source](https://www.bleepingcomputer.com/news/security/zimbra-urges-customers-to-patch-critical-web-client-xss-flaw/){:target="_blank"}
