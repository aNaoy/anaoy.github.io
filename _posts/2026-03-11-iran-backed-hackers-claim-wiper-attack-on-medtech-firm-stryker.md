---
title: 'Iran-Backed Hackers Claim Wiper Attack on Medtech Firm Stryker'
date: 2026-03-11
permalink: /posts/2026/03/11/iran-backed-hackers-claim-wiper-attack-on-medtech-firm-stryker/
tags:
- veille-cyber
- krebs
---
### Cyberattaque destructrice contre le géant médical Stryker

Le groupe de hacktivistes **Handala**, lié aux services de renseignement iraniens (MOIS) et affilié à l'entité *Void Manticore*, a revendiqué une cyberattaque par effacement de données (*wiper*) visant l'entreprise de technologie médicale Stryker. L'attaque a entraîné la paralysie des systèmes informatiques mondiaux de la société, forçant la fermeture de sites et affectant les capacités d'approvisionnement hospitalier.

**Points clés :**
*   **Mode opératoire :** Contrairement à un logiciel malveillant classique, les assaillants auraient détourné **Microsoft Intune** pour envoyer une commande d'effacement à distance à plus de 200 000 serveurs et appareils mobiles connectés.
*   **Impact opérationnel :** Interruption majeure des activités dans 79 pays, appareils personnels et professionnels réinitialisés, et sites web internes défacés.
*   **Motivation :** Les attaquants présentent cette opération comme une mesure de rétorsion contre une frappe militaire américaine ayant touché une école en Iran.
*   **Vulnérabilité :** L'incident souligne le risque critique lié à l'utilisation d'outils de gestion de flotte (MDM) tels que Microsoft Intune. Si les accès administrateurs sont compromis, ces outils deviennent des armes de destruction massive permettant de paralyser instantanément une organisation.
*   **CVE :** Aucune CVE spécifique n'est mentionnée, l'incident relevant d'une compromission de compte et d'un détournement de fonctionnalités légitimes plutôt que de l'exploitation d'une faille logicielle.

**Recommandations :**
*   **Sécurisation des accès :** Appliquer une authentification multifacteur (MFA) renforcée et une politique de moindre privilège pour tous les comptes disposant d'accès administratifs sur les outils de gestion de flotte (Intune, MDM).
*   **Surveillance des logs :** Surveiller étroitement les activités inhabituelles au sein des consoles d'administration cloud et alerter sur les déploiements de politiques de suppression de masse.
*   **Plan de continuité :** Maintenir des sauvegardes immuables et hors ligne, et préparer des procédures d'urgence pour le maintien des activités critiques en cas de perte totale de l'infrastructure informatique.
*   **Hygiène informatique :** Limiter l'accès aux services de gestion d'entreprise sur les appareils personnels et renforcer la segmentation réseau pour empêcher la propagation d'une attaque à l'ensemble du parc informatique.

---
[Source](https://krebsonsecurity.com/2026/03/iran-backed-hackers-claim-wiper-attack-on-medtech-firm-stryker/){:target="_blank"}
