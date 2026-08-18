---
title: 'Your Controls Block Known Attacks. What About the Behavior?'
date: 2026-08-18
permalink: /posts/2026/08/18/your-controls-block-known-attacks-what-about-the-behavior/
tags:
- veille-cyber
- bleepingcomp
---
### La fausse sécurité des contrôles basés sur les signatures

Le *Blue Report 2026* de Picus Security révèle un décalage critique entre l'efficacité théorique des outils de sécurité et leur capacité réelle à contrer des attaques sophistiquées. Si le taux de prévention global au périmètre remonte à 69 %, les défenses intérieures restent largement inefficaces contre les techniques furtives.

#### Points clés
*   **Limites des indicateurs de compromission (IOC) :** Les contrôles basés sur les signatures (pare-feu, proxys) peinent face à des variantes d'outils connus. Leur taux d'efficacité pour bloquer les téléchargements de malwares est tombé à 50 %.
*   **Insuffisance de la défense intérieure :** Une fois le périmètre franchi, le taux de prévention chute à 37 %. Les actions "silencieuses" (lecture directe du registre, accès mémoire non conventionnels) contournent presque systématiquement les outils de détection.
*   **Le piège du Mimikatz :** L'étude démontre que la détection dépend de la méthode d'exécution. Alors que le dump de mémoire LSASS classique est bloqué dans 94 % des cas, l'extraction des secrets LSA via le registre local ne l'est que dans 3 % des cas.

#### Vulnérabilités et techniques concernées
*   **MITRE ATT&CK T1003 (OS Credential Dumping) :** Technique centrale exploitée via différentes méthodes (accès LSASS, lecture du registre, outils signés comme `ProcDump` ou `comsvcs.dll`).
*   **Défauts de visibilité :** Les outils actuels se focalisent sur des événements "bruyants" (ouverture de handle sur `lsass.exe`), ignorant les activités légitimes détournées (lecture de ruches de registre).
*   **Manque de détection comportementale :** Les actions de découverte, de collection et d'énumération de domaine (ex: SharpHound) passent inaperçues faute d'indicateurs comportementaux robustes.

#### Recommandations
*   **Combiner deux approches de test :** 
    *   Le test par **IOC** pour valider le blocage des menaces connues au périmètre.
    *   Le test par **TTP (comportemental)** pour vérifier la capacité des outils EDR/SIEM à détecter une action malveillante, peu importe la méthode ou l'outil utilisé par l'attaquant.
*   **Valider toutes les variantes :** Ne pas se contenter de tester la procédure "standard" d'un outil de test d'intrusion. Il est crucial d'orchestrer des tests utilisant des variantes (recompilation, outils natifs, chemins d'accès alternatifs).
*   **Prioriser le risque réel :** Utiliser les données de tests d'intrusion autonomes pour décider d'appliquer une stratégie de remédiation adaptée : *patcher, atténuer, surveiller ou accepter le risque avec preuves*.

---
[Source](https://www.bleepingcomputer.com/news/security/your-controls-block-known-attacks-what-about-the-behavior/){:target="_blank"}
