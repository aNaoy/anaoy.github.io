---
title: 'Notepad++ fixes flaw that let attackers push malicious update files'
date: 2025-12-12
permalink: /posts/2025/12/12/notepad-fixes-flaw-that-let-attackers-push-malicious-update-files/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilité dans Notepad++ Permettant la Distribution de Mises à Jour Malveillantes

Une faille de sécurité dans l'outil de mise à jour automatique de Notepad++, WinGUp, a permis à des attaquants de distribuer des exécutables malveillants se faisant passer pour des mises à jour légitimes. Des incidents ont été rapportés où l'outil a téléchargé et exécuté un fichier nommé `AutoUpdater.exe` depuis le répertoire temporaire de l'utilisateur. Ce malware a ensuite collecté des informations système via des commandes comme `netstat`, `systeminfo`, `tasklist` et `whoami`, puis les a exfiltrées vers un site de partage de fichiers, `temp.sh`.

Des chercheurs et des utilisateurs ont soulevé la possibilité d'un détournement du trafic réseau ou de l'installation d'une version non officielle et compromise de Notepad++. Les attaquants pourraient potentiellement intercepter le trafic de mise à jour pour rediriger les téléchargements vers des emplacements malveillants en modifiant les informations de localisation renvoyées par le serveur de mise à jour.

**Points Clés :**

*   **Mise à jour compromettue :** L'outil de mise à jour automatique de Notepad++ a été utilisé pour télécharger et exécuter des fichiers malveillants.
*   **Collecte d'informations :** Le malware récupérait des données système sensibles.
*   **Exfiltration de données :** Les informations collectées étaient envoyées vers un service externe.
*   **Ciblage :** Des incidents ont été observés dans des organisations ayant des liens avec l'Asie de l'Est, suggérant une attaque ciblée.
*   **Mécanisme d'attaque :** La faiblesse réside dans la redirection potentielle des URL de téléchargement des mises à jour.

**Vulnérabilités :**

*   Bien qu'aucun CVE spécifique ne soit mentionné dans l'article, la faille concerne la **vérification insuffisante de l'authenticité des mises à jour** par l'outil WinGUp, permettant l'exécution d'exécutables non signés ou malveillants.

**Recommandations :**

*   **Mettre à jour vers Notepad++ version 8.8.9 ou ultérieure :** Cette version corrige la faille en introduisant une vérification stricte de la signature et du certificat des installateurs téléchargés. Toute vérification échouée entraînera l'annulation de la mise à jour.
*   **S'assurer que les binaires officiels sont signés :** Les versions récentes de Notepad++ (depuis v8.8.7) utilisent des signatures valides.
*   **Supprimer les certificats racines personnalisés anciens :** Les utilisateurs ayant installé des certificats racines personnalisés plus anciens devraient les supprimer pour éviter d'éventuels conflits ou détournements.
*   **Vigilance accrue :** Les utilisateurs doivent rester attentifs à toute activité inhabituelle lors des mises à jour.

---
[Source](https://www.bleepingcomputer.com/news/security/notepad-plus-plus-fixes-flaw-that-let-attackers-push-malicious-update-files/){:target="_blank"}
