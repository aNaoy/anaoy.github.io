---
title: 'Phishing service spoofs RingCentral to steal Microsoft 365 accounts'
date: 2026-08-05
permalink: /posts/2026/08/05/phishing-service-spoofs-ringcentral-to-steal-microsoft-365-accounts/
tags:
- veille-cyber
- bleepingcomp
---
### La plateforme "Greatness" exploite RingCentral pour détourner des comptes Microsoft 365

La plateforme de phishing-as-a-service (PhaaS) « Greatness » a fait évoluer ses méthodes en usurpant l'identité de RingCentral pour contourner les filtres de sécurité et compromettre des comptes Microsoft 365. Vendue 289 $ par mois, cette infrastructure permet désormais des attaques par intermédiaire (AiTM) et par code d'appareil, tout en tirant parti d'une liste de cibles potentiellement issues d'une récente violation de données chez RingCentral.

**Points clés :**
* **Vecteur d'attaque :** Utilisation d'e-mails frauduleux imitant des notifications de messagerie vocale ou d'évaluation de performance RingCentral.
* **Contournement des filtres :** Bien que les e-mails échouent aux tests SPF, DKIM et DMARC, ils sont acceptés par les systèmes de réception car RingCentral est présent sur des listes d'expéditeurs approuvés (*whitelisting*).
* **Techniques de vol :** Utilisation de l'AiTM pour intercepter les jetons d'authentification MFA ou déploiement de flux de phishing par code d'appareil.
* **Persistance :** Une fois le compte compromis, les attaquants utilisent Microsoft Graph pour accéder durablement à Outlook, Teams, SharePoint et OneDrive.

**Vulnérabilités exploitées :**
* Aucune CVE spécifique n'est mentionnée, mais l'attaque repose sur une **faille logique liée à l'exclusion automatique des domaines de confiance** (whitelisting excessif) dans les passerelles de messagerie.

**Recommandations :**
* **Révision des listes blanches :** Auditer les listes d'expéditeurs autorisés et remplacer les exclusions globales par des règles exigeant une authentification e-mail stricte (SPF/DKIM/DMARC obligatoires).
* **Détection proactive :** Surveiller les connexions Microsoft 365 validées par MFA provenant d'adresses IP suspectes (VPN ou hébergeurs).
* **Réponse à incident :** En cas de compromission, révoquer immédiatement tous les jetons d'accès et de rafraîchissement, et examiner les autorisations OAuth ainsi que les logs d'activité Microsoft Graph.

---
[Source](https://www.bleepingcomputer.com/news/security/phishing-service-spoofs-ringcentral-to-steal-microsoft-365-accounts/){:target="_blank"}
