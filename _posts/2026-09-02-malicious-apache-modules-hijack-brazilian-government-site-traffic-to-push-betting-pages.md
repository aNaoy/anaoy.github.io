---
title: 'Malicious Apache Modules Hijack Brazilian Government Site Traffic to Push Betting Pages'
date: 2026-09-02
permalink: /posts/2026/09/02/malicious-apache-modules-hijack-brazilian-government-site-traffic-to-push-betting-pages/
tags:
- veille-cyber
- hackernews
---
### Détournement de serveurs gouvernementaux brésiliens à des fins de SEO malveillant

Le groupe cybercriminel « Gambling Goblin », probablement lié au collectif Earth Berberoka, exploite des serveurs web compromis — notamment des portails gouvernementaux et éducatifs brésiliens (.gov.br, .jus.br) — pour mener des campagnes de manipulation SEO à grande échelle. L'objectif est de rediriger le trafic vers des sites de paris sportifs et de jeux d'argent illégitimes.

**Points clés** :
*   **Technique d'attaque** : Installation de modules Apache malveillants agissant comme des « reverse-proxies » qui redirigent les utilisateurs vers des pages de phishing tout en conservant l'apparence de légitimité du domaine initial.
*   **Objectif** : Gonfler artificiellement le classement des moteurs de recherche (SEO) des sites de jeux en exploitant la haute réputation des domaines gouvernementaux.
*   **Risque accru** : Les pages frauduleuses imitent des boutiques d'applications (Google Play, Amazon), créant un vecteur potentiel pour la distribution massive de logiciels malveillants.
*   **Infrastructure associée** : Les attaquants déploient des outils avancés, notamment des backdoors (AlphaAgent, oRAT), des outils de vol d'identifiants (basés sur 3snake) et des scanneurs de réseau.

**Vulnérabilités et vecteurs** :
*   Aucune CVE spécifique n'est mentionnée, car l'attaque repose sur l'injection directe de modules serveurs malveillants sur des systèmes dont l'accès initial n'est pas encore documenté.
*   Utilisation du binaire **3snake** pour intercepter les authentifications sur les processus SSH et sudo.
*   Le déploiement de modules malveillants, similaires au logiciel *Gamshen* observé précédemment sur les serveurs IIS, permet aux attaquants de masquer leurs activités en ne répondant qu'aux robots des moteurs de recherche (cloaking).

**Recommandations** :
*   **Audit d'intégrité** : Vérifier régulièrement la liste des modules Apache chargés sur les serveurs Linux pour détecter toute extension non autorisée ou suspecte.
*   **Surveillance des logs** : Surveiller les processus système suspects liés à `ptrace` ou à des injections dans `sshd` et `sudo`.
*   **Gestion des accès** : Renforcer la sécurité des accès distants (SSH) et restreindre les privilèges d'exécution sur les serveurs hébergeant des services publics.
*   **Réponse aux incidents** : En cas de compromission, isoler les serveurs gouvernementaux sans bloquer globalement les domaines, afin de maintenir la continuité des services publics tout en traitant l'infrastructure malveillante séparément.

---
[Source](https://thehackernews.com/2026/09/malicious-apache-modules-hijack.html){:target="_blank"}
