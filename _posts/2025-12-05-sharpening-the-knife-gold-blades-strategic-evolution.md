---
title: 'Sharpening the knife: GOLD BLADE’s strategic evolution'
date: 2025-12-05
permalink: /posts/2025/12/05/sharpening-the-knife-gold-blades-strategic-evolution/
tags:
- veille-cyber
- sophos
---
### L'Évolution de GOLD BLADE : Du Cyberespionnage au Ransomware Hybride

Le groupe de menace GOLD BLADE, également connu sous les noms de RedCurl, RedWolf et Earth Kapre, a fait évoluer ses tactiques d'attaque entre février 2024 et août 2025. Historiquement axé sur le cyberespionnage, il combine désormais le vol de données avec le déploiement sélectif de ransomware via un logiciel malveillant personnalisé appelé QWCrypt. Les attaques observées montrent une concentration géographique inhabituelle, près de 80% ciblant des organisations canadiennes.

**Points Clés:**

*   **Évolution Tactique:** GOLD BLADE a abandonné les e-mails de phishing traditionnels au profit de l'exploitation des plateformes de recrutement pour distribuer des CV infectés.
*   **Modèle Hybride:** Le groupe combine le cyberespionnage avec la monétisation sélective via le ransomware QWCrypt, suggérant une opération professionnalisée.
*   **Rythme d'Attaque:** Les opérations se caractérisent par des périodes de dormance suivies de pics d'activité, chaque vague introduisant de nouvelles techniques affinées.
*   **Ciblage Géographique:** Une forte concentration d'attaques au Canada (environ 80%) et aux États-Unis (14%) a été observée dans le cadre de la campagne STAC6565.
*   **Défense Évasion Sophistiquée:** Utilisation de techniques telles que le "Bring Your Own Vulnerable Driver" (BYOVD) avec des pilotes Zemana modifiés et des outils comme Terminator pour désactiver les solutions de sécurité.

**Vulnérabilités et Exploitations:**

*   **Exploitation des Plateformes de Recrutement:** L'envoi de CV malveillants via des plateformes comme Indeed, JazzHR et ADP WorkforceNow pour contourner les filtres de sécurité par e-mail.
*   **Techniques d'Infection Multi-étapes:** Utilisation de chaînes d'infection complexes impliquant des fichiers .lnk, des fichiers .iso/.img, et des DLL chargées de manière latérale (sideloading).
*   **Abus de Lolbins (Living Off The Land Binaries):** Utilisation d'outils légitimes Windows comme `rundll32.exe` et `pcalua.exe` pour exécuter le code malveillant.
*   **Désactivation des Défenses:** Le groupe utilise des versions modifiées de l'outil "Terminator" et des pilotes Zemana pour neutraliser les logiciels antivirus et EDR. Il a également été observé qu'ils désactivent des mécanismes de sécurité Windows comme la liste noire des pilotes vulnérables et l'intégrité du code renforcée par hyperviseur.
*   **Ransomware QWCrypt:** Déploiement d'un ransomware personnalisé qui chiffre les fichiers et laisse une note de rançon, réutilisant des phrases de familles de ransomware connues pour faire pression sur les victimes.
*   **C2 et Exfiltration:** Utilisation d'outils comme RPivot et Chisel pour la communication C2, et des services Cloudflare Workers pour l'exfiltration de données.

**Recommandations:**

*   **Sensibilisation et Formation:** Former les employés à reconnaître les tentatives de phishing et les CV potentiellement malveillants, en insistant sur le fait de ne jamais télécharger de CV à partir de liens externes en cas d'erreur.
*   **Sauvegardes Robuste:** Maintenir des sauvegardes de données critiques hors ligne ou dans un environnement isolé pour faciliter la récupération.
*   **Durcissement des Flux de Recrutement:** Examiner les pièces jointes des plateformes de recrutement via des passerelles de sécurité ou mettre en quarantaine automatiquement les CV suspects. Utiliser des visualiseurs de documents sécurisés.
*   **Couverture et Surveillance des Points d'Extrémité:** Assurer la gestion centralisée et la mise à jour des protections sur tous les points d'extrémité, avec une journalisation complète pour la visibilité et la réponse.
*   **Solutions MDR (Managed Detection and Response):** Mettre en place des solutions de détection et de réponse gérées par des analystes qualifiés pour une surveillance, une enquête et une réponse actives aux alertes.

Les indicateurs de compromission, tels que les hachages de fichiers, les URL, les noms de domaine et les adresses IP, sont répertoriés dans le document original pour aider à la détection de ces activités. Aucune vulnérabilité CVE spécifique n'est mentionnée dans l'article, mais les techniques utilisées exploitent des configurations système et des méthodes d'ingénierie sociale.

---
[Source](https://news.sophos.com/en-us/2025/12/05/sharpening-the-knife-gold-blades-strategic-evolution/){:target="_blank"}
