---
title: 'UNC6384 Deploys PlugX via Captive Portal Hijacks and Valid Certificates Targeting Diplomats'
date: 2025-08-25
permalink: /posts/2025/08/25/unc6384-deploys-plugx-via-captive-portal-hijacks-and-valid-certificates-targeting-diplomats/
tags:
- veille-cyber
- hackernews
---
## Sophistication accrue dans le cyberespionnage : le groupe UNC6384 cible les diplomates

Un acteur de menace lié à la Chine, désigné sous le nom d'UNC6384, déploie des attaques sophistiquées contre des diplomates en Asie du Sud-Est et d'autres entités à travers le monde. Ces opérations visent à servir les intérêts stratégiques de Pékin. Les chercheurs ont observé une chaîne d'attaque en plusieurs étapes exploitant des techniques d'ingénierie sociale avancées, des certificats de signature de code valides, une attaque "adversaire-en-le-milieu" (AitM) et des méthodes d'exécution indirecte pour déjouer la détection. UNC6384 partage des similitudes tactiques et d'outillage avec des groupes de pirates informatiques chinois connus, notamment Mustang Panda.

La campagne, détectée en mars 2025, se caractérise par l'utilisation d'un portail captif détourné pour usurper le trafic web et livrer un téléchargeur signé numériquement, STATICPLUGIN. Ce dernier prépare le terrain pour le déploiement en mémoire d'une variante du malware PlugX (également connu sous le nom de Korplug ou SOGU), dénommée SOGU.SEC.

PlugX est une porte dérobée (backdoor) connue pour ses capacités d'exfiltration de fichiers, d'enregistrement de frappes, de lancement de commandes à distance et d'extension de fonctionnalités via des plugins. Souvent distribué via le "DLL side-loading", le malware est également propagé par des clés USB, des e-mails de phishing contenant des pièces jointes ou des liens malveillants, ou des téléchargements de logiciels compromis.

La méthode d'attaque implique les étapes suivantes :

*   Le navigateur web de la cible vérifie une connexion internet derrière un portail captif.
*   Une attaque AitM redirige le navigateur vers un site web contrôlé par l'attaquant.
*   STATICPLUGIN est téléchargé depuis "mediareleaseupdates[.]com".
*   STATICPLUGIN récupère un paquet MSI du même site.
*   CANONSTAGER est chargé en utilisant la technique du "DLL side-loading" et déploie la charge utile SOGU.SEC en mémoire.

Le détournement du portail captif sert à distribuer le malware déguisé en mise à jour de plugin Adobe. Pour les navigateurs comme Chrome, ce détournement s'effectue via une requête à une URL codée en dur ("www.gstatic[.]com/generate_204"), qui redirige les utilisateurs vers une page de connexion Wi-Fi. Bien que "gstatic[.]com" soit un domaine légitime de Google, les acteurs de la menace profitent de ce mécanisme pour imiter les chaînes de redirection vers leur propre page web. Il est supposé que l'attaque AitM est facilitée par des appareils réseau compromis au sein des réseaux cibles, bien que le vecteur d'accès initial reste inconnu.

La page d'atterrissage imite un site de mise à jour logicielle légitime et utilise une connexion HTTPS avec un certificat TLS valide émis par Let's Encrypt. Le résultat final est le téléchargement d'un exécutable nommé "AdobePlugins.exe" (STATICPLUGIN). Au lancement, celui-ci déclenche la charge utile SOGU.SEC en arrière-plan via le fichier "cnmpaui.dll" (CANONSTAGER), qui utilise le programme "cnmpaui.exe" (Canon IJ Printer Assistant Tool) pour le chargement latéral.

Le téléchargeur STATICPLUGIN est signé par Chengdu Nuoxin Times Technology Co., Ltd, avec un certificat valide délivré par GlobalSign. Plus d'une douzaine d'échantillons de malware signés par Chengdu ont été utilisés par des groupes d'activité liés à la Chine, les premières traces remontant au moins à janvier 2023. La méthode d'obtention de ces certificats par les attaquants n'est pas claire.

L'utilisation combinée de techniques avancées comme l'AitM, de certificats de signature de code valides et d'une ingénierie sociale à plusieurs niveaux démontre les capacités évoluées et la sophistication des acteurs de menace liés à la République Populaire de Chine.

### Points Clés :

*   **Acteur de Menace :** UNC6384 (lié à la Chine), partage des similitudes avec Mustang Panda.
*   **Cible :** Diplomates en Asie du Sud-Est et autres entités mondiales.
*   **Objectif :** Cyberespionnage, avancée des intérêts stratégiques de Pékin.
*   **Malware Principal :** PlugX (SOGU.SEC), une porte dérobée polyvalente.
*   **Techniques Clés :**
    *   Portail captif détourné pour le trafic web.
    *   Attaque "Adversaire-en-le-milieu" (AitM).
    *   Ingénierie sociale (déguisement en mise à jour logicielle).
    *   Certificats de signature de code valides (via Chengdu Nuoxin Times Technology Co., Ltd).
    *   Déploiement en mémoire et "DLL side-loading".
*   **Outils Utilisés :**
    *   STATICPLUGIN (téléchargeur).
    *   CANONSTAGER (DLL de chargement).
    *   "cnmpaui.exe" (Canon IJ Printer Assistant Tool).

### Vulnérabilités :

*   **Aucune vulnérabilité spécifique avec un identifiant CVE n'est explicitement mentionnée dans l'article.** Cependant, l'attaque exploite la fonctionnalité des portails captifs des réseaux Wi-Fi et la confiance accordée aux certificats de signature de code valides. La méthode exacte de compromission des dispositifs réseau facilitant l'AitM n'est pas détaillée.

### Recommandations :

*   **Vigilance accrue face aux mises à jour logicielles inattendues ou demandées par des canaux non officiels.**
*   **Validation rigoureuse de l'authenticité des sites web et des certificats de sécurité, même lorsqu'ils semblent légitimes.**
*   **Mise en place de mesures de sécurité réseau robustes pour prévenir les attaques "Adversaire-en-le-milieu" et la compromission des dispositifs de périmètre.**
*   **Formation continue du personnel sur les techniques d'ingénierie sociale et les tactiques de phishing.**
*   **Surveillance des activités de trafic réseau suspectes et des connexions inhabituelles.**

---
[Source](https://thehackernews.com/2025/08/unc6384-deploys-plugx-via-captive.html){:target="_blank"}
