---
title: 'Hackers Use Fake Resumes to Steal Enterprise Credentials and Deploy Crypto Miner'
date: 2026-03-24
permalink: /posts/2026/03/24/hackers-use-fake-resumes-to-steal-enterprise-credentials-and-deploy-crypto-miner/
tags:
- veille-cyber
- hackernews
---
### Campagne FAUX#ELEVATE : Phishing par faux CV et minage de cryptomonnaies

Une campagne de phishing sophistiquée, baptisée **FAUX#ELEVATE**, cible les environnements d'entreprise francophones. Utilisant des faux CV sous forme de scripts VBScript hautement obscurcis, cette attaque déploie une panoplie d'outils malveillants visant le vol d'identifiants, l'exfiltration de données et le minage de cryptomonnaie (Monero).

**Points clés :**
*   **Tactique de dissimulation :** Le script (9,7 Mo) contient majoritairement des commentaires inutiles pour tromper l'analyse et simule une erreur de fichier pour masquer son exécution.
*   **Ciblage sélectif :** L'attaque utilise WMI pour détecter si la machine appartient à un domaine d'entreprise, ignorant les systèmes personnels.
*   **Vitesse d'exécution :** La chaîne d'infection complète (de l'ouverture du script à l'exfiltration) s'effectue en environ 25 secondes.
*   **Infrastructure détournée :** Utilisation de services légitimes (Dropbox pour les charges utiles, WordPress piratés pour le contrôle, et mail.ru pour l'exfiltration).
*   **Persistance et évasion :** Désactivation de l'UAC, ajout d'exclusions dans Microsoft Defender et contournement de l'encryption ABE (App-Bound Encryption) des navigateurs via le projet *ChromElevator*.

**Vulnérabilités exploitées :**
*   **UAC Bypass :** Le malware force de manière répétée les demandes de privilèges administrateur.
*   **Configuration de sécurité :** Modification du registre Windows pour désactiver les contrôles de sécurité et ajout d'exclusions globales dans Microsoft Defender (lecteurs C à I).

**Recommandations :**
*   **Filtrage des emails :** Renforcer la vigilance sur les pièces jointes VBScript. Les services de messagerie devraient bloquer systématiquement les extensions de fichiers exécutables ou de scripts provenant de sources non fiables.
*   **Contrôle des privilèges :** Restreindre les droits d'administration locale. Une élévation de privilèges anormale déclenchée par un script utilisateur doit être immédiatement bloquée.
*   **Surveillance réseau :** Surveiller les communications sortantes vers des services de messagerie publique (comme mail.ru) et les accès vers des services de stockage cloud non autorisés par la politique de l'entreprise.
*   **Protection des endpoints :** Auditer régulièrement les exclusions définies dans Microsoft Defender et surveiller les processus utilisant le pilote `WinRing0x64.sys`, souvent associé à des activités de minage illégitime.

---
[Source](https://thehackernews.com/2026/03/hackers-use-fake-resumes-to-steal.html){:target="_blank"}
