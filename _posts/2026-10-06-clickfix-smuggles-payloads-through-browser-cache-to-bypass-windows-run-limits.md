---
title: 'ClickFix Smuggles Payloads Through Browser Cache to Bypass Windows Run Limits'
date: 2026-10-06
permalink: /posts/2026/10/06/clickfix-smuggles-payloads-through-browser-cache-to-bypass-windows-run-limits/
tags:
- veille-cyber
- hackernews
---
### L'évolution des attaques ClickFix : de la manipulation psychologique au cache des navigateurs

Les attaques « ClickFix » se sont perfectionnées en exploitant le cache des navigateurs pour contourner les limitations de saisie de la boîte de dialogue « Exécuter » de Windows (limitée à 260 caractères). Au lieu de télécharger un fichier malveillant, le site compromis pré-enregistre un script dans le cache (souvent déguisé en fichier PNG). Lorsqu'une victime exécute la commande fournie par l'attaquant, le système lance le code déjà présent localement, facilitant ainsi l'injection de charges utiles complexes et furtives.

**Points clés :**
*   **Technique de "cache smuggling" :** Le script malveillant est caché dans le cache du navigateur, permettant d'exécuter des charges utiles volumineuses sans dépasser les limites de Windows.
*   **Ingénierie sociale :** Les attaquants se font passer pour des erreurs système, des captchas ou des mises à jour de navigateur, incitant l'utilisateur à copier-coller des commandes dans PowerShell ou la console Windows.
*   **Weaponisation de l'IA :** Des systèmes de résumé automatique par IA peuvent être manipulés via des injections invisibles (CSS, textes blancs, etc.) pour générer des instructions ClickFix trompeuses.
*   **Automatisation :** L'utilisation de kits de phishing (type IUAM) a largement démocratisé ces attaques, favorisant leur adoption par des groupes étatiques (ex: Stardust Chollima, Sandworm).

**Vulnérabilités :**
*   **CVE-2026-6854 :** Vulnérabilité exploitée dans des plugins WordPress pour compromettre des sites et injecter les leurres ClickFix.
*   **Abus de fonctionnalités légitimes :** L'attaque repose sur l'abus détourné d'outils systèmes de confiance (Windows Run, PowerShell, WMI, VBScript).

**Recommandations :**
*   **Sensibilisation :** Éduquer les utilisateurs sur le fait qu'aucun processus légitime (CAPTCHA, erreur système) ne demande de copier-coller du code ou des commandes dans une console ou un terminal.
*   **Contrôles techniques :**
    *   Activer la journalisation des blocs de scripts PowerShell (Script Block Logging).
    *   Renforcer le contrôle des applications (Application Control).
    *   Déployer des protections web et réseau avancées.
*   **Chasse aux menaces (Threat Hunting) :** Surveiller les activités suspectes liées au cache du navigateur, les clés de registre `RunMRU`, l'utilisation anormale de `WScript.exe`/`PowerShell.exe` en tant que processus enfants, et l'apparition de tâches planifiées inhabituelles.

---
[Source](https://thehackernews.com/2026/10/clickfix-smuggles-payloads-through.html){:target="_blank"}
