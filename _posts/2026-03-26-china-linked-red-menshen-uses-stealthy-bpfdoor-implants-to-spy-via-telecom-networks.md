---
title: 'China-Linked Red Menshen Uses Stealthy BPFDoor Implants to Spy via Telecom Networks'
date: 2026-03-26
permalink: /posts/2026/03/26/china-linked-red-menshen-uses-stealthy-bpfdoor-implants-to-spy-via-telecom-networks/
tags:
- veille-cyber
- hackernews
---
### Menace persistante : Red Menshen et le backdoor BPFDoor dans les réseaux télécoms

Le groupe de menace persistante avancée **Red Menshen** (aussi connu sous les noms Earth Bluecrow, DecisiveArchitect ou Red Dev 18) mène une campagne d'espionnage longue durée ciblant les infrastructures de télécommunications en Asie et au Moyen-Orient. Ce groupe se distingue par l'utilisation de mécanismes d'accès extrêmement furtifs, conçus pour s'implanter durablement au cœur des réseaux critiques.

**Points clés :**
*   **Ciblage stratégique :** L'attaque vise les infrastructures télécoms pour espionner des réseaux gouvernementaux et surveiller les communications des abonnés.
*   **Furtivité avancée :** Le groupe utilise des outils comme **BPFDoor**, un backdoor Linux qui n'ouvre aucun port d'écoute et n'émet aucun signal sortant conventionnel.
*   **Méthode opératoire :** Le malware utilise la technologie *Berkeley Packet Filter* (BPF) pour inspecter le trafic directement dans le noyau (kernel). Il ne s'active que lorsqu'il reçoit un « paquet magique » spécifique.
*   **Évolution :** Les variantes récentes masquent ces paquets d'activation dans du trafic HTTPS légitime et utilisent le protocole ICMP pour communiquer entre hôtes infectés.

**Vulnérabilités exploitées :**
*   Le vecteur d'infection initial repose sur l'exploitation d'infrastructures exposées sur Internet : VPN, firewalls et passerelles web (Ivanti, Cisco, Juniper, Fortinet, VMware, Palo Alto Networks, Apache Struts).
*   *Note : L'article ne mentionne pas de CVE spécifiques, mais souligne l'abus de failles dans les services de périphérie (Edge Services).*

**Logiciels malveillants identifiés :**
*   **BPFDoor :** Backdoor principal.
*   **Frameworks de post-exploitation :** CrossC2, Sliver, TinyShell.
*   **Outils annexes :** Keyloggers et utilitaires de force brute pour le vol d'identifiants et le déplacement latéral.

**Recommandations :**
*   **Durcissement des accès :** Sécuriser rigoureusement les équipements exposés sur Internet (VPN, firewalls) en appliquant systématiquement les correctifs de sécurité.
*   **Surveillance réseau approfondie :** Détecter les anomalies dans les paquets, notamment ceux encapsulés dans le trafic HTTPS ou utilisant ICMP de manière inhabituelle.
*   **Inspection noyau :** Étant donné que ces menaces opèrent au niveau du kernel, il est crucial d'utiliser des solutions EDR capables d'analyser l'intégrité du système et les comportements au niveau des appels système, plutôt que de se fier uniquement aux solutions antivirus classiques.
*   **Segmentation :** Isoler les composants critiques des réseaux de télécommunications pour limiter les capacités de déplacement latéral des attaquants.

---
[Source](https://thehackernews.com/2026/03/china-linked-red-menshen-uses-stealthy.html){:target="_blank"}
