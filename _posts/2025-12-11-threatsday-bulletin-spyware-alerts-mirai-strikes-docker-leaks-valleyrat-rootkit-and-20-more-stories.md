---
title: 'ThreatsDay Bulletin: Spyware Alerts, Mirai Strikes, Docker Leaks, ValleyRAT Rootkit — and 20 More Stories'
date: 2025-12-11
permalink: /posts/2025/12/11/threatsday-bulletin-spyware-alerts-mirai-strikes-docker-leaks-valleyrat-rootkit-and-20-more-stories/
tags:
- veille-cyber
- hackernews
---
## Tendances et Vulnérabilités Cybersécurité : Un Aperçu Hebdomadaire

Le paysage de la cybersécurité évolue rapidement, avec des acteurs malveillants exploitant diverses techniques pour compromettre des systèmes et voler des données. Cette semaine, les menaces incluent de nouvelles variantes de botnets, des vulnérabilités dans les systèmes IoT maritimes, des outils de piratage sophistiqués et des fraudes bancaires sophistiquées. Les grandes plateformes technologiques et les régulateurs travaillent à renforcer la sécurité, tout en abordant les implications de la confidentialité et de la vie privée.

**Points Clés :**

*   **Exploitation de vulnérabilités dans l'IoT maritime :** Une nouvelle variante du botnet Mirai, nommée Broadside, cible les appareils IoT maritimes, exploitant des vulnérabilités critiques pour prendre le contrôle et voler des identifiants.
*   **Persistance des failles dans les IA génératives :** Les injections de prompts dans les applications d'IA générative sont jugées difficiles à atténuer entièrement, nécessitant des approches de conception système plus robustes.
*   **Lutte contre la "Violence-as-a-Service" (VaaS) :** Une opération mondiale a conduit à 193 arrestations, démantelant des réseaux criminels recrutant de jeunes individus pour commettre des actes violents.
*   **Outils de piratage saisis :** Trois ressortissants ukrainiens ont été arrêtés en Pologne en possession d'un arsenal d'équipements de piratage potentiellement destinés à perturber des systèmes informatiques stratégiques.
*   **Vol et vente de données massifs :** Un jeune pirate informatique a été arrêté en Espagne pour le vol et la tentative de vente de millions d'enregistrements de données issus de neuf entreprises. Parallèlement, un cybercriminel ukrainien a été arrêté pour l'utilisation de malwares personnalisés afin de pirater et vendre des comptes utilisateurs.
*   **Fraude bancaire via des applications malveillantes :** Un réseau criminel en Russie a été démantelé pour avoir volé des millions à des clients bancaires en utilisant des malwares exploitant le protocole NFC, déguisés en applications bancaires légitimes.
*   **Propagation de botnets via une faille React :** Une faille de sécurité dans React (React2Shell, CVE-2025-55182) est largement exploitée pour infecter des appareils connectés et déployer des botnets comme Mirai et RondoDox.
*   **Malwares furtifs pour Linux :** Des chercheurs ont découvert GhostPenguin, un nouveau cheval de Troie pour Linux, et FlipSwitch, une technique d'accrochage de système d'appel permettant aux rootkits de se cacher plus efficacement.
*   **Blanchiment de cryptomonnaies :** Un individu a plaidé coupable de conspiration RICO pour avoir blanchi 3,5 millions de dollars en cryptomonnaies au nom d'une organisation criminelle.
*   **Notifications de spyware mondiales :** Apple et Google ont émis des alertes à de nombreux utilisateurs dans près de 80 pays concernant des menaces potentielles de spyware.
*   **Nouveau modèle publicitaire pour Meta :** La Commission européenne a approuvé une proposition de Meta offrant aux utilisateurs un choix entre le partage de moins de données avec une publicité moins personnalisée, ou le consentement total pour une publicité ciblée.
*   **Alerte sur le logiciel espion Lumma Stealer :** La Nouvelle-Zélande a alerté environ 26 000 utilisateurs infectés par Lumma Stealer, un logiciel malveillant conçu pour voler des informations sensibles.
*   **Correction d'une faille de détournement dans Notepad++ :** Une mise à jour de Notepad++ (version 8.8.9) corrige une vulnérabilité critique permettant le détournement de trafic et la distribution de malwares.
*   **Durée de vie accrue des canaux Telegram criminels :** Une analyse révèle que la durée de vie moyenne des canaux Telegram dédiés à la cybercriminalité a augmenté, bien que l'application semble renforcer ses contrôles.
*   **Sanctions britanniques contre des acteurs de guerre de l'information :** Le Royaume-Uni a imposé des sanctions contre des organisations russes et chinoises accusées de déstabilisation par le biais de cyberattaques et d'opérations d'influence.
*   **Vulnérabilités Log4Shell persistantes :** Environ 13% des téléchargements de Log4j en 2025 restent vulnérables à Log4Shell, représentant un risque évitable.
*   **Inde envisage un suivi de localisation permanent :** Le gouvernement indien examine une proposition pour activer en permanence le suivi de localisation par satellite sur les smartphones, une idée contestée par les fabricants et les défenseurs des droits de l'homme.
*   **Piquent d'attaques contre GlobalProtect :** Une vague importante de tentatives de connexion à des portails GlobalProtect de Palo Alto Networks a été observée, attribuée au même acteur malveillant que des attaques antérieures contre SonicWall.
*   **OpenAI renforce la cybersécurité :** OpenAI investit dans des mesures pour améliorer la résilience face aux cybercapacités avancées de ses modèles d'IA, visant à favoriser les usages défensifs.
*   **Malware Android DroidLock simulant des rançongiciels :** DroidLock peut verrouiller les écrans d'appareils Android et voler des identifiants d'applications, offrant un contrôle total sur l'appareil compromis.
*   **Google renforce la validation HTTPS :** Chrome et le CA/Browser Forum retirent 11 méthodes obsolètes de validation de contrôle de domaine pour les certificats TLS, renforçant ainsi la sécurité.
*   **Agent Tesla distribué via des torrents :** Une nouvelle campagne utilise un faux torrent de film pour distribuer le malware Agent Tesla, conçu pour donner un accès complet aux ordinateurs Windows.
*   **Secrets exposés dans des images Docker Hub :** Plus de 10 000 images Docker Hub exposent des identifiants de production, des clés LLM et d'autres secrets, révélant un décalage entre l'adoption de l'IA et les contrôles de sécurité.
*   **Trojans déguisés en PNG dans des extensions VS Code :** 19 extensions malveillantes ont été découvertes sur le marketplace de Visual Studio Code, cachant des malwares qui se font passer pour des images PNG.
*   **Analyse du constructeur ValleyRAT :** Une analyse du constructeur ValleyRAT révèle des capacités avancées, y compris un rootkit noyau capable de contourner les protections intégrées de Windows.
*   **Guides IA pour diffuser des voleurs d'informations :** Des acteurs malveillants exploitent les fonctionnalités de partage de conversations sur les plateformes d'IA pour diffuser des malwares voleurs d'informations, tels qu'AMOS Stealer, sous couvert de guides de dépannage.

