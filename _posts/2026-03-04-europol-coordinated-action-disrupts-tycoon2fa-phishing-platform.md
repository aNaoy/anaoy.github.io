---
title: 'Europol-coordinated action disrupts Tycoon2FA phishing platform'
date: 2026-03-04
permalink: /posts/2026/03/04/europol-coordinated-action-disrupts-tycoon2fa-phishing-platform/
tags:
- veille-cyber
- bleepingcomp
---
### Démantèlement d'une Plateforme de Phishing Avancée

Une opération internationale coordonnée par Europol a permis de neutraliser Tycoon2FA, une plateforme majeure de "phishing-as-a-service" (PhaaS) qui générait mensuellement des dizaines de millions d'e-mails d'hameçonnage. L'action a abouti à la saisie et à la mise hors ligne de 330 domaines constituant l'infrastructure de cette plateforme criminelle.

Cette opération, soutenue par des partenaires privés tels que Microsoft et Trend Micro, ainsi que par les forces de l'ordre de plusieurs pays européens, visait à déjouer les attaques sophistiquées de Tycoon2FA. La plateforme, active depuis au moins août 2023, était conçue pour contourner les protections d'authentification multifacteur (MFA) et compromettre les comptes de près de 100 000 organisations dans le monde, y compris des institutions gouvernementales, des écoles et des établissements de santé.

Microsoft a indiqué que mi-2025, Tycoon2FA était responsable de 60% de toutes les tentatives de phishing bloquées, touchant plus de 500 000 organisations.

**Points clés :**

*   **Nature de la menace :** Tycoon2FA opérait comme une plateforme "adversary-in-the-middle" (AITM), utilisant des serveurs proxy inversés pour intercepter en temps réel les identifiants de connexion et les cookies de session des victimes.
*   **Mécanisme d'attaque :** Elle permettait de voler les informations d'authentification et les codes MFA, tout en interceptant les cookies de session, autorisant ainsi le détournement de sessions authentifiées et le contournement de la MFA.
*   **Ciblage :** Les attaques visaient principalement les clients de Microsoft et Google, en imitant des pages de connexion de services populaires tels que Microsoft 365, OneDrive, Outlook, SharePoint et Gmail.
*   **Accessibilité :** La plateforme était vendue via Telegram à un coût relativement bas ($120 pour 10 jours), abaissant ainsi le seuil d'accès pour des cybercriminels moins expérimentés afin de mener des attaques à grande échelle.
*   **Persistance :** Tycoon2FA permettait aux attaquants d'établir une persistance et d'accéder à des informations sensibles même après la réinitialisation des mots de passe, sauf si les sessions et les jetons actifs étaient explicitement révoqués.

**Vulnérabilités exploitées :**

Bien qu'aucun identifiant CVE spécifique ne soit mentionné directement dans l'article pour la plateforme elle-même, le mécanisme d'exploitation repose sur la manipulation du processus d'authentification standard pour intercepter des informations sensibles et des cookies de session. L'exploitation de la confiance accordée aux pages de connexion légitimes et la capacité à relayer les codes MFA contribuent à la réussite de ces attaques.

**Recommandations :**

*   **Révocation des sessions actives :** La suppression des sessions authentifiées et des jetons actifs est cruciale pour contrer ce type d'attaques, même après une réinitialisation de mot de passe.
*   **Vigilance accrue :** Les utilisateurs doivent être particulièrement attentifs aux tentatives de phishing, même celles qui semblent légitimes et réussissent à passer les premières étapes d'authentification.
*   **Mise à jour des mesures de sécurité :** Les organisations doivent continuer à renforcer leurs défenses contre le phishing et les techniques de contournement de la MFA.

---
[Source](https://www.bleepingcomputer.com/news/security/europol-coordinated-action-disrupts-tycoon2fa-phishing-platform/){:target="_blank"}
