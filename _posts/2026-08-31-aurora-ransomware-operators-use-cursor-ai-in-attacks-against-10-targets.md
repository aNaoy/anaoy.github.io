---
title: 'Aurora Ransomware Operators Use Cursor AI in Attacks Against 10 Targets'
date: 2026-08-31
permalink: /posts/2026/08/31/aurora-ransomware-operators-use-cursor-ai-in-attacks-against-10-targets/
tags:
- veille-cyber
- hackernews
---
### L'usage de l'IA générative dans les cyberattaques : le cas Aurora et Gryxa

Les cybercriminels derrière le ransomware **Aurora** utilisent désormais l'assistant de codage IA **Cursor** pour planifier et automatiser leurs attaques. Des fuites d'infrastructures ont révélé une utilisation intensive de cet outil pour rédiger des scripts en russe, concevoir des plans d'exploitation (notamment pour AD CS) et guider les opérateurs dans l'exécution de tâches techniques complexes.

**Points clés :**
* **Mode opératoire :** L'accès initial est obtenu via des campagnes de "bombardement" d'e-mails suivies d'appels téléphoniques frauduleux (usurpation du support IT) et l'utilisation de l'outil *Xray-core*.
* **Automatisation par l'IA :** Les attaquants délèguent à Cursor des tâches telles que le scan réseau (Nmap, NetExec), l'énumération de privilèges (BloodHound) et l'exécution d'attaques complexes (Certipy, NTLM relay via PetitPotam/PrinterBug).
* **Polyvalence :** Le ransomware est écrit en Zig et décliné en versions Windows et Linux/ESXi, cette dernière forçant l'arrêt des machines virtuelles avant le chiffrement.
* **Nouvelle menace (Gryxa) :** Un autre toolkit baptisé "Gryxa" a été identifié, utilisant également l'IA pour créer des opérations complètes, incluant la persistance, le vol de jetons de navigateurs (en contournant le chiffrement ABE) et la surveillance des efforts de remédiation des équipes de sécurité.

**Vulnérabilités exploitées :**
* **AD CS (Active Directory Certificate Services) :** Exploitation planifiée via des scripts assistés par IA.
* **Relais NTLM :** Utilisation d'outils comme *PetitPotam*, *Coerce Plus* et *PrinterBug*.
* **Chiffrement ABE (Chrome) :** Contournement des protections de sécurité des navigateurs par Gryxa.
* **Services Windows :** Abus des outils légitimes (RMM) et des mécanismes de persistance (tâches planifiées).

**Recommandations :**
* **Renforcement de l'identité :** Mettre en œuvre une authentification multi-facteurs (MFA) robuste, particulièrement résistante au phishing, et sensibiliser les employés aux appels frauduleux usurpant le support technique.
* **Sécurisation des services AD :** Auditer les configurations des services de certificats Active Directory (AD CS) pour prévenir les abus de privilèges.
* **Surveillance EDR :** Détecter les comportements anormaux liés aux outils de management à distance (RMM) et surveiller la désactivation suspecte de Microsoft Defender.
* **Gestion des logs :** Surveiller les accès aux journaux système et les tentatives de suppression des clichés instantanés (*Shadow Copies*) ou de la restauration système.
* **Défense active :** Bloquer les outils de tunnelisation (ex: *Xray-core*, *proxychains*) utilisés pour établir des accès distants non autorisés.

---
[Source](https://thehackernews.com/2026/08/aurora-ransomware-operators-use-cursor.html){:target="_blank"}
