---
title: 'Dissecting DCOM part 1'
date: 2025-09-15
permalink: /posts/2025/09/15/dissecting-dcom-part-1/
tags:
- veille-cyber
- zerodaysfans
---
### Exploration Approfondie de DCOM et de ses Mécanismes d'Interaction

Cet article dissèque le fonctionnement interne du Component Object Model (COM) et de sa variante distribuée, DCOM, des technologies fondamentales de Windows. Il détaille l'historique de ces technologies, depuis les premiers échanges entre processus comme le presse-papiers jusqu'à la gestion de composants logiciels complexes et distribués.

L'article explique la nécessité de mécanismes d'identification uniques pour les classes et les interfaces, tels que les CLSID, ProgID et AppID, et comment ceux-ci sont enregistrés dans le registre Windows. Des outils comme OleView.NET sont présentés comme des moyens efficaces pour découvrir et interagir avec ces composants.

L'instanciation des objets COM/DCOM est abordée sous divers angles : par l'utilisation de PowerShell avec des identifiants CLSID ou ProgID, l'invocation directe de fonctions Windows API comme `CoCreateInstance` et `CoCreateInstanceEx`, ou encore l'utilisation de `rundll32`. Les techniques de persistance via les tâches planifiées exploitant des `ComHandler` sont également mentionnées.

L'importance des interfaces et de la manière dont elles structurent la communication (via l'interface `IUnknown` et la définition en IDL) est soulignée. Les différences entre les composants "in-process" (DLL) et "out-of-process" (EXE) sont expliquées, notamment les mécanismes d'activation spécifiques à chaque type, y compris les protocoles RPC utilisés pour la communication à distance avec des interfaces comme `IOXIDResolver`, `IActivation` et `IRemoteSCMActivator`. La structure des `OBJREF` et leur rôle dans la création de proxys pour les objets distants sont également décrits.

**Points Clés :**

*   **Origines de COM/DCOM :** Évolution des mécanismes d'inter-processus (DDE, OLE) vers des architectures de composants distribués.
*   **Identifiants Clés :** CLSID, ProgID, AppID pour l'identification unique des classes. IID pour les interfaces.
*   **Localisation Transparente :** Principe fondamental de COM permettant d'interagir avec des objets sans connaître leur emplacement physique.
*   **Marshalling et Garbage Collection :** Concepts cruciaux pour la communication distribuée.
*   **Interopérabilité :** Utilisation d'IDL et de bibliothèques de types (TLB) pour faciliter la communication inter-langages.
*   **Types de Composants :** Distinction entre composants "in-process" (DLLs) et "out-of-process" (EXEs).
*   **Activation Distribuée :** Processus impliquant `RPCSS.exe` et des interfaces RPC spécifiques pour la création d'objets distants.
*   **OBJREF :** Structure permettant de référencer ou d'embarquer des objets COM/DCOM pour une utilisation distante ou locale.

**Vulnérabilités Potentielles (Implicites) :**

Bien que non explicitement détaillées avec des CVE dans cette première partie, les mécanismes décrits ouvrent la porte à diverses vulnérabilités :

*   **Détournement d'instanciation :** L'instanciation d'objets COM arbitraires via des ProgID ou CLSID contrôlés peut mener à l'exécution de code.
*   **Abus des tâches planifiées :** L'enregistrement de CLSID malveillants pour des tâches planifiées permet la persistance et l'exécution de code.
*   **Exposition d'informations sensibles via `IOXIDResolver` :** La méthode `ServerAlive2()` peut révéler les interfaces réseau d'une machine, facilitant la reconnaissance et les mouvements latéraux.
*   **Sérialisation/Désérialisation dangereuse :** Le traitement de `OBJREF` malformés ou provenant de sources non fiables peut conduire à des vulnérabilités.

**Recommandations (Implicites) :**

*   **Gestion des permissions DCOM :** Assurer une configuration sécurisée des permissions pour l'activation et l'accès aux objets DCOM.
*   **Surveillance des enregistrements COM :** Surveiller les modifications suspectes dans le registre liées aux CLSID, ProgID et AppID.
*   **Application des correctifs de sécurité :** Maintenir le système à jour pour se prémunir contre les vulnérabilités connues affectant COM/DCOM.
*   **Principe de moindre privilège :** Exécuter les services et applications utilisant COM/DCOM avec les privilèges minimaux nécessaires.
*   **Sécurisation des communications RPC :** Utiliser des protocoles sécurisés lorsque DCOM est utilisé sur un réseau.

---
[Source](https://www.synacktiv.com/en/publications/dissecting-dcom-part-1){:target="_blank"}
