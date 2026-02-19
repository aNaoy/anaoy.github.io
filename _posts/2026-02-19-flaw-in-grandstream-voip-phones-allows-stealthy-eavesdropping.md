---
title: 'Flaw in Grandstream VoIP phones allows stealthy eavesdropping'
date: 2026-02-19
permalink: /posts/2026/02/19/flaw-in-grandstream-voip-phones-allows-stealthy-eavesdropping/
tags:
- veille-cyber
- bleepingcomp
---
**Sécurité des téléphones VoIP Grandstream compromise**

Une faille critique affecte les téléphones VoIP de la série GXP1600 de Grandstream, permettant à un attaquant distant non authentifié d'obtenir des privilèges root et d'écouter discrètement les communications. Cette vulnérabilité, identifiée sous le nom de CVE-2026-2329 avec une note de sévérité de 9.3, concerne six modèles spécifiques : GXP1610, GXP1615, GXP1620, GXP1625, GXP1628 et GXP1630, tant que leur version de firmware est antérieure à 1.0.7.81.

**Points Clés :**

*   **Accès non authentifié :** La faille réside dans le service d'API web (/cgi-bin/api.values.get) qui, par défaut, ne requiert aucune authentification.
*   **Dépassement de tampon sur la pile :** L'exploitation se produit lorsqu'une entrée excessivement longue est fournie au paramètre 'request' de l'API. Ceci provoque un dépassement de tampon sur la pile, permettant à l'attaquant de réécrire la mémoire adjacente et de prendre le contrôle des registres du processeur.
*   **Exécution silencieuse :** L'exploitation est silencieuse et n'entraîne aucun comportement anormal du téléphone.
*   **Pivotement possible :** Même si le téléphone n'est pas directement accessible depuis Internet, un attaquant peut l'atteindre via un autre appareil compromis sur le même réseau.

**Vulnérabilités :**

*   **CVE-2026-2329 :** Dépassement de tampon sur la pile (Stack buffer overflow) permettant l'exécution de code à distance.

**Conséquences de l'exploitation :**

*   Exécution de commandes arbitraires sur le système d'exploitation.
*   Extraction des identifiants des utilisateurs locaux et des comptes SIP.
*   Reconfiguration du téléphone pour utiliser un proxy SIP malveillant, permettant l'écoute clandestine des appels.

**Recommandations :**

*   **Mise à jour du firmware :** Il est fortement recommandé aux utilisateurs des produits Grandstream concernés d'appliquer immédiatement les mises à jour de sécurité disponibles, notamment le firmware version 1.0.7.81 ou ultérieure.

---
[Source](https://www.bleepingcomputer.com/news/security/flaw-in-grandstream-voip-phones-allows-stealthy-eavesdropping/){:target="_blank"}
