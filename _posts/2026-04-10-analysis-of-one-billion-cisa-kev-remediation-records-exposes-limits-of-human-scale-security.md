---
title: 'Analysis of one billion CISA KEV remediation records exposes limits of human-scale security'
date: 2026-04-10
permalink: /posts/2026/04/10/analysis-of-one-billion-cisa-kev-remediation-records-exposes-limits-of-human-scale-security/
tags:
- veille-cyber
- bleepingcomp
---
### La fin de la sécurité à l'échelle humaine : le défi de l'asymétrie opérationnelle

L'analyse de plus d'un milliard d'enregistrements de remédiation issus de la base CISA KEV révèle une incapacité structurelle des modèles de cybersécurité actuels à suivre la vitesse des attaquants. Malgré une augmentation significative des efforts de correction (6,5 fois plus de tickets traités), le délai de traitement reste largement supérieur à la rapidité d'exploitation des vulnérabilités.

**Points clés**
* **Inversion du temps d'exploitation :** Le *Time-to-Exploit* est désormais négatif (environ -7 jours), signifiant que les vulnérabilités sont exploitées avant même la publication d'un correctif.
* **Le "Plafond humain" :** L'augmentation des effectifs ou des processus manuels ne permet plus de combler l'écart. 88 % des vulnérabilités critiques étudiées sont corrigées plus lentement qu'elles ne sont exploitées.
* **Le "Manual Tax" :** Les délais de remédiation sont étirés par des processus manuels inefficaces, particulièrement sur les systèmes d'infrastructure (ex: Cisco IOS XE) par rapport aux postes de travail.
* **Changement de métrique :** La gestion par nombre de CVE est obsolète. Il est désormais crucial de mesurer la « masse de risque » (actifs vulnérables multipliés par la durée d'exposition).
* **Menace IA :** L'émergence d'attaquants autonomes basés sur l'IA rend le modèle de défense « scan-et-rapport » totalement inopérant.

**Vulnérabilités notables citées (exemples d'écarts)**
* **Spring4Shell :** Exploitée 2 jours avant divulgation ; délai moyen de remédiation de 266 jours.
* **Cisco IOS XE :** Exploitée 1 mois avant divulgation ; délai moyen de remédiation de 263 jours.
* **Follina :** Exploitée 30 jours avant divulgation ; fenêtre d'exposition moyenne totale de 85 jours.

**Recommandations**
* **Passer aux opérations autonomes :** Abandonner le modèle manuel de gestion des tickets au profit d'un centre d'opérations de risque (Risk Operations Center) automatisé.
* **Automatisation en boucle fermée :** Mettre en œuvre des systèmes capables de valider activement l'exploitabilité d'une faille dans l'environnement spécifique et d'appliquer des correctifs sans intervention humaine directe.
* **Priorisation par la donnée :** Se concentrer sur les vulnérabilités réellement exploitables (seules 357 sur 48 172 vulnérabilités divulguées en 2025 étaient à la fois exploitables à distance et activement utilisées).
* **Évolution du rôle des experts :** Recentrer le personnel de sécurité sur la gouvernance des politiques et la supervision des systèmes autonomes, plutôt que sur l'exécution tactique des patchs.

---
[Source](https://www.bleepingcomputer.com/news/security/analysis-of-one-billion-cisa-kev-remediation-records-exposes-limits-of-human-scale-security/){:target="_blank"}
