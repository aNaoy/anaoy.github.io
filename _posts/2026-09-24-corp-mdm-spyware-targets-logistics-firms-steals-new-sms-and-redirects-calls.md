---
title: 'Corp MDM Spyware Targets Logistics Firms, Steals New SMS and Redirects Calls'
date: 2026-09-24
permalink: /posts/2026/09/24/corp-mdm-spyware-targets-logistics-firms-steals-new-sms-and-redirects-calls/
tags:
- veille-cyber
- hackernews
---
### Espionnage mobile : Le malware « Corp MDM » cible le secteur de la logistique

Une nouvelle campagne de cyberespionnage utilise un logiciel malveillant Android baptisé **Corp MDM** pour cibler spécifiquement les entreprises du secteur de la logistique (notamment CEVA et TKW Logistics). Le malware est distribué via de fausses pages de téléchargement se faisant passer pour le Google Play Store.

**Points clés :**
*   **Mode opératoire :** Le malware est installé par "sideloading" via des sites frauduleux. Une fois actif, il s'exécute en arrière-plan et masque son icône d'application.
*   **Fonctionnalités :** Il intercepte les nouveaux SMS entrants, permet le transfert d'appels téléphoniques et communique avec un serveur de commande et contrôle (C2) via HTTP en texte clair.
*   **Objectif :** Le vol de données sensibles, notamment les codes de vérification (OTP), les notifications de réinitialisation de mot de passe et les informations de livraison, facilitant ainsi les fraudes financières.
*   **Origine suspectée :** Des indices dans le code source et l'interface d'administration suggèrent un lien avec des acteurs basés en Russie ou en Arménie.

**Vulnérabilités :**
*   Le malware exploite la confiance des utilisateurs par le biais de sites de phishing imitant des applications de logistique légitimes.
*   Il tire profit des autorisations système Android (SMS, téléphonie, notifications) accordées lors de l'installation pour compromettre la sécurité des communications.
*   *Note : Aucune CVE spécifique n'est associée à ce malware, car il s'appuie sur des fonctionnalités légitimes du système Android détournées par l'ingénierie sociale.*

**Recommandations :**
*   **Vigilance sur l'installation :** Ne jamais installer d'applications provenant de sources autres que le Google Play Store officiel ou les stores d'entreprise gérés par le service informatique.
*   **Gestion des permissions :** Examiner avec attention les permissions demandées par une application lors de son installation, particulièrement celles liées aux SMS et aux appels.
*   **Protection des terminaux :** Utiliser des solutions de gestion des appareils mobiles (MDM) légitimes pour contrôler et sécuriser les flottes d'appareils professionnels.
*   **Sensibilisation :** Former le personnel du secteur logistique aux tactiques de phishing, incluant les fausses pages de téléchargement et les e-mails frauduleux ciblant leurs outils métiers.

---
[Source](https://thehackernews.com/2026/09/corp-mdm-spyware-targets-logistics.html){:target="_blank"}
