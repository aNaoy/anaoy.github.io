---
title: 'The SOC Files: Time to “Sapecar”. Unpacking a new Horabot campaign in Mexico'
date: 2026-03-19
permalink: /posts/2026/03/19/the-soc-files-time-to-sapecar-unpacking-a-new-horabot-campaign-in-mexico/
tags:
- veille-cyber
- securelist
---
### Analyse de la campagne Horabot : Menace bancaire au Mexique

**Vue d’ensemble**
Horabot est une menace complexe active ciblant principalement le Mexique (93 % des 5 384 victimes identifiées). Le groupe utilise une chaîne d'attaque sophistiquée combinant des techniques d'ingénierie sociale, du polymorphisme côté serveur et l'utilisation détournée d'outils légitimes comme AutoIT pour déployer un cheval de Troie bancaire (familles *Casbaneiro*, *Ponteiro* ou *Metamorfo*).

**Points clés de la chaîne d'attaque**
*   **Vecteur initial :** Pages de faux CAPTCHA incitant l'utilisateur à exécuter manuellement une commande via la boîte de dialogue "Exécuter".
*   **Infection multi-étapes :** Utilisation de fichiers HTA et de scripts VBS hautement obfusqués. Le "heavy lifter" effectue des vérifications d'environnement (anti-VM/anti-Avast) et assure la persistance via des fichiers LNK dans le dossier de démarrage.
*   **Composant bancaire :** Un exécutable AutoIT déchiffre une DLL (via AES-192) qui injecte le cheval de Troie en mémoire. Ce dernier utilise des bibliothèques OpenSSL obsolètes et un protocole de communication réseau personnalisé pour le C2.
*   **Propagation :** Le module "spreader" récolte des adresses e-mail via l'espace de noms MAPI et automatise l'envoi de nouveaux emails de phishing contenant des PDF malveillants.
*   **Origine :** Les commentaires dans le code source et l'utilisation de termes argotiques brésiliens ("sapecar", "pega a visão") confirment une origine liée à des opérateurs lusophones.

**Vulnérabilités et vecteurs d'exploitation**
*   **Exploitation de la confiance :** Utilisation de techniques d'ingénierie sociale détournant des processus système (exécution de commandes via `mshta` et PowerShell).
*   **Persistance :** Manipulation des répertoires de démarrage Windows (Startup).
*   **Communication :** Utilisation d'un protocole réseau propriétaire chiffré par un algorithme XOR état-dépendant pour échapper à l'inspection par signature.
*   *Note : Aucune CVE spécifique n'est exploitée, la campagne repose sur l'exécution volontaire de code par la victime.*

**Recommandations**
*   **Détection réseau :** Surveiller les communications réseau présentant des marqueurs répétitifs de type "##" dans les flux de données, souvent associés au protocole C2 personnalisé d'Horabot. Implémenter les règles Suricata basées sur ces motifs.
*   **Protection des endpoints :** Bloquer ou surveiller étroitement l'exécution de `mshta.exe` et l'appel de commandes PowerShell depuis des environnements non standards.
*   **Durcissement :** Restreindre les autorisations d'exécution dans les dossiers temporaires et le dossier de démarrage (Startup).
*   **Sensibilisation :** Éduquer les utilisateurs contre les tactiques de type "faux CAPTCHA" qui incitent à copier-coller des commandes dans l'interface Windows.
*   **Filtrage MAPI :** Surveiller l'activité suspecte via MAPI pour prévenir la récolte massive de contacts e-mail.

---
[Source](https://securelist.com/horabot-campaign/119033/){:target="_blank"}
