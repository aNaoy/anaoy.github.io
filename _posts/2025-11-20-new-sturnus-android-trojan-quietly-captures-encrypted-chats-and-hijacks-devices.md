---
title: 'New Sturnus Android Trojan Quietly Captures Encrypted Chats and Hijacks Devices'
date: 2025-11-20
permalink: /posts/2025/11/20/new-sturnus-android-trojan-quietly-captures-encrypted-chats-and-hijacks-devices/
tags:
- veille-cyber
- hackernews
---
### Sturnus : Un nouveau cheval de Troie Android discret

Ce logiciel malveillant, baptisé Sturnus, cible les utilisateurs d'Android dans le but de voler des informations bancaires et de prendre le contrôle total des appareils pour commettre des fraudes financières. Une de ses particularités est sa capacité à intercepter les conversations même chiffrées sur des applications comme WhatsApp, Telegram et Signal en capturant le contenu de l'écran après son décryptage.

Il utilise également des attaques par superposition, présentant de fausses interfaces de connexion par-dessus les applications bancaires légitimes pour dérober les identifiants des victimes. Sturnus, actuellement en phase d'évaluation, semble opérer de manière privée et se concentre sur les institutions financières d'Europe du Sud et Centrale, adaptant ses attaques aux spécificités régionales.

Ses mécanismes de communication mélangent texte brut, AES et RSA, rappelant ainsi le chant varié et mimétique de l'étourneau européen (Sturnus vulgaris). Une fois actif, le cheval de Troie communique avec un serveur distant pour s'enregistrer et recevoir des charges utiles cryptées. Il peut également établir une connexion pour permettre aux acteurs malveillants de contrôler l'appareil via des sessions VNC.

Sturnus exploite les services d'accessibilité d'Android pour enregistrer les frappes au clavier et les interactions avec l'interface utilisateur. Après avoir dérobé des identifiants, il désactive la superposition spécifique à cette banque pour éviter de susciter la méfiance. Il peut aussi afficher une fausse mise à jour du système d'exploitation pour masquer ses activités malveillantes en arrière-plan.

Le logiciel malveillant surveille l'activité du téléphone, recueille des informations sur les capteurs, les conditions réseau, les données matérielles et la liste des applications installées, créant ainsi un profil détaillé de l'appareil pour adapter ses tactiques. De plus, il empêche le retrait de ses privilèges administrateur, rendant sa désinstallation manuelle ou via des outils externes difficile.

**Points clés :**

*   Capture des conversations chiffrées sur des applications de messagerie.
*   Détournement d'identifiants bancaires via de fausses interfaces.
*   Prise de contrôle à distance de l'appareil.
*   Ciblage des institutions financières en Europe du Sud et Centrale.
*   Utilisation des services d'accessibilité pour le suivi et l'interception.
*   Mécanismes de protection contre la désinstallation.

**Vulnérabilités exploitées :**

*   Abus des services d'accessibilité Android.
*   Potentiellement, vulnérabilités non spécifiées dans les applications bancaires ciblées.

**Recommandations :**

*   Être vigilant face aux applications inconnues et aux demandes d'autorisations inhabituelles.
*   Privilégier le téléchargement d'applications depuis des sources officielles (Google Play Store).
*   Garder le système d'exploitation et les applications à jour.
*   Ne pas désactiver les services de sécurité intégrés.
*   Vérifier les autorisations accordées aux applications.
*   En cas de suspicion, envisager une réinitialisation d'usine après sauvegarde des données importantes.

---
[Source](https://thehackernews.com/2025/11/new-sturnus-android-trojan-quietly.html){:target="_blank"}
