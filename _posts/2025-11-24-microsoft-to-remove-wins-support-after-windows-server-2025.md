---
title: 'Microsoft to remove WINS support after Windows Server 2025'
date: 2025-11-24
permalink: /posts/2025/11/24/microsoft-to-remove-wins-support-after-windows-server-2025/
tags:
- veille-cyber
- bleepingcomp
---
**Suppression de WINS : Préparation à la Transition vers DNS**

Microsoft a annoncé le retrait du service Windows Internet Name Service (WINS) des futures versions de Windows Server, à partir de celles qui suivront Windows Server 2025. Le support standard de WINS se poursuivra jusqu'en novembre 2034, période durant laquelle il est fortement conseillé aux administrateurs de migrer vers des solutions de résolution de noms basées sur le DNS.

WINS, un système hérité pour l'enregistrement et la résolution des noms d'ordinateurs, a été officiellement déprécié avec la sortie de Windows Server 2022 en août 2021. Sa suppression entraînera la disparition du rôle serveur WINS, de sa console de gestion, et de ses interfaces d'automatisation.

Les raisons invoquées par Microsoft pour cette décision incluent la supériorité du DNS en termes de scalabilité et de conformité aux normes modernes, ainsi que les protections de sécurité offertes par DNSSEC contre les attaques de cache poisoning et de spoofing, que WINS/NetBIOS ne peut pas contrer. De plus, les services Microsoft actuels, tels qu'Active Directory et les plateformes cloud, dépendent intrinsèquement du DNS pour la résolution de noms.

**Points clés :**

*   **Fin du support de WINS :** WINS sera retiré des versions de Windows Server après Windows Server 2025.
*   **Dernière version avec support :** Windows Server 2025 sera la dernière version à inclure WINS.
*   **Fin du support standard :** Le support standard de WINS se terminera en novembre 2034.
*   **Motif de la suppression :** Scalabilité, conformité aux normes, et sécurité renforcée du DNS par rapport à WINS/NetBIOS.

**Vulnérabilités :**

Bien que l'article ne détaille pas de vulnérabilités spécifiques avec des identifiants CVE associés à WINS lui-même, il souligne indirectement les faiblesses de WINS/NetBIOS en matière de sécurité par rapport au DNS moderne :

*   **Absence de protection contre le cache poisoning et le spoofing :** Contrairement à DNSSEC, WINS/NetBIOS n'offre pas de mitigation contre ces types d'attaques.

**Recommandations :**

*   **Migration vers DNS :** Les organisations utilisant encore WINS doivent entamer dès maintenant la planification de leur migration vers des solutions basées sur le DNS.
*   **Audit des dépendances :** Identifier tous les services et applications qui dépendent encore de la résolution de noms NetBIOS via WINS.
*   **Stratégies de remplacement :** Utiliser des fonctionnalités DNS telles que les forwarders conditionnels, le split-brain DNS, ou les listes de suffixes de recherche pour reproduire la fonctionnalité de WINS.
*   **Éviter les solutions temporaires :** Ne pas recourir à des solutions de contournement non durables comme les fichiers hôtes statiques dans un environnement d'entreprise.
*   **Évaluation des plans de migration :** Examiner et valider les plans de migration vers DNS pour assurer une transition sans interruption.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-to-remove-wins-support-after-windows-server-2025/){:target="_blank"}
