---
title: '100+ Compromised Websites Use Fake Cloudflare Checks to Deliver LunexStealer'
date: 2026-10-07
permalink: /posts/2026/10/07/100-compromised-websites-use-fake-cloudflare-checks-to-deliver-lunexstealer/
tags:
- veille-cyber
- hackernews
---
### Campagne de malwares LunexStealer via de faux contrôles Cloudflare

Le CERT-UA a identifié plus de 100 sites web compromis par le groupe UAC-0277 pour diffuser le logiciel malveillant **LunexStealer** (alias Psychedelic Stealer). L'attaque repose sur la technique « ClickFix », où une fausse page de vérification Cloudflare incite les utilisateurs à exécuter une commande malveillante téléchargeant un paquet MSI.

**Points clés :**
*   **Technique EtherHiding :** Utilisation de contrats intelligents sur Ethereum ou Polygon pour récupérer la configuration et le mode opératoire de l'attaque.
*   **Ciblage :** La fausse vérification n'apparaît que pour les utilisateurs Windows provenant de moteurs de recherche.
*   **Persistance et exfiltration :** Installation d'une extension malveillante (LUNARAXE) déguisée en extension Microsoft Office, capable de voler des identifiants, des cookies et de contrôler le navigateur.
*   **Composant auxiliaire :** Le module NAIVEMESS permet à l'attaquant d'accéder au système de fichiers Windows via PowerShell.

**Vulnérabilités exploitées :**
*   **Pilote AMD vulnérable (PDFWKRNL.sys) :** Utilisé pour désactiver les logiciels de sécurité (blindage).
*   **DLL Sideloading :** Utilisation du binaire légitime `FnHotkeyUtility.exe` pour charger une DLL malveillante (`spkvol.dll`).
*   **CSP (Content Security Policy) :** Le module `LUNARAXE.STRIP` neutralise les protections CSP pour injecter du code JavaScript arbitraire.

**Recommandations :**
*   **Restrictions système :** Désactiver la boîte de dialogue « Exécuter » via les politiques de groupe et limiter l'installation de paquets MSI aux utilisateurs sans droits d'administration.
*   **Sécurité des pilotes :** Activer la liste de blocage des pilotes vulnérables de Microsoft et la règle ASR (Attack Surface Reduction) « Bloquer l'abus de pilotes signés vulnérables ».
*   **Surveillance :** Surveiller l'exécution de `msiexec.exe`.
*   **Extensions :** Restreindre l'installation d'extensions de navigateur via une liste blanche (allowlist).

---
[Source](https://thehackernews.com/2026/10/100-compromised-websites-use-fake.html){:target="_blank"}
