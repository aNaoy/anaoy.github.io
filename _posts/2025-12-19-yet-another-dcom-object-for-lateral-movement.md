---
title: 'Yet another DCOM object for lateral movement'
date: 2025-12-19
permalink: /posts/2025/12/19/yet-another-dcom-object-for-lateral-movement/
tags:
- veille-cyber
- securelist
---
### Nouvelle méthode de mouvement latéral via DCOM et éléments du panneau de configuration

Une nouvelle technique de mouvement latéral a été découverte, exploitant un objet DCOM (Distributed Component Object Model) jusqu'alors méconnu, nommé COpenControlPanel, intégré à `shell32.dll` (CLSID {06622D85-6856-4460-8DE1-A81921B41C4B}). Cet objet permet d'ouvrir des éléments du panneau de configuration via son interface `IOpenControlPanel` et sa fonction `Open`.

Cette découverte s'inscrit dans le contexte du mouvement latéral, où les attaquants cherchent à étendre leur accès au-delà du système initialement compromis. Les objets DCOM ont été historiquement utilisés à cette fin, mais leur efficacité diminue avec les mises à jour de sécurité.

La nouveauté de cette approche réside dans la combinaison de DCOM avec les éléments du panneau de configuration. Les éléments du panneau de configuration (.cpl) sont traditionnellement utilisés pour l'accès initial ou la persistance en étant enregistrés dans des clés de registre spécifiques. Ils sont généralement exécutés via `rundll32.exe`, mais peuvent également être chargés par le processus COM Surrogate (`dllhost.exe`) lorsqu'ils sont associés à des objets COM.

L'objet COpenControlPanel, s'il est accessible à distance (donc en tant que DCOM), peut être utilisé pour déclencher le chargement d'une DLL arbitraire (pas nécessairement un fichier .cpl) enregistrée dans les emplacements de registre dédiés au panneau de configuration. L'appel à la fonction `Open` de cet objet, même avec un nom d'élément du panneau de configuration invalide, suffit à charger toutes les DLLs enregistrées dans ces emplacements dans le processus COM Surrogate.

Cette méthode permet à la fois l'exécution de code à distance et l'établissement de persistance, car la DLL malveillante peut être déclenchée soit par l'ouverture du panneau de configuration par un utilisateur, soit à distance via une connexion DCOM.

**Points clés :**

*   **Mouvement Latéral et Exécution de Commande à Distance :** Utilisation d'objets DCOM pour exécuter du code sur des systèmes distants.
*   **Nouvel Objet DCOM :** COpenControlPanel ({06622D85-6856-4460-8DE1-A81921B41C4B}) exposé par `shell32.dll`.
*   **Exploitation des Éléments du Panneau de Configuration :** Association de DCOM avec les DLLs (.cpl ou autres) enregistrées pour le panneau de configuration.
*   **Chargement de DLL arbitraire :** La fonction `Open` de COpenControlPanel peut charger n'importe quelle DLL enregistrée.
*   **Exécution via COM Surrogate :** Le chargement de la DLL malveillante s'effectue dans le processus `dllhost.exe`.
*   **Persistance :** La technique permet de déclencher l'exécution soit par l'utilisateur, soit à distance via DCOM.
*   **Bypass Potentiel des Défenses :** Les emplacements d'enregistrement des éléments du panneau de configuration peuvent ne pas être entièrement couverts par les solutions de sécurité.

**Vulnérabilités et Exploits :**

*   Bien qu'aucun CVE spécifique ne soit mentionné pour cet objet DCOM lui-même, la vulnérabilité réside dans la manière dont le système Windows gère l'activation et l'exécution des objets DCOM et des éléments du panneau de configuration enregistrés via des clés de registre potentiellement non surveillées.
*   L'exploitation repose sur l'absence de restrictions d'accès par défaut pour les membres du groupe Administrateurs sur cet objet DCOM, permettant une invocation à distance.

**Recommandations :**

*   **Surveillance des Enregistrements du Panneau de Configuration :** Surveiller activement les clés de registre suivantes pour toute modification ou ajout suspect :
    *   `HKCU\Software\Microsoft\Windows\CurrentVersion\Control Panel\Cpls`
    *   `HKLM\Software\Microsoft\Windows\CurrentVersion\Control Panel\Cpls`
    *   `HKLM\Software\WOW6432Node\Microsoft\Windows\CurrentVersion\Control Panel\Cpls`
*   **Surveillance de `dllhost.exe` :** Surveiller le processus COM Surrogate (`dllhost.exe`) pour la détection d'objets COM inhabituels, tels que COpenControlPanel, ou le chargement de DLLs inattendues.
*   **Surveillance du Registre Distant :** Surveiller l'utilisation du service de Registre Distant, car il est souvent utilisé pour manipuler les enregistrements du registre à distance lors de ce type d'attaques.
*   **Durcissement des Configurations :** Mettre en œuvre des pratiques de sécurité robustes pour limiter les privilèges d'accès aux registres et aux objets DCOM.
*   **Surveillance de la Bitness :** Porter une attention particulière au chargement de DLLs 32 bits sur des systèmes x64, car cela peut indiquer une activité suspecte (processus `dllhost.exe *32`).

---
[Source](https://securelist.com/lateral-movement-via-dcom-abusing-control-panel/118232/){:target="_blank"}
