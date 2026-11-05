---
title: 'The SOC Files 5: Ghost in the pipeline, or a fileless SharePoint breach by Storm-2603'
date: 2026-11-05
permalink: /posts/2026/11/05/the-soc-files-5-ghost-in-the-pipeline-or-a-fileless-sharepoint-breach-by-storm-2603/
tags:
- veille-cyber
- securelist
---
### Analyse de l'attaque "Ghost in the Pipeline" par le groupe Storm-2603

L'acteur de menace Storm-2603 a mené une campagne d'intrusion sophistiquée visant des serveurs Microsoft SharePoint sur site en 2025. L'attaque se caractérise par une exécution de code sans fichier (fileless) et une exploitation "stratégique" s'étalant sur plusieurs jours pour éviter la détection.

#### Points clés
*   **Tactique de furtivité :** L'attaquant utilise un délai entre la reconnaissance et l'exploitation pour minimiser les corrélations d'alertes.
*   **Architecture "Fileless" :** La charge utile est injectée directement dans le processus `w3wp.exe` (IIS) via une manipulation du runtime ASP.NET. Aucun artefact n'est écrit sur le disque lors de l'accès initial.
*   **Outils de persistance :** Utilisation détournée de frameworks légitimes (Velociraptor, Zoho Assist, VS Code Tunneling, Cloudflare Tunnel) pour maintenir l'accès après l'exploitation initiale.
*   **Élévation de privilèges :** Exploitation du protocole EFSRPC (variante d'EfsPotato) pour usurper des jetons système depuis le processus IIS.
*   **Cible finale :** Tentative de déploiement du ransomware Warlock, bloquée par les solutions EDR.

#### Vulnérabilités exploitées
*   **CVE-2025-53770 & CVE-2025-53771 :** Vulnérabilités critiques dans le composant "ToolPane" de SharePoint permettant l'exécution de code à distance (RCE) via des requêtes HTTP contrefaites.
*   **CVE-2025-6264 :** Vulnérabilité exploitée dans une version obsolète de Velociraptor pour faciliter l'exécution de commandes.

#### Recommandations de sécurité
1.  **Détection de la désérialisation :** Surveiller la présence d'assemblages générés (`App_Web_*.dll`, `Microsoft.GeneratedCode`) et l'utilisation de types dangereux (`ObjectDataProvider`, `ExpandedWrapper`, `LosFormatter`) en mémoire via des outils comme *CLRDeserializationExploitFinder*.
2.  **Surveillance des VirtualPathProvider (VPP) :** Auditer les enregistrements de VPP. Une anomalie se détecte par une divergence entre IIS (qui résout un chemin virtuel) et le système de fichiers (absence de fichier physique et absence de moniteur de changement de fichier associé).
3.  **Analyse des logs ETW :** Utiliser les événements IIS (Event IDs 25, 47) pour identifier les ressources résolues par configuration qui ne correspondent pas à des fichiers réels.
4.  **Réponse post-compromission :** En cas d'exploitation confirmée, procéder à une rotation des *MachineKey*, une chasse aux persistance (tunnels, nouveaux comptes administratifs créés via SAM RPC) et un confinement immédiat des serveurs touchés.
5.  **Hygiène réseau :** Restreindre les communications sortantes des serveurs SharePoint et surveiller les connexions inhabituelles vers des nœuds de réseaux anonymes (SPN) ou des services de tunneling.

---
[Source](https://securelist.com/storm-2603-fileless-toolshell-attack/121467/){:target="_blank"}
