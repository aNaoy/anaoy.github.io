---
title: 'Citrus Ransomware: VLESS for traffic, Sn00py for encryption, and LLMs lending a hand'
date: 2026-11-11
permalink: /posts/2026/11/11/citrus-ransomware-vless-for-traffic-sn00py-for-encryption-and-llms-lending-a-hand/
tags:
- veille-cyber
- securelist
---
### Analyse du groupe Citrus Ransomware et de ses techniques d’attaque

Le groupe Citrus Ransomware combine des méthodes d'intrusion classiques avec l'automatisation par IA et des techniques de dissimulation avancées. Ce groupe s'infiltre principalement par le biais de comptes de prestataires compromis, utilisant ensuite des outils d'administration standard pour sa progression.

**Points clés :**
*   **Utilisation de l'IA :** Les attaquants exploitent des LLM pour générer des scripts malveillants, des commandes PowerShell et commenter leur propre code afin d'accélérer l'énumération et l'exécution.
*   **Exfiltration et Tunneling :** Utilisation de tunnels VLESS (protocole Xray) pour masquer le trafic malveillant en HTTPS légitime et exfiltration de données via des services web.
*   **Mascarade :** Les outils malveillants sont renommés pour imiter des logiciels légitimes (ex: "KasperskyGPO_Deploy") afin de tromper les administrateurs et les outils de sécurité.
*   **Ransomware :** Utilisation de la famille Sn00py (écrite en Go) pour chiffrer les données (extension `.citrus`) via RSA-2048 et ChaCha20. Le déploiement s'effectue via des GPO malveillantes.

**Vulnérabilités exploitées :**
*   **CVE-2026-54121 (Certighost) :** Contournement de l'authentification AD CS pour créer des comptes machines et usurper l'identité de contrôleurs de domaine.
*   **CVE-2020-1337 :** Exploitation pour l'élévation de privilèges, souvent via des composants issus de Metasploit.

**Recommandations de sécurité :**
*   **Gestion des tiers :** Appliquer le principe du moindre privilège aux comptes des prestataires et auditer strictement leurs accès VPN et RDP.
*   **Contrôle des privilèges :** Restreindre les accès aux serveurs 1C:Enterprise et surveiller les configurations AD CS pour prévenir l'abus de certificats.
*   **Détection proactive :** Surveiller la création de tâches planifiées suspectes, l'utilisation de `wevtutil` pour effacer les journaux d'événements et l'apparition de noms de machines inhabituels (ex: préfixes "GHOST").
*   **Protection des solutions de sécurité :** Empêcher la modification des exclusions antivirus et restreindre l'accès aux consoles de gestion centralisée des solutions de cybersécurité.

---
[Source](https://securelist.com/citrus-ransomware/121879/){:target="_blank"}
