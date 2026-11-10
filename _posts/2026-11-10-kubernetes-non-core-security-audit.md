---
title: 'Kubernetes Non-Core Security Audit'
date: 2026-11-10
permalink: /posts/2026/11/10/kubernetes-non-core-security-audit/
tags:
- veille-cyber
- zerodaysfans
---
### Audit de sécurité de l'écosystème Kubernetes « Non-Core »

Shielder a réalisé un audit de sécurité approfondi sur divers composants et sous-projets de l'écosystème Kubernetes, initialement exclus des audits du cœur du système. Cette mission, menée avec l'OSTIF, a permis d'identifier 19 vulnérabilités (4 critiques, 5 majeures, 7 mineures, 3 informatives) en adoptant une approche par composant et par modèle de menace dédié.

#### Points clés et vulnérabilités identifiées

*   **Coercition NTLM sur les nœuds Windows (CVE-2026-76654) :** Une manipulation via le champ `subPath` permet de forcer le nœud à s'authentifier auprès d'une machine contrôlée par un attaquant, exposant potentiellement des hachages NetNTLMv2. Bien qu'un correctif existe, des comportements suspects persistent.
*   **Identifiants codés en dur (CVE-2025-7342) :** Des scripts de construction d'images (OVA/Nutanix) pour *Image Builder* contenaient des mots de passe administrateur par défaut, exposant les hôtes à une compromission distante. Le correctif est disponible.
*   **Path Traversal dans Cluster API :** La commande `clusterctl generate` ne valide pas les entrées du paramètre `--flavor`, permettant à un attaquant de forcer le téléchargement et l'application de fichiers YAML arbitraires depuis GitHub.
*   **Contournement de la politique Pod Security Admission (PSS) :** Une faiblesse dans la gestion des profils AppArmor sur Debian/Ubuntu permet aux pods d'utiliser des profils `Localhost` qui agissent comme des alias pour `unconfined`, neutralisant les protections basiques attendues.

#### Recommandations

*   **Nœuds Windows :** Restreindre strictement les connexions NTLM sortantes au niveau du réseau.
*   **Cluster API :** S'assurer qu'aucune entrée non fiable ne soit transmise à l'option `--flavor` lors de l'utilisation de `clusterctl`.
*   **Gestion des composants tiers :** Étant donné la diversité et la gouvernance variable des sous-projets Kubernetes, les administrateurs doivent systématiquement vérifier la provenance des composants (notamment les pilotes CSI exécutés avec des privilèges root) et maintenir une veille active sur les correctifs.
*   **Suivi :** Consulter régulièrement les problèmes publics et les pull requests des projets concernés, car plusieurs vulnérabilités sont encore en cours de traitement ou font l'objet de discussions communautaires.

---
[Source](https://www.shielder.com/blog/2026/11/kubernetes-non-core-security-audit/){:target="_blank"}
