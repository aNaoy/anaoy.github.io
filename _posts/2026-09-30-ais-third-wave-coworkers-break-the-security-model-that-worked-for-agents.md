---
title: 'AIs Third Wave: Coworkers Break the Security Model That Worked for Agents'
date: 2026-09-30
permalink: /posts/2026/09/30/ais-third-wave-coworkers-break-the-security-model-that-worked-for-agents/
tags:
- veille-cyber
- bleepingcomp
---
### L'évolution des agents IA : vers un nouveau modèle de sécurité des identités

L'intégration des agents d'IA persistants en entreprise marque une troisième vague technologique qui rend obsolètes les modèles de sécurité actuels. Contrairement aux outils précédents, ces "collègues numériques" fonctionnent de manière autonome et durable, créant des risques inédits en matière de gestion des accès et de gouvernance.

**Points clés :**
*   **Dissolution des modèles d'accès :** Les agents utilisent actuellement les identifiants des employés ("emprunt de privilèges"), ce qui empêche une attribution précise des actions dans les logs d'audit.
*   **Escalade des privilèges (*Access Creep*) :** Les agents accumulent des droits et combinent des autorisations initialement isolées pour effectuer des tâches non prévues, créant des risques de sécurité majeurs.
*   **Absence d'identité dédiée :** La plupart des plateformes actuelles ne permettent pas de créer des identités distinctes pour les agents, forçant les entreprises à utiliser des jetons statiques ou des comptes de service mal adaptés.
*   **Complexité de la collaboration :** La capacité des agents à engendrer des sous-agents et à collaborer entre eux rend la traçabilité des actions quasi impossible sans un système d'identité propre à chaque entité.

**Vulnérabilités identifiées :**
*   **Shadow AI (IA fantôme) :** Présence d'agents non enregistrés opérant sur le réseau sans supervision.
*   **Privilèges permanents :** Les agents héritent des droits complets des utilisateurs humains, créant une surface d'attaque étendue et incontrôlée.
*   **Audit corrompu :** Les traces d'activité (logs) affichent l'utilisateur humain comme auteur des actions effectuées par l'IA, masquant les comportements malveillants ou erronés.
*   *Note : Bien que l'article souligne des failles structurelles critiques, aucune CVE spécifique n'est mentionnée, car le problème relève de la conception des systèmes d'identité plutôt que de bugs logiciels isolés.*

**Recommandations de sécurité :**
1.  **Découverte active :** Identifier tous les agents opérant dans l'environnement en analysant le trafic d'authentification et les accès OAuth.
2.  **Attribution d'identités uniques :** Fournir à chaque agent une identité propre, distincte de celle de l'employé humain.
3.  **Responsabilité (Accountability) :** Associer systématiquement chaque agent à un "propriétaire" humain responsable du cycle de vie de l'outil.
4.  **Principe du moindre privilège :** Restreindre les scopes d'accès à l'agent lui-même, indépendamment des droits possédés par l'utilisateur qui l'a initié.
5.  **Gestion du cycle de vie :** Définir des politiques de suppression automatique (deprovisioning) basées sur l'inactivité, le départ de l'employé responsable ou la fin d'un projet.

---
[Source](https://www.bleepingcomputer.com/news/security/ais-third-wave-coworkers-break-the-security-model-that-worked-for-agents/){:target="_blank"}
