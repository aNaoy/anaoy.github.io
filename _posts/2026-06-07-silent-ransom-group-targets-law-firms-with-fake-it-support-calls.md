---
title: 'Silent Ransom Group targets law firms with fake IT support calls'
date: 2026-06-07
permalink: /posts/2026/06/07/silent-ransom-group-targets-law-firms-with-fake-it-support-calls/
tags:
- veille-cyber
- bleepingcomp
---
### Menace du « Silent Ransom Group » : Attaques par ingénierie sociale contre les cabinets juridiques

Le « Silent Ransom Group » (également suivi sous les noms UNC3753, Luna Moth ou Chatty Spider) cible activement les cabinets d'avocats et les entreprises de services professionnels via des campagnes sophistiquées d'ingénierie sociale basées sur le rappel téléphonique (*callback phishing*). Contrairement aux méthodes classiques, ce groupe se concentre exclusivement sur le vol de données sensibles et l'extorsion, sans recours au chiffrement par ransomware.

**Points clés :**
*   **Mode opératoire :** L'attaque débute par un e-mail de facturation légitime en apparence, incitant la victime à appeler un faux support informatique.
*   **Techniques d'accès :** Les attaquants manipulent les employés pour qu'ils installent des outils de prise en main à distance (AnyDesk, Zoho Assist, Bomgar, SuperOps) lors de sessions Teams ou Zoom.
*   **Infrastructure furtive :** Utilisation de services de messages éphémères (Privnote) pour limiter les traces forensiques et recours à une infrastructure DNS « fast-flux » utilisant des proxies résidentiels pour masquer les serveurs de fuite de données.
*   **Extorsion agressive :** Le groupe exige le paiement sous trois jours, menaçant de contacter directement les clients et partenaires de la victime en cas de refus.
*   **Vulnérabilité physique :** Le FBI signale que les attaquants vont parfois jusqu'à se présenter physiquement dans les locaux en se faisant passer pour du personnel IT afin de copier des données.

**Vulnérabilités :**
*   Il n'y a pas de CVE spécifique mentionnée, car l'attaque repose sur l'exploitation humaine (ingénierie sociale) et l'utilisation détournée d'outils d'administration à distance légitimes.

**Recommandations :**
*   **Vérification stricte :** Mettre en place des procédures de validation obligatoires pour toute intervention du support informatique.
*   **Contrôle des accès :** Restreindre l'utilisation des outils de prise en main à distance et interdire les logiciels non autorisés.
*   **Renforcement de l'authentification :** Imposer l'authentification multifacteur (MFA) sur tous les accès critiques.
*   **Sécurisation physique :** Restreindre l'accès aux terminaux informatiques et aux ports USB, et former le personnel à détecter les tentatives d'usurpation d'identité.
*   **Sensibilisation :** Éduquer les employés sur les risques du *callback phishing* et les méthodes d'ingénierie sociale par téléphone.

---
[Source](https://www.bleepingcomputer.com/news/security/silent-ransom-group-targets-law-firms-with-fake-it-support-calls/){:target="_blank"}
