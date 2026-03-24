---
title: 'Zero Trust: Bridging the Gap Between Authentication and Trust'
date: 2026-03-24
permalink: /posts/2026/03/24/zero-trust-bridging-the-gap-between-authentication-and-trust/
tags:
- veille-cyber
- bleepingcomp
---
### L'évolution du Zero Trust : au-delà de l'authentification utilisateur

Le modèle de sécurité périmétrique traditionnel est devenu obsolète face à la généralisation du travail hybride. Bien que le *Zero Trust* (« ne jamais faire confiance, toujours vérifier ») s'impose comme la nouvelle norme, de nombreuses organisations échouent à sécuriser correctement leurs accès en se focalisant uniquement sur l'identité de l'utilisateur au détriment de l'état du terminal utilisé.

**Points clés :**
* **La limite de l'authentification unique :** L'authentification multifactorielle (MFA) confirme l'identité, mais ne garantit pas la sécurité de la session. Un utilisateur légitime peut utiliser un appareil infecté ou non conforme, ouvrant une porte aux attaquants.
* **Le fossé identité-appareil :** La menace ne réside plus seulement dans le vol de mots de passe, mais dans le détournement de sessions actives via le vol de jetons (*token theft*).
* **Confiance contextuelle :** L'accès ne doit plus être binaire. Il doit résulter d'une évaluation dynamique combinant l'identité de l'utilisateur et l'intégrité (la "posture") de son appareil en temps réel.

**Vulnérabilités associées :**
L'article souligne des vecteurs d'attaque exploitant les faiblesses des modèles d'authentification actuels :
* **Session Hijacking / Token Theft :** Vol de cookies ou de jetons d'authentification après une connexion MFA réussie, permettant aux attaquants de contourner les contrôles d'identité.
* **Infostealers :** Logiciels malveillants ciblant les informations d'identification et les sessions actives.
* *Note : Bien que l'article mentionne des menaces génériques, il n'identifie pas de CVE spécifique, ces vulnérabilités relevant de techniques d'exploitation logicielles et de détournement de jetons OAuth/SAML.*

**Recommandations :**
* **Lier identité et appareil :** Ne plus autoriser l'accès sans vérifier simultanément la conformité du terminal (mises à jour, antivirus, état du système).
* **Monitoring continu :** Passer d'une vérification ponctuelle (lors du login) à une surveillance constante de la posture du dispositif tout au long de la session.
* **Remédiation dynamique :** Mettre en place des outils capables de restreindre ou de suspendre automatiquement l'accès si l'état de sécurité du terminal se dégrade en cours d'utilisation.
* **Approche holistique :** Intégrer des solutions de type « Device Trust » qui automatisent la validation des appareils pour limiter la surface d'attaque sans sacrifier la productivité des employés.

---
[Source](https://www.bleepingcomputer.com/news/security/zero-trust-bridging-the-gap-between-authentication-and-trust/){:target="_blank"}
