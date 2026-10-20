---
title: 'Go Issues Emergency Update Blocking Eight CA Keys Over Undisclosed Security Concerns'
date: 2026-10-20
permalink: /posts/2026/10/20/go-issues-emergency-update-blocking-eight-ca-keys-over-undisclosed-security-concerns/
tags:
- veille-cyber
- hackernews
---
### Mise à jour d'urgence Go : Blocage de certificats eMudhra

L'équipe Go a publié les versions **1.27.3** et **1.26.10** pour bloquer huit clés intermédiaires d'autorité de certification (CA) en raison de problèmes de sécurité non divulgués. Cette mesure « urgente » empêche les programmes Go de valider les chaînes de certificats utilisant ces clés spécifiques, issues de l'entité eMudhra (emSign).

**Points clés :**
* **Action coordonnée :** Mozilla a également ajouté six de ces certificats à sa liste de révocation (OneCRL) quelques jours auparavant, bien que les détails précis des vulnérabilités restent confidentiels.
* **Impact technique :** Le filtre opère en comparant les hashs SHA-256 des clés publiques. Il est impossible de le désactiver, même pour des déploiements privés utilisant ces clés.
* **Obsolescence forcée :** Les applications utilisant ces certificats doivent être impérativement redéployées après reconstruction avec les nouvelles versions de Go pour restaurer la connectivité.
* **Ciblage :** Huit clés sont concernées, incluant des certificats TLS (DV, OV, EV) et de signature de code (CS) sous les racines *emSign Root TLS CA - G3* et *emSign Root CS CA - G3*.

**Vulnérabilités :**
* Aucune CVE n'a été officiellement associée à cet incident. L'équipe Go qualifie la situation de menace pour l'intégrité de l'écosystème, sans apporter de précisions supplémentaires.

**Recommandations :**
* **Mise à jour immédiate :** Passer aux versions Go 1.27.3 ou 1.26.10 dès que possible.
* **Audit des certificats :** Vérifier si les services ou infrastructures utilisent des certificats émis par les intermédiaires eMudhra cités.
* **Renouvellement :** Remplacer tout certificat utilisant ces chaînes compromises par de nouveaux certificats délivrés par une autre autorité de certification non restreinte.

---
[Source](https://thehackernews.com/2026/10/go-issues-emergency-update-blocking.html){:target="_blank"}
