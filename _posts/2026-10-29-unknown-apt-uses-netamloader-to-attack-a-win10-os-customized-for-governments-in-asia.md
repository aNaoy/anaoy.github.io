---
title: 'Unknown APT uses NetamLoader to attack a Win10 OS customized for governments in Asia'
date: 2026-10-29
permalink: /posts/2026/10/29/unknown-apt-uses-netamloader-to-attack-a-win10-os-customized-for-governments-in-asia/
tags:
- veille-cyber
- securelist
---
### NetamLoader : Une campagne d'espionnage sophistiquée ciblant des systèmes gouvernementaux

Une nouvelle campagne d'attaque par chaîne d'approvisionnement a été identifiée, visant spécifiquement une version personnalisée de Windows utilisée par des entités gouvernementales en Asie. Le malware, baptisé **NetamLoader**, utilise un cadre de chargement .NET complexe reposant sur des fichiers XAML et des techniques d'injection avancées pour rester furtif.

#### Points clés
*   **Vecteur d'infection :** Le malware est distribué via un fichier CAB placé dans le répertoire des mises à jour Windows, utilisant des composants légitimes pour masquer son activité.
*   **Architecture modulaire :** L'infection se déroule en plusieurs étapes utilisant des fichiers XAML chiffrés, des plugins .NET et des configurations JSON.
*   **Furtivité :** Le malware utilise des techniques de contournement AMSI (Antimalware Scan Interface), désactive les logs ETW (Event Tracing for Windows), nettoie les traces système (Prefetch, logs d'update) et migre son exécution dans le processus `dllhost.exe` pour échapper aux EDR.
*   **Persistance et C2 :** Le malware adopte des délais de communication très longs (jusqu'à 28 heures) pour éviter la détection en sandbox et utilise un canal de communication chiffré (AES-128-CBC + HMAC) vers un serveur C2 hébergé via Cloudflare.

#### Vulnérabilités exploitées
*   **AppDomainManager Injection :** Détournement du chargement des assemblies .NET via des fichiers de configuration (`.config`).
*   **Désérialisation non sécurisée :** Utilisation de la classe `BinaryFormatter` (vulnérabilité critique, bien que non listée par un CVE spécifique, elle est liée aux risques de **TypeConfuseDelegate**).
*   **Défaut de conception (Microsoft.HostIntegration.Connectors) :** Abus du comportement de `DataCacheFactoryConfiguration` pour charger des bibliothèques arbitraires.

#### Recommandations
*   **Durcissement des configurations .NET :** Surveiller et restreindre l'utilisation des `AppDomainManager` et auditer les fichiers `.config` dans les répertoires de mise à jour système.
*   **Désactivation de BinaryFormatter :** Éviter l'utilisation de `BinaryFormatter` dans les applications .NET et migrer vers des sérialiseurs plus sécurisés (ex: System.Text.Json).
*   **Surveillance comportementale :** Mettre en place des alertes EDR sur :
    *   L'exécution de `PatchMyPC-ScriptRunner.exe` avec des arguments inhabituels.
    *   La modification des tables de méthodes virtuelles (VTable) ou le patching mémoire des APIs liées à AMSI (`CAmsiAntimalware::Scan`).
    *   La création de processus isolés via RPC ou le chargement de fichiers XAML via `XamlReader.Load()`.
*   **Analyse des logs :** Surveiller les suppressions suspectes de clés de registre liées aux GUIDs (générés dynamiquement selon le C2) et les accès aux répertoires de maintenance `SoftwareDistribution`.

---
[Source](https://securelist.com/netamloader/121676/){:target="_blank"}