**Vulnérabilités (avec CVE si applicable) :**

*   **CVE-2024-3721 :** Vulnérabilité critique dans TBK DVR, exploitée par la nouvelle variante Mirai Broadside.
*   **React2Shell (CVE-2025-55182) :** Faille de sécurité dans React, largement exploitée pour la propagation de botnets.
*   **Log4Shell :** Vulnérabilité persistante dans les versions obsolètes de Log4j.

**Recommandations :**

*   **Maintenir à jour les logiciels :** Appliquer les correctifs de sécurité dès leur publication, comme pour Notepad++.
*   **Vérifier l'authenticité des mises à jour :** S'assurer de la validité des certificats et des signatures lors du téléchargement de mises à jour logicielles.
*   **Être vigilant face aux injections de prompts :** Adopter des pratiques de conception sécurisées pour les systèmes d'IA générative.
*   **Utiliser des solutions de sécurité robustes :** Déployer des antivirus, des pare-feu et des systèmes de détection d'intrusions à jour.
*   **Sécuriser les conteneurs et les environnements cloud :** Examiner attentivement les images Docker Hub et mettre en place des contrôles d'accès stricts.
*   **Se méfier des liens et des fichiers suspects :** Éviter de télécharger des fichiers provenant de sources non fiables, notamment via des torrents ou des publicités malveillantes.
*   **Contrôler les autorisations des applications :** Examiner attentivement les autorisations demandées par les applications, particulièrement sur Android.
*   **Prudence avec les plateformes d'IA :** Se méfier des guides de dépannage partagés sur des plateformes d'IA, qui peuvent contenir des instructions malveillantes.
*   **Diversifier les mesures de sécurité :** Utiliser des solutions de sécurité multicouches, y compris pour la protection des systèmes Linux.
*   **Sensibilisation aux risques :** Informer les utilisateurs sur les nouvelles menaces, les techniques d'ingénierie sociale et les risques liés aux données personnelles.

---
[Source](https://thehackernews.com/2025/12/threatsday-bulletin-spyware-alerts.html){:target="_blank"}
