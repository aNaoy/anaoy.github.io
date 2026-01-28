---
title: 'Mustang Panda Deploys Updated COOLCLIENT Backdoor in Government Cyber Attacks'
date: 2026-01-28
permalink: /posts/2026/01/28/mustang-panda-deploys-updated-coolclient-backdoor-in-government-cyber-attacks/
tags:
- veille-cyber
- hackernews
---
## La menace COOLCLIENT évolue dans les cyberattaques gouvernementales

Des acteurs malveillants associés à la Chine, identifiés comme Mustang Panda (également connu sous les noms d'Earth Preta, Fireant, HoneyMyte, Polaris et Twill Typhoon), déploient une version améliorée de la porte dérobée COOLCLIENT dans le cadre d'opérations de cyberespionnage. Ces attaques visent principalement des entités gouvernementales, touchant des campagnes en Birmanie, Mongolie, Malaisie et Russie.

L'exploitation de COOLCLIENT, qui sert de porte dérobée secondaire aux côtés de PlugX et LuminousMoth, a été observée à travers plusieurs campagnes entre 2021 et 2025. Le malware utilise la technique du "DLL side-loading", nécessitant un exécutable légitime signé pour charger une DLL malveillante. Mustang Panda a exploité des binaires signés de logiciels variés tels que Bitdefender, VLC Media Player, Ulead PhotoImpact et Sangfor pour cette fin. Des attaques récentes ont également vu l'utilisation d'une variante de COOLCLIENT livrant un rootkit inédit.

COOLCLIENT, documenté pour la première fois en 2022, est capable de voler des informations sensibles, notamment les frappes clavier, le contenu du presse-papiers, les fichiers, ainsi que les identifiants de proxy HTTP. Il peut également établir des tunnels inversés, exécuter des plugins supplémentaires en mémoire pour la gestion des services, des fichiers, et des shells à distance. Des programmes de vol d'identifiants de navigateurs ont aussi été déployés, ciblant Chrome, Edge et d'autres navigateurs basés sur Chromium, ainsi que des données de cookies Firefox exfiltrées vers Google Drive.

Ces activités s'étendent au-delà de l'espionnage traditionnel, indiquant une surveillance active des activités utilisateur. Le groupe utilise également des scripts batch et PowerShell pour la collecte d'informations système, le vol de documents et la compromission des données de connexion des navigateurs. D'autres outils comme TONESHELL et QReverse sont aussi employés pour la persistance, l'exécution de charges utiles supplémentaires, et la prise de contrôle à distance.

**Points clés :**

*   **Acteur de menace :** Mustang Panda (Earth Preta, Fireant, HoneyMyte, Polaris, Twill Typhoon).
*   **Malware principal :** COOLCLIENT (porte dérobée mise à jour).
*   **Objectifs :** Espionnage cybernétique, vol de données complet.
*   **Cibles :** Entités gouvernementales, opérateurs télécom.
*   **Zones géographiques touchées :** Birmanie, Mongolie, Malaisie, Russie, Thaïlande, Pakistan.
*   **Techniques :** DLL side-loading, utilisation de binaires légitimes signés, déploiement de rootkits, stealers d'identifiants, scripts batch/PowerShell.

**Vulnérabilités (non spécifiées avec des identifiants CVE dans l'article) :**

L'article ne mentionne pas de vulnérabilités spécifiques avec des identifiants CVE. Les attaques exploitent plutôt des techniques d'exécution de code malveillant comme le "DLL side-loading" et l'abus de logiciels légitimes.

**Recommandations :**

Bien que l'article ne détaille pas de recommandations spécifiques, les pratiques générales de cybersécurité applicables incluent :

*   **Surveillance et détection :** Renforcer la surveillance des réseaux et des points d'accès pour détecter les activités suspectes.
*   **Mises à jour logicielles :** S'assurer que tous les logiciels, y compris les exécutables légitimes utilisés pour le DLL side-loading, sont maintenus à jour et patchés.
*   **Sécurité des points d'accès :** Mettre en œuvre des mesures de sécurité robustes sur les points d'accès pour prévenir l'exécution non autorisée de code.
*   **Sensibilisation :** Former les utilisateurs aux risques de phishing et à l'ingénierie sociale, qui peuvent être des vecteurs d'infection initiaux.
*   **Gestion des accès :** Appliquer le principe du moindre privilège pour limiter les dommages potentiels en cas de compromission.

---
[Source](https://thehackernews.com/2026/01/mustang-panda-deploys-updated.html){:target="_blank"}
