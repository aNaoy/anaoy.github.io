---
title: 'TeamPCP Supply Chain Campaign: Activity Through 2026-05-17, (Mon, May 18th)'
date: 2026-05-19
permalink: /posts/2026/05/19/teampcp-supply-chain-campaign-activity-through-2026-05-17-mon-may-18th/
tags:
- veille-cyber
- sans-isc
---
### Intensification de la campagne TeamPCP : Compromissions logicielles et vers auto-propagés

La campagne TeamPCP a récemment franchi une étape majeure avec deux incidents critiques survenus en 48 heures : la compromission du plugin Jenkins de Checkmarx et le déploiement du ver "Mini Shai-Hulud" via les écosystèmes npm et PyPI. Cette vague d'attaques se distingue par l'utilisation de signatures numériques légitimes (provenance SLSA Build Level 3), prouvant que la validation de la provenance ne garantit plus l'intégrité du code.

#### Points clés
*   **Compromission Checkmarx :** Le plugin Jenkins AST a été piégé (version 2026.5.09), marquant la troisième intrusion chez Checkmarx en trois mois.
*   **Ver Mini Shai-Hulud :** Une attaque de supply chain a empoisonné environ 170 paquets (dont la suite @tanstack). Le ver a été publié via le pipeline de publication légitime de TanStack en abusant des workflows CI/CD et en extrayant des tokens OIDC.
*   **Comportement destructeur :** Le ver inclut un mécanisme de sabotage probabiliste (1 chance sur 6) ciblant les systèmes en Israël et en Iran, ainsi qu'une persistance au sein des outils de développement (VS Code, Claude).
*   **PCPJack :** Un ver concurrent, probablement opéré par un ancien affilié, traque et élimine les infections TeamPCP avant de voler les identifiants.

#### Vulnérabilités identifiées
*   **CVE-2026-45321 (CVSS 9.6) :** Identifiant de suivi pour la compromission des paquets TanStack (alias GHSA-g7cv-rxg3-hmpx).
*   **Vulnérabilités exploitées par PCPJack :** CVE-2025-29927, CVE-2025-55182, CVE-2026-1357, CVE-2025-9501 et CVE-2025-48703.

#### Recommandations
*   **Audit de dépendances :** Inventorier les installations des paquets touchés (TanStack, Mistral AI, etc.) réalisés pendant les fenêtres de compromission.
*   **Sécurisation CI/CD :** Ne plus se fier uniquement à la provenance SLSA. Verrouiller les versions (pinning) et vérifier les hashs des fichiers lockfile.
*   **Rotation des secrets :** Révoquer les jetons npm, GitHub et cloud exposés aux runners CI/CD compromis.
*   **Remédiation Jenkins :** S'assurer d'utiliser les versions corrigées du plugin Checkmarx Jenkins (2.0.13-848.v76e89de8a_053 ou 2.0.13-847.v08c0072b_2fd5).
*   **Inspection des endpoints :** Vérifier les fichiers de configuration `.vscode/tasks.json` et `~/.claude/settings.json` à la recherche de hooks de persistance.
*   **Filtrage réseau :** Bloquer les indicateurs de compromission, notamment l'IP C2 `83.142.209.194` et les domaines `git-tanstack.com` ainsi que les nœuds d'exfiltration `getsession.org`.

---
[Source](https://isc.sans.edu/diary/rss/32994){:target="_blank"}
