---
title: '2025: The Untold Stories of Check Point Research'
date: 2026-02-24
permalink: /posts/2026/02/24/2025-the-untold-stories-of-check-point-research/
tags:
- veille-cyber
- zerodaysfans
---
## Paysage des Menaces Cybernétiques en 2025 : Rapports de Check Point Research

L'année 2025 a vu un paysage des menaces cybernétiques complexe et interconnecté, marqué par une convergence d'acteurs étatiques, d'acteurs offensifs privés et de cybercriminels de haut niveau. Les tactiques évoluent moins par l'innovation de nouveaux outils que par la combinaison et l'adaptation de techniques familières, exploitant les plateformes et les méthodes d'accès courantes telles que le cloud, les outils d'administration à distance, le chargement de DLL et l'ingénierie sociale. L'accent est mis sur la durabilité de la visibilité, la réduction des points d'entrée vulnérables et la collaboration sectorielle.

**Points Clés et Vulnérabilités Observées :**

*   **Région Amériques :** Focalisation sur des cibles de grande valeur.
    *   **Exploitation de ToolShell en tant que zero-day :** Attribuée à des acteurs liés à la Chine, visant des organisations gouvernementales nord-américaines via des vulnérabilités non corrigées de Microsoft SharePoint.
        *   **Vulnérabilité :** Connue pour permettre l'exécution de code à distance (RCE) sur des serveurs SharePoint non corrigés. CVE potentielle mentionnée dans une référence : CVE-2025-53770.
    *   **Campagnes d'hameçonnage de Kimsuky :** Ciblant des chercheurs dans des think tanks américains spécialisés dans les affaires nord-coréennes. Utilisation de pages d'atterrissage d'usurpation avec des kits d'attaques par l'homme du milieu (AiTM) pour contourner la MFA et voler des identifiants.
    *   **RedCurl :** Utilisation de fichiers LNK armés pour une chaîne d'infection multi-étapes, exploitant le répertoire de travail pour charger des ressources distantes et potentiellement déployer des ransomwares.

*   **Région Europe :** Mélange de perturbation, d'espionnage, d'opérations d'influence et d'intrusions à motivation financière.
    *   **Camaro Dragon (Mustang Panda) :** Ciblage d'agences gouvernementales européennes avec des e-mails d'hameçonnage sophistiqués menant à des charges utiles PlugX via des pages d'atterrissage hébergées sur Microsoft Azure.
    *   **COLDRIVER :** Persistance des activités malgré l'exposition, avec des campagnes imitant des organisations américaines et ciblant l'Europe du Sud-Est. Adaptation des chaînes de livraison de malware MAYBEROBOT/SIMPLEFIX avec des mesures de sécurité côté attaquant renforcées.
    *   **Lying Pigeon :** Continuation des campagnes d'influence et de désinformation en Moldavie, ciblant les élections parlementaires avec des faux documents et des concours de propagande.
    *   **UAC-0050 :** Campagne d'hameçonnage ciblant l'Ukraine, se faisant passer pour les autorités fiscales ukrainiennes et livrant un outil de support IT à distance via un lien vers un service de partage de fichiers.
    *   **Zipline :** Déplacement du ciblage vers l'Europe, avec des leurres centrés sur les RH et l'utilisation de domaines `herokuapp` pour la communication C2.

*   **Région Asie-Pacifique et Asie Centrale :** Espionnage soutenu par des acteurs liés à la Chine.
    *   **GoldenSMTP :** Évolution de l'IndigoZebra APT, ciblant l'Asie Centrale avec des archives ZIP protégées par mot de passe, le détournement de DLL et un implant basé sur SMTP/IMAP utilisant des comptes e-mail compromis pour le C2. Vérifications des systèmes en langue russe observées.
    *   **Flax Typhoon :** Ciblage de chaînes d'approvisionnement informatiques à Taïwan via l'abus de produits de sécurité légitimes pour une chaîne de chargement de DLL side-loading avec PlugX. Utilisation de l'utilitaire `ns nslookup.exe` pour la communication C2.
    *   **SilverFox :** Exploitation de serveurs PHP compromis pour une exécution de code à distance, suivie de l'installation de l'implant ValleyRAT via `msiexec`. Utilisation de la technique "bring your own vulnerable driver" (BYOVD).
    *   **YoroTrooper :** Ciblage des pays membres de l'Union économique eurasiatique (UEE) et de son organe de réglementation, utilisant des documents PDF pour voler des identifiants ou livrer des RAT via Telegram et Discord pour le C2.
    *   **APT36 :** Campagne d'hameçonnage ciblant l'industrie aérospatiale indienne et les entités gouvernementales, utilisant des pièces jointes ISO avec des fichiers LNK malveillants pour déployer un logiciel espion. Extension de l'activité vers l'Afghanistan.

*   **Région Moyen-Orient et Afrique :** Diversification des menaces avec des APT alignées sur des États, des acteurs offensifs privés (PSOAs) et des acteurs de destruction.
    *   **Acteurs Offensifs Privés :**
        *   **StealthFalcon :** Exploitation de la vulnérabilité CVE-2025-33053, ciblant des organisations de haut profil au Moyen-Orient et en Afrique.
        *   **LANDFALL :** Exploitation d'une vulnérabilité dans l'analyse des fichiers TIFF/DNG par Samsung (CVE-2025-21042) pour cibler les appareils Android.
    *   **Activité Iranienne :**
        *   **Ciblage de caméras israéliennes :** Augmentation des tentatives de compromission de caméras connectées pour l'évaluation des dommages de bombardement, exploitant CVE-2023-6895 et CVE-2017-7921.
        *   **MuddyWater :** Activité de "password spray" et campagne d'hameçonnage en Israël utilisant des leurres Teams et des scripts PowerShell malveillants.
        *   **Nimbus Manticore :** Déploiement de malwares plus sophistiqués, ciblant le nord-est de l'Afrique en imitant T-Mobile.
        *   **Wipers liés à l'Iran :** Campagnes perturbatrices visant Israël avec des wipers et des ransomwares comme 'WhiteLock', déployés après l'infostealer WezRat. Un wiper a été distribué via un installateur `.msi` malveillant.
    *   **WIRTE (associé au Hamas) :** Opérations destructrices continues avec de nouvelles variantes du wiper SameCoin et des campagnes d'espionnage ciblant des entités politiques arabophones. Utilisation du détournement de DLL et d'un loader Havoc, avec une infrastructure C2 hébergée sur DigitalOcean.

**Recommandations Générales :**

*   **Visibilité Durable :** Maintenir une visibilité continue sur l'identité, le cloud et les points d'extrémité.
*   **Réduction des Points d'Entrée :** Fermer rapidement les points d'entrée exposés et non corrigés.
*   **Collaboration Industrielle :** Renforcer la coopération entre les chercheurs en sécurité et les fournisseurs.
*   **Mise à Jour et Correction :** Assurer la mise à jour des systèmes et des logiciels pour corriger les vulnérabilités connues et les zero-days dès que possible.
*   **Sensibilisation à l'Ingénierie Sociale :** Former les utilisateurs à reconnaître et signaler les tentatives d'hameçonnage et d'ingénierie sociale, notamment celles utilisant des plateformes légitimes comme des leurres.
*   **Surveillance des Plateformes Courantes :** Porter une attention particulière aux abus des plateformes cloud pour le C2, des outils d'administration à distance et des techniques de chargement de DLL.

---
[Source](https://research.checkpoint.com/2026/2025-the-untold-stories-of-check-point-research/){:target="_blank"}
