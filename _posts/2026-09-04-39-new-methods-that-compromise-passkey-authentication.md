---
title: '39 New Methods That Compromise Passkey Authentication'
date: 2026-09-04
permalink: /posts/2026/09/04/39-new-methods-that-compromise-passkey-authentication/
tags:
- veille-cyber
- bleepingcomp
---
### La réalité des menaces pesant sur l'authentification par passkeys

Bien que le protocole cryptographique FIDO2 reste robuste, l'écosystème entourant les *passkeys* (navigateurs, systèmes d'exploitation, gestionnaires de mots de passe, services cloud) est devenu une cible privilégiée. Avec au moins 39 vecteurs d'attaque documentés, les cybercriminels ne cherchent plus à casser la cryptographie, mais à manipuler le processus d'authentification ou son environnement.

**Points clés :**
*   **Intégrité vs Compromission :** La cryptographie peut rester intacte alors que le compte est piraté, car l'attaque cible les couches périphériques (OS, interface utilisateur, synchronisation).
*   **Extension de la surface d'attaque :** La capacité des *passkeys* à être synchronisés, exportés ou restaurés via le cloud fragilise leur sécurité en les exposant aux vulnérabilités des appareils et comptes associés.
*   **Vulnérabilité des processus :** Les phases d'enrôlement et de récupération des comptes sont des maillons faibles ; un attaquant peut créer une nouvelle *passkey* légitime plutôt que de voler celle existante.
*   **Tromperie utilisateur :** Des outils permettent de falsifier des invites d'authentification (phishing de *passkeys*) ou de détourner des sessions via des logiciels malveillants.

**Principales vulnérabilités exploitées :**
*   **Interface utilisateur :** *Prompt flooding*, usurpation d'identité d'application, et overlays d'interface FIDO.
*   **Infrastructure de gestion :** Compromission de comptes cloud (Apple/Google), accès à des gestionnaires de mots de passe, et malware sur terminaux mobiles.
*   **Processus métier :** Détournement des procédures d'enrôlement (social engineering via vishing) et des mécanismes de récupération de compte.

*Note : L'article ne mentionne pas de CVE spécifiques, les attaques reposant davantage sur des scénarios d'exploitation logique et d'ingénierie sociale que sur des failles logicielles isolées.*

**Recommandations :**
*   **Privilégier le matériel dédié :** Utiliser des clés de sécurité biométriques physiques qui ne sont ni synchronisables, ni exportables, et qui ne partagent pas d'OS avec des applications tierces.
*   **Sécuriser l'enrôlement :** L'ajout de nouveaux authentificateurs doit impérativement nécessiter la validation par un authentificateur déjà approuvé, et non par des méthodes de récupération plus faibles.
*   **Configuration stricte des services :** Restreindre les classes d'authentificateurs autorisés, valider systématiquement l'identité de l'authentificateur et imposer une vérification utilisateur stricte (biométrie).
*   **Réduction de la surface :** Éviter l'utilisation de *passkeys* logiciels partagés ou synchronisés pour les accès sensibles en entreprise.

---
[Source](https://www.bleepingcomputer.com/news/security/39-new-methods-that-compromise-passkey-authentication/){:target="_blank"}
