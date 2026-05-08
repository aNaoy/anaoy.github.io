---
title: 'Quasar Linux RAT Steals Developer Credentials for Software Supply Chain Compromise'
date: 2026-05-08
permalink: /posts/2026/05/08/quasar-linux-rat-steals-developer-credentials-for-software-supply-chain-compromise/
tags:
- veille-cyber
- hackernews
---
### Quasar Linux RAT (QLNX) : Une menace furtive pour la chaîne d'approvisionnement logicielle

Le malware **Quasar Linux RAT (QLNX)** est un implant sophistiqué ciblant spécifiquement les environnements de développement Linux. Conçu pour le vol de secrets et l'espionnage à long terme, il permet aux attaquants de compromettre la chaîne d'approvisionnement logicielle en accédant aux pipelines CI/CD, aux registres de paquets (NPM, PyPI) et aux infrastructures Cloud.

**Points clés :**
*   **Vol de secrets :** Extraction systématique de jetons et identifiants (AWS, GitHub, Kubernetes, Docker, Terraform, npm, PyPI).
*   **Furtivité avancée :** Exécution en mémoire, dissimulation via des processus de type noyau (*kworker*), et utilisation d'un rootkit à deux niveaux (LD_PRELOAD en espace utilisateur et eBPF au niveau noyau).
*   **Persistance multiple :** Sept méthodes de maintien, incluant *systemd*, *crontab* et injection dans `.bashrc`.
*   **Capacités étendues :** Supporte 58 commandes, incluant le keylogging, la capture d'écran, le tunneling réseau (SOCKS/TCP) et la gestion de réseau P2P.
*   **Backdoor PAM :** Interception des identifiants en clair lors des authentifications système et capture des sessions SSH.

**Vulnérabilités :**
*   Aucune CVE spécifique n'est exploitée ; le malware utilise des fonctionnalités légitimes du système (LD_PRELOAD, eBPF, PAM) pour se dissimuler et se maintenir, détournant ainsi la configuration standard des systèmes Linux.

**Recommandations :**
*   **Surveillance eBPF :** Auditer l'utilisation des programmes BPF sur les systèmes critiques pour détecter des comportements anormaux.
*   **Gestion des accès :** Implémenter le principe du moindre privilège pour les outils de développement et isoler les environnements CI/CD.
*   **Analyse d'intégrité :** Utiliser des outils d'EDR capables de détecter des injections mémoire et des hooks sur les modules d'authentification PAM.
*   **Sécurisation des secrets :** Utiliser des coffres-forts de secrets (ex: HashiCorp Vault) plutôt que de stocker des jetons en clair dans des fichiers de configuration (`.npmrc`, `.aws/credentials`, etc.).
*   **Monitoring réseau :** Surveiller les communications sortantes vers des infrastructures inconnues, notamment les flux TCP bruts et les tunnels non autorisés.

---
[Source](https://thehackernews.com/2026/05/quasar-linux-rat-steals-developer.html){:target="_blank"}
