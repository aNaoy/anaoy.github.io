---
title: 'Nigerian man gets eight years in prison for hacking tax firms'
date: 2026-02-20
permalink: /posts/2026/02/20/nigerian-man-gets-eight-years-in-prison-for-hacking-tax-firms/
tags:
- veille-cyber
- bleepingcomp
---
**Condamnation pour Fraude Fiscale et Piratage Informatique**

Un ressortissant nigérian, Matthew Abiodun Akande, a été condamné à huit ans de prison pour avoir piraté plusieurs cabinets de préparation fiscale aux États-Unis et pour avoir déposé plus de 1 000 déclarations de revenus frauduleuses, réclamant plus de 8,1 millions de dollars en remboursements. Il a été arrêté à Londres en octobre 2024 et extradé vers les États-Unis.

**Points Clés :**

*   **Méthode d'Attaque :** Akande a utilisé le logiciel malveillant de type RAT (Remote Access Trojan) appelé Warzone, acheté avec une licence, et un logiciel de cryptage pour le rendre indétectable par les antivirus.
*   **Ingénierie Sociale :** Il a envoyé des e-mails de phishing usurpent l'identité du PDG d'une société d'ingénierie-architecture du Massachusetts à quatre cabinets fiscaux.
*   **Pièce Jointe Trompeuse :** Les e-mails contenaient des documents fiscaux (W-2 et 1099) falsifiés et un lien Dropbox. En cliquant sur ce lien, les victimes téléchargaient silencieusement le logiciel malveillant.
*   **Vol de Données :** Une fois les systèmes compromis, Akande a volé les informations personnelles (numéros de sécurité sociale, données fiscales antérieures) des clients des cabinets.
*   **Fraude :** Ces informations ont été utilisées pour déposer des déclarations de revenus frauduleuses. Les remboursements ont été dirigés vers des comptes bancaires contrôlés par des complices aux États-Unis, puis transférés vers le Mexique.
*   **Condamnation :** Akande a été condamné à huit ans de prison, trois ans de mise à l'épreuve et à une restitution de près de 1,4 million de dollars.

**Vulnérabilités Exploités :**

*   **Absence de détection des logiciels malveillants :** L'utilisation d'un crypteur a permis de contourner les solutions antivirus.
*   **Ingénierie sociale (Phishing) :** L'usurpation d'identité et la création de faux domaines et adresses e-mail ont trompé les employés des cabinets fiscaux.
*   **Confiance dans les liens externes :** Le téléchargement de fichiers à partir de liens externes, même s'ils semblent légitimes, a permis l'installation du RAT.

**Recommandations (implicites) :**

*   **Renforcement de la sécurité des endpoints :** Solutions antivirus avancées et détection des menaces de type RAT.
*   **Sensibilisation à la sécurité :** Formation des employés à la reconnaissance des e-mails de phishing et aux dangers des liens suspects.
*   **Authentification forte :** Mise en place de mesures d'authentification multi-facteurs pour accéder aux systèmes sensibles.
*   **Filtrage des e-mails :** Solutions de sécurité avancées pour bloquer les e-mails de phishing et les pièces jointes malveillantes.
*   **Gestion des accès :** Principe du moindre privilège pour limiter les dommages en cas de compromission.

---
[Source](https://www.bleepingcomputer.com/news/security/nigerian-man-gets-eight-years-in-prison-for-hacking-tax-firms/){:target="_blank"}
