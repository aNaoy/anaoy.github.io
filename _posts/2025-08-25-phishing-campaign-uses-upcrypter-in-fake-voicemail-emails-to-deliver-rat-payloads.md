---
title: 'Phishing Campaign Uses UpCrypter in Fake Voicemail Emails to Deliver RAT Payloads'
date: 2025-08-25
permalink: /posts/2025/08/25/phishing-campaign-uses-upcrypter-in-fake-voicemail-emails-to-deliver-rat-payloads/
tags:
- veille-cyber
- hackernews
---
Voici un résumé de l'article :

**Campagne de Phishing : UpCrypter et les Fausses Messageries Vocales**

Une campagne de phishing sophistiquée utilise des courriels se faisant passer pour des messageries vocales ou des bons de commande pour diffuser le chargeur de malware UpCrypter. Ce dernier sert de passerelle pour des outils d'accès à distance (RAT) tels que PureHVNC RAT, DCRat et Babylon RAT, permettant aux attaquants de prendre le contrôle total des systèmes compromis. Les attaques ciblent principalement les secteurs de la fabrication, de la technologie, de la santé, de la construction et du commerce de détail/hospitalité à l'échelle mondiale.

Les courriels contiennent des liens vers des pages de phishing conçues pour paraître authentiques, incorporant parfois le logo de l'entreprise victime. Ces pages incitent les utilisateurs à télécharger des fichiers, souvent des archives ZIP contenant des scripts JavaScript obfusqués. Ces scripts effectuent des vérifications anti-analyse et anti-virtuelle avant de contacter un serveur externe pour récupérer la charge utile finale, potentiellement dissimulée par stéganographie. Une variante d'UpCrypter utilise également un chargeur MSIL pour télécharger un script PowerShell, une DLL et la charge utile principale, permettant une exécution sans écriture sur le système de fichiers pour minimiser les traces forensiques.

Cette campagne s'inscrit dans une tendance plus large où les cybercriminels exploitent des services légitimes (comme Google Classroom, Microsoft 365 Direct Send, OneNote, Vercel, Discord CDN, SendGrid, Zoom, etc.) pour leurs attaques. Cette approche, connue sous le nom de "living-off-trusted-sites" (LOTS), permet de contourner les protocoles d'authentification des courriels et de cibler les utilisateurs plus efficacement. Pour contrer ces menaces, des mesures telles que le rejet du "Direct Send" dans Microsoft 365 ou l'application de politiques de quarantaine peuvent être mises en place. Les pages de phishing utilisent également des techniques d'évasion côté client, comme des scripts anti-analyse JavaScript, pour déjouer les systèmes de détection automatisés et les analystes.

**Points Clés :**

*   **Outil principal :** UpCrypter, un chargeur de malware.
*   **Méthode de distribution :** Courriels de phishing imitant des messageries vocales ou des bons de commande.
*   **Objectif :** Délivrer des outils d'accès à distance (RAT) comme PureHVNC RAT, DCRat, Babylon RAT.
*   **Secteurs ciblés :** Fabrication, technologie, santé, construction, commerce de détail/hospitalité.
*   **Mécanismes d'évasion :** Obfuscation, anti-analyse, anti-VM, stéganographie, exploitation de services légitimes (LOTS).
*   **Tendances annexes :** Utilisation de Google Classroom, Microsoft 365 Direct Send, OneNote, et divers services en ligne pour la distribution de malwares et le phishing.

**Vulnérabilités :**

*   Aucune vulnérabilité spécifique (CVE) n'est mentionnée dans cet article concernant UpCrypter ou les RAT mentionnés. La campagne exploite la confiance des utilisateurs et les fonctionnalités des plateformes de communication et de collaboration pour contourner les défenses.

**Recommandations :**

*   **Vigilance face aux courriels de phishing :** Être prudent avec les courriels inattendus, surtout ceux contenant des liens ou des pièces jointes, même s'ils semblent provenir de sources connues.
*   **Vérification des sources :** En cas de doute, contacter directement l'expéditeur par un canal de communication vérifié (pas par les informations contenues dans le courriel suspect).
*   **Mises à jour de sécurité :** S'assurer que les systèmes d'exploitation, les navigateurs et les logiciels de sécurité sont à jour.
*   **Formation des utilisateurs :** Sensibiliser les employés aux tactiques de phishing et aux bonnes pratiques de cybersécurité.
*   **Configuration des services de messagerie :** Examiner et configurer les règles de messagerie pour bloquer ou mettre en quarantaine les courriels suspects et envisager des mesures de sécurité supplémentaires pour les services comme Microsoft 365 Direct Send.

---
[Source](https://thehackernews.com/2025/08/phishing-campaign-uses-upcrypter-in.html){:target="_blank"}
