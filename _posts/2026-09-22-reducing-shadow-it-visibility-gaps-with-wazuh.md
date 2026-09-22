---
title: 'Reducing shadow IT visibility gaps with Wazuh'
date: 2026-09-22
permalink: /posts/2026/09/22/reducing-shadow-it-visibility-gaps-with-wazuh/
tags:
- veille-cyber
- bleepingcomp
---
### Combler les failles de visibilité du « Shadow IT » avec Wazuh

Le « Shadow IT » représente un risque majeur de sécurité, car les actifs non répertoriés ou non surveillés échappent aux contrôles standard. Si les scans réseau traditionnels mesurent la portée réseau, ils restent inefficaces pour détecter les systèmes isolés, les logiciels sans ports d'écoute ou les appareils éteints lors du scan.

**Points clés :**
*   **Limites du scan réseau :** Il ne détecte que les hôtes répondant au moment T, laissant dans l'ombre les terminaux hors ligne ou les applications sans écoute active (extensions de navigateur, outils en sortie seule).
*   **Approche centrée sur l'inventaire :** Wazuh utilise des agents pour collecter en continu l'état réel des terminaux (matériel, logiciels, services, utilisateurs, extensions de navigateur).
*   **Visibilité étendue :** La solution centralise les données, permettant une analyse granulaire sur l'ensemble du parc plutôt que sur des hôtes isolés.
*   **Surveillance hybride :** Pour les appareils ne supportant pas d'agent (imprimantes, routeurs), Wazuh utilise le monitoring sans agent (SSH) et l'ingestion de logs via Syslog.

**Vulnérabilités et risques associés :**
Bien que l'article n'énumère pas de CVE spécifiques, il souligne les vecteurs de risque suivants :
*   **Absence de correctifs :** Les terminaux non gérés ne remontent pas dans les rapports de vulnérabilité.
*   **Logiciels non autorisés :** Installation d'outils (accès distant, partage de fichiers) sur des postes gérés, augmentant la surface d'attaque.
*   **Logiciels en fin de vie (EOL) :** Absence de mises à jour de sécurité critiques.

**Recommandations :**
*   **Automatiser l'inventaire :** Déployer des agents pour maintenir une vision en temps réel du parc (OS, processus, services, ports d'écoute).
*   **Surveiller l'état des agents :** Suivre activement les statuts « déconnecté » ou « jamais connecté » pour identifier les angles morts de la couverture de sécurité.
*   **Corréler avec l'intelligence des menaces :** Utiliser les données d'inventaire pour détecter automatiquement les logiciels non approuvés ou obsolètes.
*   **Implémenter la réponse active :** Configurer des scripts de réponse automatisée via Wazuh pour supprimer ou isoler les applications non autorisées détectées sur le réseau.
*   **Audit des extensions :** Normaliser la visibilité des extensions de navigateur sur tous les systèmes d'exploitation pour identifier celles disposant de permissions excessives.

---
[Source](https://www.bleepingcomputer.com/news/security/reducing-shadow-it-visibility-gaps-with-wazuh/){:target="_blank"}
