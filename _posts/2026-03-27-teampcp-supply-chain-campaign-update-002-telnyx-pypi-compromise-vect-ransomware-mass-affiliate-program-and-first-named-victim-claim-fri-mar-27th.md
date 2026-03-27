---
title: 'TeamPCP Supply Chain Campaign: Update 002 - Telnyx PyPI Compromise, Vect Ransomware Mass Affiliate Program, and First Named Victim Claim, (Fri, Mar 27th)'
date: 2026-03-27
permalink: /posts/2026/03/27/teampcp-supply-chain-campaign-update-002-telnyx-pypi-compromise-vect-ransomware-mass-affiliate-program-and-first-named-victim-claim-fri-mar-27th/
tags:
- veille-cyber
- sans-isc
---
### Escalade de la campagne TeamPCP : Compromissions PyPI et alliance avec le ransomware Vect

La campagne d'attaques sur la chaîne d'approvisionnement logicielle menée par **TeamPCP** s'intensifie, passant du simple vol de privilèges à une industrialisation du déploiement de ransomwares via un partenariat avec **Vect** et **BreachForums**.

**Points clés :**
*   **Compromission du SDK Telnyx (PyPI) :** Les versions 4.87.1 et 4.87.2 du package `telnyx` ont été compromises via des identifiants dérobés. L'attaquant utilise une nouvelle technique de stéganographie via des fichiers `.wav` pour dissimuler des charges utiles.
*   **Alliance cybercriminelle :** TeamPCP fournit les accès initiaux (issus de compromissions de la chaîne d'approvisionnement), tandis que Vect fournit les outils d'extorsion à une base potentielle de 300 000 affiliés sur BreachForums.
*   **Revendication LAPSUS$ :** Le groupe LAPSUS$ revendique le vol de 3 Go de données chez AstraZeneca, marquant la première victime nommée de cette campagne.
*   **Vecteur d'attaque :** La compromission initiale de LiteLLM a été rendue possible par le piratage du compte GitHub personnel du CEO de l'entreprise.

**Vulnérabilités et CVE associées :**
*   **CVE-2026-33634 (Trivy) :** RCE dans l'outil Trivy. Date limite de remédiation CISA : **8 avril 2026**.
*   **CVE-2026-33017 (Langflow) :** RCE non authentifiée dans Langflow (< 1.8.2). Date limite de remédiation CISA : **9 avril 2026**.

**Recommandations :**
1.  **Audits immédiats :** Vérifiez vos environnements Python pour les versions compromises de `telnyx` (4.87.1, 4.87.2) et recherchez les fichiers `.wav` suspects ou le binaire `msbuild.exe` dans les dossiers de démarrage Windows.
2.  **Rotation des identifiants :** Toute organisation ayant utilisé des composants liés à la campagne (Trivy, LiteLLM, Telnyx) doit considérer ses identifiants comme compromis et procéder à une rotation immédiate et généralisée.
3.  **Indicateurs de compromission (IoC) :** Surveillez le domaine C2 `models.litellm.cloud`, le chemin de persistance `~/.config/sysmon/sysmon.py`, la présence de fichiers `.pth` anormaux dans les `site-packages`, ainsi que les pods Kubernetes nommés `node-setup-*`.
4.  **Sécurisation CI/CD :** Appliquez systématiquement l'épinglage des dépendances via des hashs de commit complets (SHA) dans vos workflows GitHub Actions pour contrer la réécriture de tags.

---
[Source](https://isc.sans.edu/diary/rss/32838){:target="_blank"}
