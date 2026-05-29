---
title: 'New Russian-Linked GREYVIBE Targets Ukraine with AI-Powered Cyberattacks'
date: 2026-05-29
permalink: /posts/2026/05/29/new-russian-linked-greyvibe-targets-ukraine-with-ai-powered-cyberattacks/
tags:
- veille-cyber
- hackernews
---
### GREYVIBE : L'émergence d'acteurs hybrides utilisant l'IA pour des cyberattaques ciblées

Le groupe de menaces **GREYVIBE**, d'origine russophone, mène des campagnes persistantes contre des cibles ukrainiennes (gouvernementales, militaires et civiles) depuis août 2025. Ce collectif se distingue par son caractère hybride, opérant à la frontière entre le cybercrime classique et l'espionnage étatique, tout en intégrant massivement l'intelligence artificielle générative (GenAI) dans son arsenal technique.

#### Points clés
*   **Utilisation de l'IA :** Le groupe emploie des outils comme ChatGPT, Gemini et Ideogram pour accélérer le développement de malwares, créer des images de leurre, générer des scripts d'obfuscation et structurer ses infrastructures.
*   **Polyvalence des vecteurs d'attaque :** GREYVIBE utilise une large gamme de techniques :
    *   **ClickFix :** Pages de faux CAPTCHA simulant des outils comme Zoom.
    *   **Phishing ciblé :** Campagnes via des archives malveillantes (ZIP/RAR) hébergées sur des services cloud (Google Drive, 4sync).
    *   **Sites leurres :** Utilisation de faux sites de clubs ukrainiens (captation audio/vidéo) et de sites de fondations caritatives factices.
*   **Origines mixtes :** Le groupe présente des liens avec la cybercriminalité traditionnelle (utilisation de mineurs XMRig, réutilisation d'outils issus de gangs comme TrickBot/UAC-0098) tout en servant les intérêts du renseignement russe.

#### Outils et Malwares observés
*   **PhantomRelay / LegionRelay :** RAT (Remote Access Trojan) basés sur PowerShell permettant l'énumération de fichiers, l'exfiltration de données, la capture d'écran et la prise de contrôle à distance.
*   **FallSpy :** Spyware ciblant les appareils Android.
*   **Watchdog :** Mécanisme de persistance personnalisé.

#### Vulnérabilités et failles
Bien qu'aucune CVE spécifique ne soit citée, les failles exploitées reposent sur :
*   **L'ingénierie sociale :** Tromperie des utilisateurs via des interfaces de confiance (CAPTCHA, sites caritatifs).
*   **Erreurs opérationnelles :** L'usage intensif de l'IA a introduit des défauts de conception dans le code de *LegionRelay*, exposant les fonctionnalités de son backend.
*   **Fuites de développement :** Téléchargement de versions de test sur VirusTotal et utilisation de conventions de nommage peu professionnelles (ex: "cuteuwu").

#### Recommandations
*   **Vigilance accrue face aux CAPTCHA :** Se méfier des fenêtres contextuelles de vérification demandant l'exécution de commandes PowerShell ou de scripts, une méthode caractéristique de la campagne *ClickFix*.
*   **Sécurisation des terminaux :** Bloquer l'exécution non autorisée de scripts PowerShell et surveiller les processus suspects (exfiltration de données vers des serveurs inconnus).
*   **Sensibilisation aux leurres :** Éduquer le personnel sur les risques liés aux sites web falsifiés et aux archives reçues par mail, même si elles semblent provenir de sources légitimes ou caritatives.
*   **Analyse comportementale :** Privilégier la détection comportementale (détection d'exfiltration, usage de RAT) plutôt que les signatures statiques, ces dernières étant rapidement modifiées par l'IA du groupe.

---
[Source](https://thehackernews.com/2026/05/new-russian-linked-greyvibe-targets.html){:target="_blank"}
