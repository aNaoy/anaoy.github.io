---
title: 'Fake Booking Emails Redirect Hotel Staff to Fake BSoD Pages Delivering DCRat'
date: 2026-01-06
permalink: /posts/2026/01/06/fake-booking-emails-redirect-hotel-staff-to-fake-bsod-pages-delivering-dcrat/
tags:
- veille-cyber
- hackernews
---
## Tactique de phishing par fausses annulations de réservation ciblant le secteur hôtelier

Une campagne malveillante, baptisée PHALT#BLYX, exploite des emails d'apparence légitime de type Booking.com pour inciter le personnel hôtelier à télécharger et exécuter des commandes PowerShell. Ces commandes, dissimulées derrière de fausses pages d'erreur "écran bleu de la mort" (BSoD), servent à déployer un cheval de Troie d'accès à distance (RAT) connu sous le nom de DCRat. La campagne a été détectée fin 2025 et semble cibler spécifiquement le secteur hôtelier européen, comme en témoigne l'utilisation de devises européennes dans les emails et la langue russe dans certains fichiers malveillants, suggérant une origine russe.

Les acteurs de la menace utilisent une chaîne d'attaque en plusieurs étapes. Ils commencent par un email de phishing se faisant passer pour une notification d'annulation de réservation Booking.com, contenant un lien vers un faux site web. Ce site affiche une fausse page de confirmation et des instructions pour ouvrir l'outil "Exécuter" de Windows et y coller une commande. Cette action déclenche l'exécution d'un script PowerShell qui télécharge ensuite un fichier projet MSBuild ("v.proj"). Ce dernier, exécuté via "MSBuild.exe", configure des exclusions dans Microsoft Defender Antivirus pour échapper à la détection, établit une persistance dans le dossier de démarrage et télécharge finalement le RAT DCRat.

Le malware DCRat peut désactiver le programme de sécurité s'il dispose des privilèges administrateur. Sinon, il tente d'obtenir ces privilèges par des invites de contrôle de compte d'utilisateur répétées. Parallèlement, une page administrative légitime de Booking.com est ouverte dans le navigateur pour détourner l'attention de la victime. DCRat, également connu sous le nom de Dark Crystal RAT, est un RAT polyvalent capable de voler des informations sensibles, d'exécuter des commandes arbitraires et de télécharger d'autres charges utiles.

Cette campagne illustre l'utilisation de techniques "living-off-the-land" (LotL), notamment l'abus d'outils système légitimes comme MSBuild.exe, pour masquer les activités malveillantes, établir une présence durable sur les systèmes compromis et démontrer une compréhension avancée des mécanismes de protection des points d'extrémité.

**Points clés :**

*   **Technique principale :** Phishing ciblé avec usurpation de Booking.com, fausses pages BSoD, et utilisation de PowerShell et MSBuild.exe.
*   **Cible :** Secteur hôtelier européen.
*   **Malware final :** DCRat (Dark Crystal RAT), un RAT d'accès à distance.
*   **Tactiques avancées :** Utilisation de LotL, contournement de la sécurité, persistance et élévation de privilèges.

**Vulnérabilités :**

*   Aucune vulnérabilité logicielle spécifique avec un identifiant CVE n'est mentionnée dans l'article. La vulnérabilité exploitée réside dans l'ingénierie sociale et la confiance accordée aux emails et aux instructions apparentes.

**Recommandations :**

*   **Vigilance accrue face aux emails :** Former les employés à identifier les emails suspects, particulièrement ceux concernant des réservations ou des annulations, et à ne jamais cliquer sur des liens ou exécuter des commandes sans vérification approfondie.
*   **Validation des sources :** Toujours vérifier l'authenticité des sites web et des demandes d'informations avant de fournir des identifiants ou d'exécuter des actions.
*   **Mises à jour et sécurisation des logiciels :** Maintenir à jour les systèmes d'exploitation et les logiciels de sécurité.
*   **Sensibilisation à la sécurité :** Mener des formations régulières sur la cybersécurité pour informer le personnel des menaces actuelles et des bonnes pratiques.
*   **Surveillance des activités suspectes :** Mettre en place des outils de surveillance pour détecter les comportements anormaux sur le réseau et les points d'extrémité.

---
[Source](https://thehackernews.com/2026/01/fake-booking-emails-redirect-hotel.html){:target="_blank"}
