---
title: 'TeamPCP Weekly Analysis: 2026-W18 (2026-04-27 through 2026-05-03), (Mon, May 4th)'
date: 2026-05-04
permalink: /posts/2026/05/04/teampcp-weekly-analysis-2026-w18-2026-04-27-through-2026-05-03-mon-may-4th/
tags:
- veille-cyber
- sans-isc
---
### Analyse de la campagne TeamPCP : Propagation multi-écosystèmes et défaillance critique des outils d'extorsion

La semaine 18 de 2026 a été marquée par une intensification significative des activités du groupe **TeamPCP**, avec le déploiement du ver « Mini Shai-Hulud » et la découverte d'une faille critique dans leur outil de ransomware.

**Points clés :**
*   **Ver multi-écosystèmes :** Le ver Mini Shai-Hulud a réussi une propagation automatisée entre trois écosystèmes (npm, PyPI et Packagist) en moins de 36 heures, compromettant des paquets officiels (SAP, PyTorch Lightning, Intercom).
*   **Ciblage des agents IA :** Pour la première fois, une attaque de supply chain exploite délibérément les fichiers de configuration d'outils de codage IA (`.claude/settings.json`, `.vscode/tasks.json`) pour assurer la persistance de l'attaquant.
*   **Échec de monétisation :** Le partenaire d'extorsion de TeamPCP, Vect 2.0, s'est révélé être un « wiper » accidentel. En raison d'une réutilisation de nonce dans l'algorithme ChaCha20-IETF, tout fichier dépassant 128 Ko est définitivement corrompu, rendant le paiement de la rançon inutile pour la récupération des données.
*   **Silence institutionnel :** Malgré l'impact sur des entreprises majeures (SAP), les autorités (CISA, Five Eyes) n'ont émis aucune alerte spécifique concernant TeamPCP, créant un décalage inquiétant entre la menace réelle et la réponse publique.

**Vulnérabilités mentionnées :**
*   **Vect 2.0 (Logiciel malveillant) :** Faille de réutilisation de nonce dans l'implémentation ChaCha20-IETF, entraînant la destruction irréversible des fichiers > 128 Ko.
*   **CVE-2024-1708 :** Vulnérabilité de traversée de chemin dans ConnectWise ScreenConnect (non liée à TeamPCP, mais ajoutée au catalogue KEV).
*   **CVE-2026-31431 :** Escalade de privilèges locale dans le noyau Linux (non liée à TeamPCP, ajoutée au KEV).

**Recommandations :**
*   **Audit des configurations IA :** Examiner les répertoires `.claude/` et `.vscode/` pour détecter toute modification non autorisée dans les fichiers de tâches ou de paramètres.
*   **Révision de la chaîne d'approvisionnement :** Vérifier l'intégrité des dépendances npm, PyPI et Packagist installées récemment (notamment les versions spécifiques des paquets SAP, Lightning AI et intercom-client).
*   **Ne pas payer Vect 2.0 :** En cas d'infection par ce ransomware, il est inutile de payer, car le chiffrement est irréversible pour les fichiers volumineux.
*   **Gestion des secrets :** Considérant le vol massif de jetons (GitHub, AWS, Azure, GCP, Kubernetes) lors de cette campagne, une rotation immédiate de tous les secrets et clés d'API potentiellement compromis est impérative pour les organisations ayant utilisé les paquets affectés.

---
[Source](https://isc.sans.edu/diary/rss/32950){:target="_blank"}
