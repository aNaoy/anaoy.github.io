---
title: 'Russian Hacker Sentenced to 2 Years for TA551 Botnet-Driven Ransomware Attacks'
date: 2026-03-25
permalink: /posts/2026/03/25/russian-hacker-sentenced-to-2-years-for-ta551-botnet-driven-ransomware-attacks/
tags:
- veille-cyber
- hackernews
---
### Condamnation d'un opérateur du botnet TA551 pour cybercriminalité

Un ressortissant russe, Ilya Angelov, a été condamné à deux ans de prison et à une amende de 100 000 dollars pour son rôle dans la gestion du groupe cybercriminel TA551 (également connu sous les noms de Shathak, UNC2420 ou Gold Cabin). Entre 2017 et 2021, ce groupe a orchestré la création d'un vaste botnet par le biais de campagnes de spam, permettant d'infecter des milliers d'ordinateurs pour revendre des accès à des gangs de ransomware, tels que BitPaymer et IcedID. Ces activités ont généré plus de 14 millions de dollars en extorsions.

**Points clés :**
* **Modèle économique :** TA551 agissait comme un « Initial Access Broker » (courtier d'accès initial), fournissant des accès à des réseaux compromis aux groupes de ransomware.
* **Chaîne d'attaque :** Utilisation d'e-mails de phishing contenant des archives protégées par mot de passe. L'exécution de macros malveillantes dans Microsoft Word permettait de télécharger des outils comme *MOUSEISLAND* et *PHOTOLOADER* pour déployer le malware *IcedID*.
* **Partenariats criminels :** Le groupe a collaboré avec des acteurs majeurs de la menace, notamment les opérateurs de TrickBot et les gangs Conti et Lockean.

**Vulnérabilités exploitées :**
* L'article ne mentionne pas de CVE spécifique, mais souligne l'exploitation récurrente des **macros Microsoft Word** comme vecteur d'infection principal, couplée à des techniques d'ingénierie sociale (archives protégées par mot de passe pour contourner les outils de sécurité périmétriques).

**Recommandations :**
* **Désactivation des macros :** Bloquer les macros dans les documents Office provenant d'Internet via des politiques de groupe (GPO).
* **Filtrage des emails :** Renforcer les solutions de filtrage de messagerie pour détecter les campagnes de phishing et les pièces jointes suspectes (archives protégées).
* **Formation à la cybersécurité :** Sensibiliser les utilisateurs aux risques liés à l'ouverture de documents provenant de sources inconnues, même s'ils semblent protégés par un mot de passe.
* **Détection comportementale :** Mettre en place des solutions EDR (Endpoint Detection and Response) capables d'identifier les comportements malveillants des scripts (téléchargement de charges utiles secondaires).

---
[Source](https://thehackernews.com/2026/03/russian-hacker-sentenced-to-2-years-for.html){:target="_blank"}
