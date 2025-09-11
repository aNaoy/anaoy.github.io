---
title: 'Senator Wyden Urges FTC to Probe Microsoft for Ransomware-Linked Cybersecurity Negligence'
date: 2025-09-11
permalink: /posts/2025/09/11/senator-wyden-urges-ftc-to-probe-microsoft-for-ransomware-linked-cybersecurity-negligence/
tags:
- veille-cyber
- hackernews
---
**Pression sur Microsoft pour négligence en cybersécurité après une attaque de ransomware**

Un sénateur américain a demandé à la Commission fédérale du commerce (FTC) d'enquêter sur Microsoft, arguant d'une "négligence grossière en matière de cybersécurité" ayant permis des attaques par ransomware, notamment contre des infrastructures de santé critiques.

Les informations obtenues auprès du système de santé Ascension, victime d'une importante cyberattaque par ransomware ayant entraîné le vol de données personnelles et médicales de près de 5,6 millions de personnes, ont été au cœur de cette démarche. L'attaque, attribuée au groupe Black Basta, a été rendue possible lorsqu'un contractant, après avoir cliqué sur un lien malveillant via le moteur de recherche Bing, a vu son système infecté. Les attaquants ont ensuite exploité des "paramètres par défaut dangereusement peu sécurisés" des logiciels Microsoft pour accéder à des zones sensibles du réseau.

La technique utilisée, le "Kerberoasting", cible le protocole d'authentification Kerberos pour voler des identités d'accès à des services. Cette méthode tire parti d'une technologie de chiffrement obsolète, le RC4, toujours supporté par défaut par certains logiciels Microsoft, bien que ses faiblesses cryptographiques soient connues depuis longtemps. Le sénateur a souligné que Microsoft a tardé à alerter ses clients sur ce risque, malgré les sollicitations.

Microsoft a finalement publié des recommandations en octobre, annonçant son intention de déprécier le support du RC4 dans les futures mises à jour de Windows 11 et Windows Server. L'entreprise a également introduit des améliorations de sécurité dans Server 2025 pour limiter la délivrance de tickets Kerberos utilisant le chiffrement RC4.

**Points clés :**

*   Un sénateur américain demande une enquête de la FTC sur Microsoft pour négligence en cybersécurité.
*   Une attaque par ransomware contre le réseau de santé Ascension a été facilitée par des failles dans les logiciels Microsoft.
*   La technique de "Kerberoasting", utilisant des paramètres par défaut non sécurisés et un chiffrement obsolète (RC4), a été exploitée.
*   Microsoft a réagi tardivement en publiant des conseils et en annonçant la dépréciation du RC4.

**Vulnérabilités :**

*   Utilisation de paramètres par défaut "dangereusement peu sécurisés" dans les logiciels Microsoft.
*   Support par défaut de la technologie de chiffrement RC4, considérée comme obsolète et faible sur le plan cryptographique.
*   Absence de validation stricte de la longueur des mots de passe pour les comptes privilégiés.

**Recommandations (extraites des annonces de Microsoft et de l'article) :**

*   Utiliser des comptes de service gérés (gMSA ou dMSA) autant que possible.
*   Sécuriser les comptes de service avec des mots de passe longs (au moins 14 caractères) et aléatoires.
*   Configurer tous les comptes de service pour utiliser le chiffrement AES (128 et 256 bits) pour le chiffrement des tickets de service Kerberos.
*   Auditer les comptes utilisateurs avec des Noms Principaux de Service (SPN).
*   Mettre à jour les systèmes d'exploitation vers les versions qui déprécient le support du RC4.

---
[Source](https://thehackernews.com/2025/09/senator-wyden-urges-ftc-to-probe.html){:target="_blank"}
