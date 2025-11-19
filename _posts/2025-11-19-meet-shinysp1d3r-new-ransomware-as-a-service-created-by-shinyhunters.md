---
title: 'Meet ShinySp1d3r: New Ransomware-as-a-Service created by ShinyHunters'
date: 2025-11-19
permalink: /posts/2025/11/19/meet-shinysp1d3r-new-ransomware-as-a-service-created-by-shinyhunters/
tags:
- veille-cyber
- bleepingcomp
---
## ShinySp1d3r : Nouvelle Plateforme RaaS Émergente

Une nouvelle plateforme de ransomware-as-a-service (RaaS), nommée ShinySp1d3r, est en cours de développement par des acteurs malveillants associés aux groupes ShinyHunters et Scattered Spider. Ces groupes, auparavant utilisateurs d'autres ransomwares (ALPHV/BlackCat, Qilin, RansomHub, DragonForce), lancent désormais leur propre opération pour mener des attaques et les proposer à des affiliés.

La découverte de cette plateforme a été faite via un canal Telegram, où les auteurs se présentent comme "Scattered Lapsus$ Hunters", une combinaison des noms des groupes d'origine.

**Points Clés et Vulnérabilités Potentielles :**

*   **Développement Personnalisé :** L'encryptor ShinySp1d3r est développé à partir de zéro, et non basé sur des codes existants divulgués.
*   **Fonctionnalités d'Évasion et Persistance :**
    *   Interception de la fonction `EtwEventWrite` pour éviter l'enregistrement des événements dans le journal des événements Windows.
    *   Tuer les processus qui maintiennent un fichier ouvert pour faciliter le chiffrement.
    *   Utilisation potentielle de l'API `Restart Manager` (non encore implémentée).
    *   Propagation sur le réseau local via la création de services, WMI (`Win32_Process.Create`), ou l'ajout de scripts de démarrage GPO.
    *   Fonctionnalités anti-analyse et effacement des tampons mémoire.
*   **Destruction de Données de Récupération :** Suppression des "Shadow Volume Copies" pour empêcher la restauration des fichiers chiffrés.
*   **Recherche et Chiffrement de Partages Réseau :** Identification et chiffrement de ressources accessibles via des partages réseau ouverts.
*   **Mécanisme de Chiffrement :** Utilisation de l'algorithme ChaCha20 pour le chiffrement des fichiers, avec la clé privée protégée par RSA-2048. Chaque fichier reçoit une extension unique basée sur une formule mathématique.
*   **Structure des Fichiers Chiffrés :** Les fichiers chiffrés commencent par "SPDR" et se terminent par "ENDS", incluant des métadonnées comme le nom du fichier et la clé privée chiffrée.
*   **Tactiques d'Extorsion :**
    *   Un fichier `README.txt` (ou similaire) est laissé dans chaque dossier, expliquant l'incident, les modalités de négociation et une adresse TOX pour la communication.
    *   Une note de rançon mentionne une fuite de données potentielle sur un site Tor.
    *   Un fond d'écran personnalisé alerte la victime et l'invite à lire la note de rançon.
*   **Déploiement Multi-plateforme (en développement) :** Des versions CLI, Linux et ESXi sont prévues, ainsi qu'une version "lightning" optimisée pour la vitesse.
*   **Restrictions Ciblées :** Interdiction de cibler le secteur de la santé (hôpitaux, cliniques, entreprises pharmaceutiques et assurances), et les pays de la CEI (Russie, etc.). Cependant, ces restrictions peuvent être contournées par le passé avec d'autres groupes.

**Recommandations :**

Bien que l'article ne détaille pas de recommandations spécifiques pour la protection contre ShinySp1d3r, les pratiques générales de cybersécurité s'appliquent :

*   **Sauvegardes régulières et hors ligne :** Assurer la possibilité de restaurer les données sans dépendre des mécanismes de récupération du système d'exploitation potentiellement compromis.
*   **Mises à jour et gestion des correctifs :** Maintenir les systèmes d'exploitation et les logiciels à jour pour corriger les vulnérabilités connues.
*   **Segmentation réseau :** Limiter la propagation latérale des menaces en segmentant le réseau.
*   **Surveillance et détection :** Mettre en place des solutions de sécurité capables de détecter les comportements suspects et les tentatives d'évasion.
*   **Sensibilisation des employés :** Former les utilisateurs aux risques de phishing et d'ingénierie sociale, qui sont souvent des vecteurs d'infection initiaux.
*   **Application stricte des principes de moindre privilège :** Accorder uniquement les permissions nécessaires aux utilisateurs et aux applications pour limiter l'impact d'une compromission.
*   **Désactivation des partages réseau inutiles :** Réduire la surface d'attaque exposée.

---
[Source](https://www.bleepingcomputer.com/news/security/meet-shinysp1d3r-new-ransomware-as-a-service-created-by-shinyhunters/){:target="_blank"}
