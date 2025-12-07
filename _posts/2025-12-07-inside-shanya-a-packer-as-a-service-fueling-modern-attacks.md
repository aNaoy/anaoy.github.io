---
title: 'Inside Shanya, a packer-as-a-service fueling modern attacks'
date: 2025-12-07
permalink: /posts/2025/12/07/inside-shanya-a-packer-as-a-service-fueling-modern-attacks/
tags:
- veille-cyber
- sophos
---
**Shanya : Le nouveau service de "packer" au service des cyberattaques**

Une nouvelle offre malveillante, baptisée "Shanya" (ou VX Crypt), s'est imposée sur le marché underground comme un service de "packer" (outil de chiffrement et d'obfuscation de malware). Ce service est déjà privilégié par les groupes de ransomware, remplaçant en partie des outils similaires comme HeartCrypt. Shanya permet aux attaquants de créer des charges utiles indétectables en mémoire, de contourner les protections antivirus, d'éviter les environnements virtualisés et de masquer leur activité.

**Points clés :**

*   **Service "Packer-as-a-Service" :** Shanya offre des fonctionnalités avancées pour rendre les malwares plus furtifs, incluant la génération d'un code unique avec des algorithmes de chiffrement personnalisés pour chaque client.
*   **Techniques d'obfuscation et d'évasion :** Il intègre des méthodes pour contourner l'AMSI (.NET), masquer la charge utile en mémoire, modifier les informations d'icône et de version, et exploiter le manifeste pour l'escalade de privilèges (UAC Bypass). Il offre également des fonctionnalités de démarrage automatique et de protection contre l'analyse en environnement virtualisé ou sandbox.
*   **Utilisation par des groupes de cybercriminels :** Shanya est utilisé pour déployer diverses familles de malwares, notamment les ransomwares Akira, Medusa, Qilin et Crytox, ainsi que des outils comme le loader Armillaria, l'EDR killer et le backdoor CastleRAT.
*   **Techniques techniques :** Le packer utilise des méthodes sophistiquées comme le stockage de données critiques dans le PEB (Process Environment Block), la résolution dynamique d'API par hachage, et des techniques d'anti-analyse pour détecter et perturber les outils de débogage et les sandboxes. Il charge également une seconde instance d'une DLL système (souvent `shell32.dll`) modifiée pour masquer la charge utile malveillante.
*   **Campagnes ciblées :** Des campagnes ont été observées utilisant Shanya pour cibler des entreprises, comme une attaque de type "booking.com" visant le secteur de l'hôtellerie pour déployer le RAT CastleRAT.

**Vulnérabilités :**

Bien que l'article ne mentionne pas de vulnérabilités spécifiques avec des identifiants CVE, les techniques utilisées par Shanya exploitent l'évasion des mécanismes de sécurité existants. La fonctionnalité "privilege escalation via manifest (UAC Bypass)" suggère une exploitation des autorisations du système d'exploitation. L'abus de drivers légitimes (comme ThrottleStop.sys) et de programmes de Microsoft (comme `consent.exe`) démontre une exploitation de la confiance et des fonctionnalités systèmes.

**Recommandations :**

*   **Détection et protection avancées :** Les solutions de sécurité doivent être capables de détecter les comportements associés à Shanya, tels que le chargement de modules suspects, l'obfuscation de code, et les tentatives de contournement des défenses. Les protections comme celles de Sophos (ATK/Shanya-B, ATK/Shanya-C, et ATK/Shanya-D) sont essentielles.
*   **Surveillance des indicateurs de compromission (IoCs) :** Il est crucial de surveiller les IoCs fournis par les chercheurs en sécurité (disponibles sur GitHub) pour identifier les traces de Shanya dans les environnements.
*   **Mises à jour et patchs :** Maintenir les systèmes d'exploitation et les logiciels à jour est fondamental pour corriger les vulnérabilités potentielles qui pourraient être exploitées.
*   **Formation à la sécurité :** Sensibiliser les utilisateurs aux techniques d'ingénierie sociale, comme les faux formulaires de vérification, peut aider à prévenir l'exécution initiale des malwares.
*   **Analyse comportementale :** Les outils d'analyse comportementale sont primordiaux pour détecter les activités suspectes qui échappent aux signatures classiques, notamment lors du déchiffrement de charges utiles en mémoire.

---
[Source](https://news.sophos.com/en-us/2025/12/06/inside-shanya-a-packer-as-a-service-fueling-modern-attacks/){:target="_blank"}
