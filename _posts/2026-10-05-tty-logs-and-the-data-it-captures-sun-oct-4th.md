---
title: 'TTY Logs and the Data it Captures, (Sun, Oct 4th)'
date: 2026-10-05
permalink: /posts/2026/10/05/tty-logs-and-the-data-it-captures-sun-oct-4th/
tags:
- veille-cyber
- sans-isc
---
### Analyse des logs TTY : suivi de l'activité des attaquants

L'exploitation des logs TTY (terminal) recueillis sur des capteurs DShield permet de centraliser et d'analyser les commandes exécutées par les attaquants après une intrusion réussie. En corrélant ces données dans un SIEM via des requêtes ES|QL, il est possible d'identifier les comportements malveillants récurrents et de mapper les commandes hashées en activités réelles.

**Points clés :**
*   **Centralisation :** L'utilisation de scripts pour parser et envoyer les logs TTY quotidiennement permet une corrélation à grande échelle.
*   **Persistence automatisée :** Une analyse sur 90 jours a révélé qu'une commande spécifique liée au `crontab` a été exécutée par plus de 3 130 adresses IP distinctes, soulignant l'automatisation massive des attaques.
*   **Visibilité :** La corrélation des IDs de transaction permet de démasquer le contenu réel des commandes dissimulées par des hashs, offrant une meilleure visibilité sur les tactiques des attaquants.

**Vulnérabilités :**
*   Bien que l'article ne mentionne pas de CVE spécifique, il met en évidence l'exploitation de systèmes via des accès non autorisés (brute force ou exploitation de failles connues), suivie par l'injection de tâches planifiées (`crontab`) pour assurer la persistance de malwares ou de backdoors.

**Recommandations :**
*   **Monitoring :** Mettre en place un journalisation rigoureuse des activités de terminal (logs TTY) pour détecter les commandes suspectes après une connexion.
*   **Corrélation :** Utiliser des outils SIEM pour automatiser l'analyse comportementale et le décodage des commandes malveillantes.
*   **Durcissement :** Restreindre strictement les permissions `crontab` et surveiller toute modification non autorisée des fichiers de configuration système.
*   **Veille :** Utiliser les indicateurs d'attaques (IPs et ASN sources) identifiés dans les logs pour mettre à jour les politiques de filtrage (pare-feu/IPS).

---
[Source](https://isc.sans.edu/diary/rss/33396){:target="_blank"}
