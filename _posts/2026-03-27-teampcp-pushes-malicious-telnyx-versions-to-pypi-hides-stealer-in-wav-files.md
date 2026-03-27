---
title: 'TeamPCP Pushes Malicious Telnyx Versions to PyPI, Hides Stealer in WAV Files'
date: 2026-03-27
permalink: /posts/2026/03/27/teampcp-pushes-malicious-telnyx-versions-to-pypi-hides-stealer-in-wav-files/
tags:
- veille-cyber
- hackernews
---
### Compromission de la supply chain Python : Le package Telnyx piégé par TeamPCP

Le groupe de cybermenaces **TeamPCP** a compromis le package Python `telnyx` sur le dépôt PyPI (versions 4.87.1 et 4.87.2) afin d'exfiltrer des données sensibles. Cette attaque utilise une technique de stéganographie audio dissimulant des charges utiles malveillantes dans des fichiers `.WAV`.

**Points clés :**
* **Mode opératoire :** Le code malveillant est injecté dans `telnyx/_client.py` et s'exécute lors de l'importation du package.
* **Stéganographie :** Les payloads sont extraits de fichiers WAV (`hangup.wav` pour Windows, `ringtone.wav` pour Linux/macOS).
* **Persistance différentiée :** 
    * Sur **Windows**, le malware se copie dans le dossier de démarrage sous le nom `msbuild.exe`.
    * Sur **Linux/macOS**, l'attaque est furtive (« smash-and-grab ») : elle collecte les données en mémoire, les exfiltre et s'auto-supprime sans laisser de traces.
* **Objectif :** Vol de credentials, secrets CI/CD et variables d'environnement.

**Vulnérabilités :**
* **CVE-2026-33634** (associée à cette campagne de supply chain).

**Recommandations :**
* **Nettoyage :** Rétrograder immédiatement le package `telnyx` vers la version 4.87.0 et auditer les fichiers `requirements.txt`.
* **Remédiation :** Supprimer tout fichier `msbuild.exe` suspect situé dans le dossier de démarrage Windows.
* **Sécurité des secrets :** Considérer que tous les secrets présents dans les environnements ayant utilisé les versions compromises sont compromis ; procéder à une rotation immédiate de tous les jetons, clés API et mots de passe.
* **Filtrage réseau :** Bloquer le trafic vers l'adresse IP du serveur de commande et de contrôle : `83.142.209[.]203`.

---
[Source](https://thehackernews.com/2026/03/teampcp-pushes-malicious-telnyx.html){:target="_blank"}
