---
title: 'New Fluent Bit Flaws Expose Cloud to RCE and Stealthy Infrastructure Intrusions'
date: 2025-11-24
permalink: /posts/2025/11/24/new-fluent-bit-flaws-expose-cloud-to-rce-and-stealthy-infrastructure-intrusions/
tags:
- veille-cyber
- hackernews
---
**Vulnérabilités Critiques dans Fluent Bit Permettant le Dépassement de la Sécurité et l'Intrusion d'Infrastructure**

Cinq failles de sécurité ont été identifiées dans Fluent Bit, un agent de télémétrie open-source, qui, une fois combinées, peuvent mener à la compromission totale des infrastructures cloud. Ces vulnérabilités autorisent le contournement de l'authentification, le parcours de répertoire, l'exécution de code à distance, le déni de service et la manipulation des étiquettes (tags).

**Points Clés :**

*   La chaîne d'exploitation de ces failles permet aux attaquants de perturber les services cloud, de manipuler des données, de s'infiltrer plus profondément dans les infrastructures cloud et Kubernetes, et de dissimuler leurs traces.
*   La popularité de Fluent Bit dans les environnements d'entreprise rend ces vulnérabilités particulièrement préoccupantes, potentiellement affectant l'accès aux services cloud, la manipulation de données et le contrôle du service de journalisation lui-même.

**Vulnérabilités Identifiées :**

*   **CVE-2025-12972** : Vulnérabilité de parcours de répertoire due à l'utilisation d'étiquettes non assainies pour les noms de fichiers de sortie, permettant l'écriture ou la réécriture de fichiers arbitraires. Ceci peut mener à la falsification de logs et à l'exécution de code à distance.
*   **CVE-2025-12970** : Dépassement de tampon sur la pile dans le plugin d'entrée Docker Metrics (in_docker), pouvant causer l'exécution de code ou planter l'agent via des noms de conteneurs excessivement longs.
*   **CVE-2025-12978** : Failles dans la logique de correspondance d'étiquettes permettant l'usurpation d'étiquettes de confiance (en devinant le premier caractère d'une clé d'étiquette). Ceci peut détourner les logs, contourner les filtres et injecter des enregistrements malveillants sous des étiquettes de confiance.
*   **CVE-2025-12977** : Validation d'entrée incorrecte des étiquettes dérivées de champs contrôlés par l'utilisateur, permettant l'injection de nouvelles lignes, séquences de parcours et caractères de contrôle pour corrompre les logs.
*   **CVE-2025-12969** : Absence d'authentification `security.users` dans le plugin `in_forward` (utilisé pour recevoir des logs via le protocole Forward), permettant l'envoi de logs falsifiés, l'injection de télémétrie erronée et le bombardement des logs de sécurité avec de faux événements.

**Recommandations :**

*   Mettre à jour vers les versions corrigées de Fluent Bit, notamment les versions 4.1.1 et 4.0.12.
*   Éviter l'utilisation d'étiquettes dynamiques pour le routage.
*   Restreindre les chemins et destinations de sortie pour prévenir l'expansion ou le parcours de répertoire basé sur les étiquettes.
*   Monter les fichiers de configuration et le répertoire `/fluent-bit/etc/` en lecture seule pour empêcher la falsification à l'exécution.
*   Exécuter le service avec des utilisateurs non privilégiés (non-root).

---
[Source](https://thehackernews.com/2025/11/new-fluent-bit-flaws-expose-cloud-to.html){:target="_blank"}
