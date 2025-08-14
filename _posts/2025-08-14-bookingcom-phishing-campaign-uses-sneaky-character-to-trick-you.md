---
title: 'Booking.com phishing campaign uses sneaky ん character to trick you'
date: 2025-08-14
permalink: /posts/2025/08/14/bookingcom-phishing-campaign-uses-sneaky-character-to-trick-you/
tags:
- veille-cyber
- bleepingcomp
---
**Campagnes de Phishing Exploitant la Typographie Trompeuse**

Des acteurs malveillants utilisent des techniques d'ingénierie sociale basées sur la ressemblance visuelle des caractères pour tromper les utilisateurs.

**Points Clés :**

*   Une campagne cible les utilisateurs de Booking.com en utilisant le caractère japonais hiragana "ん" (Unicode U+3093).
*   Ce caractère, dans certaines polices, peut ressembler à une barre oblique ("/") ou à la séquence "/n", permettant de créer des URLs qui semblent légitimes à première vue mais redirigent vers des sites malveillants.
*   L'URL d'apparence légitime "https://admin.booking.com/hotel/hoteladmin/..." masque en réalité un domaine frauduleux comme "www-account-booking.com".
*   Ces URL mènent à des pages qui distribuent des fichiers MSI contenant potentiellement des logiciels espions (infostealers) ou des chevaux de Troie d'accès à distance (RATs).
*   Une autre campagne détectée exploite la ressemblance entre "Intuit" et "Lntuit" (en utilisant un "L" majuscule suivi de "ntuit") pour créer des domaines d'apparence similaire.
*   Ces attaques tirent parti des homoglyphes, des caractères qui se ressemblent mais appartiennent à des jeux de caractères différents.

**Vulnérabilités Exploités :**

*   L'exploitation de la ressemblance visuelle des caractères Unicode (homoglyphes) pour créer des URLs trompeuses. Bien qu'aucun CVE spécifique ne soit mentionné pour cette technique, elle s'apparente aux attaques par homographes.

**Recommandations :**

*   **Survoler les liens :** Avant de cliquer, passer la souris sur les liens pour révéler l'URL réelle et vérifier la destination.
*   **Inspection des domaines :** Vérifier attentivement le domaine principal, situé à droite du dernier slash dans l'adresse URL.
*   **Mise à jour des logiciels de sécurité :** Maintenir à jour les logiciels de sécurité des terminaux pour se protéger contre les malwares distribués directement après un clic sur un lien de phishing.
*   **Vigilance accrue :** Être conscient que les attaquants recherchent constamment de nouvelles méthodes pour exploiter la typographie à des fins de manipulation.

---
[Source](https://www.bleepingcomputer.com/news/security/bookingcom-phishing-campaign-uses-sneaky-character-to-trick-you/){:target="_blank"}
