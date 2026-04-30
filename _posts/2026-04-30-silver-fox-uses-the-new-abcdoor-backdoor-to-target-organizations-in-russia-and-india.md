---
title: 'Silver Fox uses the new ABCDoor backdoor to target organizations in Russia and India'
date: 2026-04-30
permalink: /posts/2026/04/30/silver-fox-uses-the-new-abcdoor-backdoor-to-target-organizations-in-russia-and-india/
tags:
- veille-cyber
- securelist
---
### Analyse de la campagne cybercriminelle du groupe Silver Fox

Le groupe de menace Silver Fox cible des organisations en Inde, en Russie et au Japon par des campagnes de phishing massives exploitant la confiance des utilisateurs envers les autorités fiscales. Les attaquants utilisent des documents (PDF) contenant des liens malveillants pour contourner les passerelles de sécurité, incitant les victimes à télécharger des archives contenant un chargeur (« loader ») personnalisé basé sur RustSL.

#### Points clés
*   **Mode opératoire :** Utilisation de l'ingénierie sociale (prétextes de violations fiscales) et de liens intégrés dans des PDF pour éviter la détection des pièces jointes malveillantes.
*   **Charge utile :** Le chargeur RustSL (modifié par Silver Fox) déploie le backdoor ValleyRAT (Winos 4.0), qui télécharge ensuite un nouveau malware non documenté baptisé **ABCDoor**.
*   **ABCDoor :** Un backdoor Python complexe, modulaire et persistant, capable de capturer des écrans (via ffmpeg), d'exfiltrer des données et de prendre le contrôle distant. Il utilise le nom de processus `appclient` et se dissimule parfois en imitant le répertoire du logiciel légitime *Tailscale*.
*   **Évolution :** Le groupe a ajouté des techniques de persistance sophistiquées comme la « Phantom Persistence » (abus du processus d'extinction système pour redémarrer le malware).

#### Vulnérabilités et techniques exploitées
*   **Techniques d'évasion :** Géofencing (vérification du pays cible via des services IP publics), détection de sandboxes/machines virtuelles intégrée au chargeur RustSL.
*   **Persistence :** Utilisation du registre Windows (`HKCU\Software\Microsoft\Windows\CurrentVersion\Run`), du planificateur de tâches (`schtasks`) et de la technique *Phantom Persistence* (interception du signal d'arrêt système).
*   **CVE :** Aucune CVE spécifique n'est citée ; les attaquants privilégient l'exécution de code légitime (PowerShell, Node.js, outils système) pour maintenir une empreinte discrète.

#### Recommandations
*   **Sensibilisation :** Former le personnel à la vigilance concernant les emails officiels non sollicités, particulièrement ceux contenant des liens de téléchargement de documents administratifs.
*   **Filtrage :** Renforcer la sécurité des passerelles email pour bloquer les domaines non fiables et analyser systématiquement les liens contenus dans les PDF.
*   **Surveillance système :**
    *   Détecter l'installation ou l'exécution suspecte de `node.exe` depuis des répertoires non standards (`%USERPROFILE%\.node\`).
    *   Surveiller les modifications suspectes du registre liées à la persistance (`UserInitMprLogonScript`, clés `...\Run`).
    *   Bloquer ou surveiller les requêtes sortantes vers des services de géolocalisation IP (ex: `ip-api.com`, `ipinfo.io`) initiées par des processus autres que des navigateurs web.
*   **Segmentation :** Restreindre les privilèges d'exécution des scripts (PowerShell, Node.js) sur les postes de travail des employés ne nécessitant pas ces outils pour leurs fonctions.

---
[Source](https://securelist.com/silver-fox-tax-notification-campaign/119575/){:target="_blank"}
