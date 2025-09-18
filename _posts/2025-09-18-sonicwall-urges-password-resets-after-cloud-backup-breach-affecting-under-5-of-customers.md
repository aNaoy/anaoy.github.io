---
title: 'SonicWall Urges Password Resets After Cloud Backup Breach Affecting Under 5% of Customers'
date: 2025-09-18
permalink: /posts/2025/09/18/sonicwall-urges-password-resets-after-cloud-backup-breach-affecting-under-5-of-customers/
tags:
- veille-cyber
- hackernews
---
**Violation de Sécurité chez SonicWall : Impact sur les Sauvegardes Cloud**

SonicWall a détecté une activité suspecte ciblant son service de sauvegarde cloud pour pare-feux, ayant mené à l'accès par des acteurs malveillants aux fichiers de configuration de sauvegarde de pare-feux de moins de 5% de ses clients. Bien que les identifiants contenus dans ces fichiers soient chiffrés, leur exposition pourrait faciliter des attaques contre les pare-feux concernés. L'entreprise assure qu'il ne s'agit pas d'un incident de ransomware et qu'elle n'a pas connaissance de fuites de ces données en ligne. L'attaque semble avoir été une série d'attaques par force brute visant à accéder aux fichiers de préférences pour une utilisation ultérieure.

**Points Clés :**

*   Accès non autorisé à des fichiers de sauvegarde de configuration de pare-feux via le service MySonicWall.
*   Impacte moins de 5% des clients.
*   Les identifiants dans les fichiers sont chiffrés, mais les données exposées peuvent aider les attaquants.
*   Il ne s'agit pas d'une attaque par ransomware.
*   Nature de l'attaque : brute-force ciblant les fichiers de préférences.

**Vulnérabilités :**

Bien que l'article ne détaille pas de CVE spécifique pour cet incident de sauvegarde cloud, il mentionne en parallèle que des acteurs malveillants du groupe Akira exploitent une faille de sécurité ancienne (CVE-2024-40766, score CVSS: 9.3) pour cibler des appareils SonicWall non corrigés, notamment via des VPN SSL. De plus, un incident récent impliquait l'exploitation de VPN SonicWall et l'utilisation de codes de récupération en clair pour contourner l'authentification multifacteur.

**Recommandations :**

SonicWall recommande vivement aux clients concernés de :

*   Se connecter à MySonicWall.com pour vérifier l'activation des sauvegardes cloud et identifier les numéros de série affectés.
*   Mettre en œuvre des procédures de confinement et de remédiation, incluant :
    *   Limiter l'accès aux services depuis le WAN.
    *   Désactiver l'accès à la gestion HTTP/HTTPS/SSH.
    *   Désactiver l'accès aux VPN SSL et IPSec.
    *   Réinitialiser les mots de passe et les TOTP enregistrés sur le pare-feu.
    *   Analyser les journaux et les modifications récentes de configuration pour déceler toute activité inhabituelle.
*   Importer des fichiers de préférences mis à jour fournis par SonicWall, qui incluent :
    *   Mots de passe aléatoires pour tous les utilisateurs locaux.
    *   Réinitialisation du lien TOTP, si activé.
    *   Clés IPSec VPN aléatoires.

Il est crucial pour les organisations de traiter les codes de récupération avec la même sensibilité que les mots de passe de comptes privilégiés.

---
[Source](https://thehackernews.com/2025/09/sonicwall-urges-password-resets-after.html){:target="_blank"}
