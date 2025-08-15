---
title: 'Cisco warns of max severity flaw in Firewall Management Center'
date: 2025-08-15
permalink: /posts/2025/08/15/cisco-warns-of-max-severity-flaw-in-firewall-management-center/
tags:
- veille-cyber
- bleepingcomp
---
**Vulnérabilité Critique dans le Firewall Management Center de Cisco : Exécution de Code à Distance**

Une faille de sécurité critique, notée 10/10, a été identifiée dans le sous-système RADIUS du logiciel Cisco Secure Firewall Management Center (FMC). Cette vulnérabilité, référencée CVE-2025-20265, permet à un attaquant non authentifié d'exécuter des commandes arbitraires avec des privilèges élevés sur l'appareil.

**Points Clés :**

*   **Nature de la Vulnérabilité :** Exécution de code à distance (RCE) par injection de commandes.
*   **Cause :** Mauvaise gestion des entrées utilisateur lors de la phase d'authentification RADIUS.
*   **Impact :** Compromission totale du système avec des privilèges élevés.
*   **Produit Affecté :** Cisco Secure Firewall Management Center (FMC).
*   **Versions Concernées :** FMC versions 7.0.7 et 7.7.0, lorsque l'authentification RADIUS est activée pour l'interface web ou SSH, ou les deux.
*   **Mode d'Exploitation :** Un attaquant peut envoyer des entrées spécialement conçues lors de la saisie des identifiants RADIUS.

**Vulnérabilité Principale :**

*   **CVE-2025-20265** : Exécution de code à distance dans le sous-système RADIUS du Cisco Secure Firewall Management Center.

**Recommandations :**

*   **Mise à jour Immédiate :** Installer les mises à jour logicielles gratuites publiées par Cisco pour corriger le problème.
*   **Mesure Alternative (si la mise à jour n'est pas possible) :** Désactiver l'authentification RADIUS et la remplacer par une méthode alternative telle que les comptes utilisateurs locaux, LDAP externe ou l'authentification unique SAML. Il est crucial de vérifier l'applicabilité et l'impact de cette mesure dans votre environnement.

Cisco a également corrigé 13 autres vulnérabilités de haute gravité affectant divers produits, principalement des dénis de service (DoS). Aucune de ces vulnérabilités n'est connue pour être exploitée activement à l'heure actuelle. Pour la majorité de ces failles, la recommandation est d'installer les dernières mises à jour. Pour CVE-2025-20127 (déni de service TLS 1.3), la suggestion est de retirer la suite de chiffrement TLS 1.3.

---
[Source](https://www.bleepingcomputer.com/news/security/cisco-warns-of-max-severity-flaw-in-firewall-management-center/){:target="_blank"}
