---
title: 'Flaw in Grandstream VoIP phones allows stealthy eavesdropping'
date: 2026-02-20
permalink: /posts/2026/02/20/flaw-in-grandstream-voip-phones-allows-stealthy-eavesdropping/
tags:
- veille-cyber
- bleepingcomp
---
**Vulnérabilité Critique sur les Téléphones VoIP Grandstream : Espionnage Silencieux et Escalade de Privilèges**

Une faille majeure, identifiée sous la référence CVE-2026-2329, affecte plusieurs modèles de la série GXP1600 de téléphones VoIP Grandstream. Cette vulnérabilité critique (score de sévérité de 9.3) permet à un attaquant distant et non authentifié d'obtenir des privilèges root sur l'appareil. L'exploitation de cette faille est indétectable et permet l'écoute clandestine des communications, l'extraction d'identifiants sensibles et la reconfiguration du téléphone pour détourner les appels.

**Points Clés :**

*   **Nature de la vulnérabilité :** Dépassement de tampon sur la pile (stack buffer overflow) dans l'API web du téléphone (/cgi-bin/api.values.get).
*   **Mécanisme d'exploitation :** L'API, accessible par défaut sans authentification, traite de manière non sécurisée un paramètre d'entrée, permettant à un attaquant de surcharger un tampon de 64 octets.
*   **Conséquences :** Obtention de privilèges root, exécution de commandes système arbitraires, vol d'identifiants locaux et SIP, et détournement des appels vers des serveurs malveillants.
*   **Facilité d'exploitation :** La recherche a démontré la faisabilité d'une exploitation à distance via un module Metasploit, avec une technique innovante pour contourner une restriction liée à l'écriture de caractères nuls.
*   **Impact :** Les téléphones Grandstream de la série GXP1600, couramment utilisés par les petites et moyennes entreprises, les écoles et les hôtels, sont potentiellement exposés.

**Vulnérabilités :**

*   **CVE-2026-2329 :** Dépassement de tampon sur la pile dans l'API web permettant l'exécution de code à distance.

**Modèles Affectés (firmware antérieur à 1.0.7.81) :**

*   GXP1610
*   GXP1615
*   GXP1620
*   GXP1625
*   GXP1628
*   GXP1630

**Recommandations :**

*   **Mise à jour immédiate du firmware :** Appliquer la version 1.0.7.81 ou une version ultérieure dès que possible pour corriger la vulnérabilité.
*   **Audit de sécurité :** Vérifier la configuration des appareils VoIP Grandstream et s'assurer qu'aucune vulnérabilité similaire n'est présente.

---
[Source](https://www.bleepingcomputer.com/news/security/flaw-in-grandstream-voip-phones-allows-stealthy-eavesdropping/){:target="_blank"}
