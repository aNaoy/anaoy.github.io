---
title: 'The end of an era: Properly formated IP addresses in all of our data., (Sun, Aug 24th)'
date: 2025-08-24
permalink: /posts/2025/08/24/the-end-of-an-era-properly-formated-ip-addresses-in-all-of-our-data-sun-aug-24th/
tags:
- veille-cyber
- sans-isc
---
**Modernisation du format des adresses IP sur les sites du Internet Storm Center et DShield**

Les sites du Internet Storm Center et DShield, âgés d'environ 25 ans, abandonnent leur ancien format d'adresses IP. Historiquement, une méthode de "remplissage à 15 caractères avec des zéros" était utilisée pour faciliter le tri des adresses dans la base de données MySQL. Cette pratique, bien que jugée efficace à l'époque, présentait des inconvénients, notamment l'ambiguïté potentielle liée aux zéros initiaux qui peuvent suggérer un format octal.

Le passage à un format "décimal pointé" standard, tel que défini dans la RFC 4001 (succédant à la RFC 2851 de 2000), est en cours.

**Points clés:**

*   Abandon du format d'adresses IP "15 caractères 0-padded" utilisé historiquement.
*   Adoption du format standard "décimal pointé".
*   Le changement vise à corriger une pratique ancienne jugée problématique et potentiellement ambiguë.

**Vulnérabilités identifiées:**

Aucune vulnérabilité de sécurité spécifique (avec CVE) n'est mentionnée dans l'article. L'enjeu porte sur la correction d'un format de données ancien et moins conforme aux standards actuels.

**Recommandations:**

*   Les utilisateurs sont invités à signaler toute observation du format d'adresses IP "ancien".
*   La conversion des données historiques prendra du temps.
*   Il est noté que la fonction `inet_aton()` de MySQL gère l'ancien format en ignorant les zéros initiaux, ce qui évite les interprétations octales incorrectes.

---
[Source](https://isc.sans.edu/diary/rss/32228){:target="_blank"}
