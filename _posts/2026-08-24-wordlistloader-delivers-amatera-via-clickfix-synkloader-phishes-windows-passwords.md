---
title: 'WordlistLoader Delivers Amatera via ClickFix, SynkLoader Phishes Windows Passwords'
date: 2026-08-24
permalink: /posts/2026/08/24/wordlistloader-delivers-amatera-via-clickfix-synkloader-phishes-windows-passwords/
tags:
- veille-cyber
- hackernews
---
### Menaces émergentes : WordlistLoader et SynkLoader

Deux nouvelles familles de logiciels malveillants, **WordlistLoader** et **SynkLoader**, ont été identifiées. Elles servent de vecteurs d'infection pour des charges utiles secondaires, telles que le voleur d'informations *Amatera*, et sont probablement utilisées pour fournir un accès initial à des groupes de rançongiciels.

#### Points clés
*   **WordlistLoader** : Utilisé dans les campagnes *ClearFake* exploitant la technique "ClickFix". Les victimes sont incitées par de faux CAPTCHA à exécuter des commandes PowerShell dissimulées via une interface WebDAV. Le chargeur reconstruit un shellcode à partir d'une liste de mots ou de segments UUID pour contourner l'analyse statique et les outils de détection (ETW).
*   **SynkLoader** : Diffusé via des campagnes de phishing sur Microsoft Teams en usurpant l'identité d'un service informatique. Le malware déploie un installateur MSI contenant un chargeur Python capable de télécharger divers modules malveillants (RAT, proxy inverse, VNC).
*   **Tactiques communes** : Utilisation d'infrastructures légitimes (CDN jsDelivr, stockage Azure, blockchain via EtherHiding) pour héberger des scripts malveillants et contourner les filtres de sécurité.

#### Vulnérabilités et techniques exploitées
Aucune CVE spécifique n'est mentionnée, car ces attaques reposent sur l'ingénierie sociale (abus de confiance) et des techniques de vie sur le système (Living-off-the-Land) :
*   **ClickFix (FakeCaptcha)** : Manipulation de l'utilisateur pour copier/coller et exécuter des commandes malveillantes via `cmd.exe`.
*   **Dérivation d'ETW** : Utilisation de points d'arrêt matériels pour neutraliser le traçage des événements Windows.
*   **Techniques d'évasion** : Usage de `Heaven's Gate`, exécution en mémoire sans fichier sur disque (fileless) et injection dynamique.

#### Recommandations
*   **Sensibilisation** : Former les utilisateurs à se méfier des invites de sécurité ou de CAPTCHA inattendues, particulièrement celles demandant une interaction avec le terminal ou PowerShell.
*   **Contrôle des accès** : Restreindre l'exécution des scripts PowerShell et l'utilisation de `rundll32.exe` via des politiques de contrôle d'application (AppLocker ou Windows Defender Application Control).
*   **Filtrage réseau** : Bloquer les connexions sortantes vers les partages WebDAV externes suspects et surveiller les communications vers des services de stockage cloud non autorisés.
*   **Sécurité des endpoints** : Maintenir les solutions EDR/XDR à jour pour détecter les comportements suspects tels que l'exécution de processus masqués (`conhost.exe --headless`) ou la création de tâches planifiées inhabituelles.

---
[Source](https://thehackernews.com/2026/08/wordlistloader-delivers-amatera-via.html){:target="_blank"}
