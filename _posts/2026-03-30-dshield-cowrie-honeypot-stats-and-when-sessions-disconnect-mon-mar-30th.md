---
title: 'DShield (Cowrie) Honeypot Stats and When Sessions Disconnect, (Mon, Mar 30th)'
date: 2026-03-30
permalink: /posts/2026/03/30/dshield-cowrie-honeypot-stats-and-when-sessions-disconnect-mon-mar-30th/
tags:
- veille-cyber
- sans-isc
---
### Analyse des comportements des attaquants sur les honeypots DShield (Cowrie)

Cette étude analyse trois ans de données issues de honeypots Cowrie (SSH/Telnet) pour identifier des modèles d'attaques automatisées et améliorer la fidélité des leurres.

**Points clés :**
*   **Volume et automatisation :** Sur 1,2 million de sessions, la majorité est hautement automatisée. Environ 94 % des sessions se terminent après l'exécution de moins de 50 commandes, avec un pic fréquent à 22 commandes.
*   **Durée des sessions :** La durée médiane est de 17,4 secondes. Si une corrélation existe entre le nombre de commandes et la durée, les variations importantes indiquent souvent des scripts complexes ou des tentatives de fingerprinting du honeypot.
*   **Tactiques observées :** Les attaquants cherchent fréquemment à installer des backdoors (clés SSH), collecter des informations système (`uname`, `df -h`) ou télécharger des exécutables (ex: variante Mirai "anthrax").
*   **Détection du honeypot :** Les attaquants utilisent des commandes spécifiques pour comparer les réponses du système (ex: `/proc/self/exe`, `df -h`) afin de distinguer un honeypot d'un véritable serveur Linux.

**Vulnérabilités associées :**
L'article ne mentionne pas de CVE spécifique, mais met en évidence des vecteurs d'attaques courants :
*   **Brute force et injection :** Tentatives récurrentes de modification de mots de passe et d'ajout de clés SSH (`authorized_keys`).
*   **Reconnaissance système :** Utilisation de `busybox` et de commandes système pour vérifier l'environnement.

**Recommandations pour les administrateurs de honeypots :**
*   **Améliorer la fidélité (Realism) :** Ajuster les réponses des commandes système (ex: `df -h`, `uptime`, `uname`) pour qu'elles correspondent à des sorties de systèmes réels et non à des valeurs par défaut de Cowrie, afin d'éviter le "fingerprinting" par les bots.
*   **Analyse comportementale :** Utiliser la durée des sessions et le nombre total de commandes comme indicateurs pour isoler les sessions les plus "intéressantes" (celles qui sortent de la norme des 22 commandes).
*   **Filtrage des données variables :** Pour identifier des campagnes d'attaques similaires, il est conseillé de concaténer et hasher les commandes en excluant les variables dynamiques (mots de passe, URLs de téléchargement).
*   **Maintenance :** Maintenir des configurations de honeypot à jour via Docker pour faciliter les tests de comparaison entre le leurre et une machine réelle.

---
[Source](https://isc.sans.edu/diary/rss/32840){:target="_blank"}
