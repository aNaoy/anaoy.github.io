---
title: 'Ousaban Banking Trojan Targets Iberian Bank Users with Fake PDF Lures'
date: 2026-07-01
permalink: /posts/2026/07/01/ousaban-banking-trojan-targets-iberian-bank-users-with-fake-pdf-lures/
tags:
- veille-cyber
- hackernews
---
### Menace Bancaire : Le Cheval de Troie Ousaban cible la péninsule Ibérique

Le cheval de troie bancaire « Ousaban » (ou Javali), membre de la famille malveillante brésilienne « Tetrade », mène une campagne active contre les utilisateurs Windows en Espagne et au Portugal. Ce malware sophistiqué utilise des techniques de dissimulation avancées pour voler des identifiants bancaires et prendre le contrôle total des sessions des victimes.

**Points clés :**
*   **Vecteur d'attaque :** Utilisation de PDF de phishing prétendant contenir un fichier corrompu, incitant la victime à cliquer sur un bouton « Actualiser ».
*   **Techniques de dissimulation :**
    *   **Géofencing :** Le malware vérifie l'origine géographique (IP, langue, fuseau horaire) pour ne cibler que l'Espagne et le Portugal, évitant ainsi les analyses de sécurité automatisées.
    *   **Stéganographie :** Le code malveillant est extrait d'une image téléchargée après le contournement des vérifications.
    *   **Infrastructures éphémères :** Le serveur de commande change quotidiennement son adresse via un mécanisme de génération dynamique basé sur la date du jour.
*   **Persistence :** Le malware s'installe via une entrée de registre nommée « Financeiro » pour se lancer automatiquement au démarrage de Windows.
*   **Capacités :** Capture d'écran, enregistrement des frappes clavier (keylogging), manipulation du presse-papier et accès à distance.

**Vulnérabilités :**
*   Aucune CVE spécifique n'est mentionnée ; le malware exploite la crédulité des utilisateurs (ingénierie sociale) et l'exécution de scripts via des PDF.

**Recommandations :**
*   **Vigilance utilisateur :** Ne jamais cliquer sur les boutons « Actualiser » ou « Update » dans des documents PDF reçus par mail, et se méfier des invites demandant de copier/coller des commandes pour « corriger » une erreur.
*   **Filtrage :** Bloquer les fichiers et accès liés aux indicateurs de compromission (IoC) fournis par Fortinet.
*   **Surveillance système :** Surveiller la création de clés de registre nommées « Financeiro » et la présence de fichiers suspects dans les répertoires système (ex: `C:\SysMain_5874288`).
*   **Défense périmétrique :** Les solutions de filtrage d'emails (type FortiMail) et les antivirus mis à jour sont efficaces pour bloquer les échantillons connus.

---
[Source](https://thehackernews.com/2026/07/ousaban-banking-trojan-targets-iberian.html){:target="_blank"}
