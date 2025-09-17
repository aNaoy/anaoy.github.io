---
title: 'SonicWall warns customers to reset credentials after breach'
date: 2025-09-17
permalink: /posts/2025/09/17/sonicwall-warns-customers-to-reset-credentials-after-breach/
tags:
- veille-cyber
- bleepingcomp
---
**Violation de données chez SonicWall : Exfiltration de fichiers de configuration de pare-feu**

Une compromission de sécurité a affecté les comptes MySonicWall, entraînant l'exposition de fichiers de sauvegarde de configuration de pare-feu. Ces fichiers contiennent des informations sensibles qui pourraient faciliter les attaques contre les pare-feu SonicWall. L'incident concerne moins de 5% des pare-feu SonicWall et résulte d'attaques par force brute ciblées sur les comptes clients. SonicWall a mis fin à l'accès des attaquants et collabore avec les autorités.

**Points Clés :**

*   **Nature de la violation :** Exfiltration de fichiers de sauvegarde de configuration de pare-feu via des comptes MySonicWall compromis.
*   **Impact potentiel :** Facilite l'exploitation des pare-feu par les acteurs malveillants, potentiellement en exposant des identifiants et des jetons pour les services exécutés sur les appareils SonicWall.
*   **Cause :** Attaques par force brute visant les comptes MySonicWall.
*   **Portée :** Affecte moins de 5% des pare-feu SonicWall.

**Vulnérabilités :**

*   Aucune vulnérabilité spécifique (CVE) n'est directement attribuée à cet incident d'exfiltration de fichiers de configuration dans le texte. Cependant, il est mentionné que l'accès aux fichiers compromis "pourrait rendre l'exploitation des pare-feu beaucoup plus facile pour les acteurs de la menace".

**Recommandations :**

*   **Réinitialiser les identifiants :** Changer tous les mots de passe, clés API et jetons d'authentification utilisés par les utilisateurs, les comptes VPN et les services.
*   **Mettre à jour les secrets :** Les mots de passe, secrets partagés et clés de chiffrement configurés dans SonicOS peuvent nécessiter une mise à jour auprès de fournisseurs externes (FAI, DNS dynamique, fournisseur de messagerie, serveur VPN IPSec, serveur LDAP/RADIUS, etc.).
*   **Procéder par étapes :**
    1.  Désactiver ou restreindre l'accès aux services sur l'appareil depuis le WAN.
    2.  Réinitialiser tous les identifiants, clés API et jetons d'authentification.
*   **Consulter la documentation :** Se référer aux bulletins de support "Essential Credential Reset" et au "Remediation Playbook" pour une approche structurée.

---
[Source](https://www.bleepingcomputer.com/news/security/sonicwall-warns-customers-to-reset-credentials-after-MySonicWall-breach/){:target="_blank"}
