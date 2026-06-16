---
title: 'From a VHDX File to a Remcos RAT, (Tue, Jun 16th)'
date: 2026-06-16
permalink: /posts/2026/06/16/from-a-vhdx-file-to-a-remcos-rat-tue-jun-16th/
tags:
- veille-cyber
- sans-isc
---
### Propagation de Remcos RAT via des images disques VHDX

Une nouvelle campagne d'infection utilise des fichiers VHDX (disques virtuels) distribués dans des archives ZIP pour contourner les contrôles de sécurité périmétriques. Une fois monté, le fichier VHDX révèle un script JavaScript malveillant qui déclenche une chaîne d'exécution complexe visant à installer le cheval de Troie d'accès à distance (RAT) **Remcos**.

**Points clés :**
*   **Contournement EDR :** L'utilisation de WMI (`Win32_Process.Create`) pour lancer PowerShell masque la relation parent-enfant habituelle des processus, trompant les règles de détection classiques.
*   **Obfuscation multicouche :** Le malware utilise plusieurs niveaux d'obfuscation (concaténation de chaînes, encodage Base64, clés XOR statiques "Identificational" et ajout de texte parasite comme "bubble").
*   **Infection furtive :** Le payload final est injecté directement dans le processus système `backgroundTaskHost.exe` et assure sa persistance via une clé de registre `Run` pointant vers un script PowerShell.
*   **Infrastructure :** Les payloads sont récupérés via des domaines tels que `cembusconfort[.]ro` et communiquent avec un serveur C2 hébergé sur `animal342[.]duckdns[.]org`.

**Vulnérabilités exploitées :**
*   **Montage automatique des VHDX :** Les systèmes Windows modernes montent automatiquement les fichiers VHDX, facilitant l'exécution immédiate du code malveillant.
*   **Abus de fonctionnalités légitimes :** Utilisation détournée des services WMI et des capacités de chargement d'assemblage .NET (`System.Reflection.Assembly.Load()`) pour charger du code arbitraire en mémoire.
*   *Note : Aucune CVE spécifique n'est citée dans l'article, il s'agit d'une exploitation de comportements système par défaut.*

**Recommandations :**
*   **Restreindre les montages :** Limiter les droits des utilisateurs pour monter des fichiers images (VHDX, ISO, IMG) ou bloquer ces extensions au niveau de la passerelle de messagerie.
*   **Surveillance EDR avancée :** Configurer les outils de détection pour surveiller les appels WMI suspects et l'exécution de scripts PowerShell codés en Base64 ou utilisant des techniques de chargement en mémoire (`Reflection.Assembly`).
*   **Filtrage réseau :** Bloquer les connexions sortantes vers les services de DNS dynamique (ex: `duckdns.org`) à partir des postes de travail.
*   **Hygiène des terminaux :** Auditer régulièrement la clé de registre `HKCU\Software\Microsoft\Windows\CurrentVersion\Run` à la recherche de scripts PowerShell suspects ou de chemins d'exécution inhabituels.

---
[Source](https://isc.sans.edu/diary/rss/33080){:target="_blank"}
