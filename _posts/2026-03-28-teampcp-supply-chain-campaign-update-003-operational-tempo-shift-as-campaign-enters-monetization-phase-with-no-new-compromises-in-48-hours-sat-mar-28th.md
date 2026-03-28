---
title: 'TeamPCP Supply Chain Campaign: Update 003 - Operational Tempo Shift as Campaign Enters Monetization Phase With No New Compromises in 48 Hours, (Sat, Mar 28th)'
date: 2026-03-28
permalink: /posts/2026/03/28/teampcp-supply-chain-campaign-update-003-operational-tempo-shift-as-campaign-enters-monetization-phase-with-no-new-compromises-in-48-hours-sat-mar-28th/
tags:
- veille-cyber
- sans-isc
---
### Évolution de la campagne TeamPCP : Transition vers la monétisation

La campagne de compromission de la chaîne d'approvisionnement TeamPCP observe une pause inédite de 48 heures sans nouvelle infection, marquant probablement une transition opérationnelle : le groupe délaisse l'expansion pour se concentrer sur la monétisation des identifiants volés (environ 300 Go de données). Malgré cette accalmie, la menace reste élevée, notamment avec l'implication potentielle du ransomware Vect.

**Points clés :**
*   **Changement de stratégie :** TeamPCP privilégie l'exploitation des accès déjà acquis via une approche affiliée plutôt que de nouvelles compromissions de paquets.
*   **Détection comportementale :** Palo Alto Networks a publié des règles pour identifier les attaques CI/CD via des anomalies (accès mémoire, exfiltration vers des domaines récents) plutôt que par des indicateurs de compromission (IOC) fixes, qui changent à chaque vague.
*   **Exfiltration furtive :** Utilisation détournée de l'API GitHub Releases pour exfiltrer des données, rendant le trafic difficile à distinguer des usages légitimes.
*   **Analyse d'impact :** GitGuardian souligne un "effet boule de neige" avec un ratio de propagation des accès supérieur à 10 000:1 (un jeton volé expose des milliers de secrets en aval).

**Vulnérabilités :**
*   **CVE-2026-33634 :** Intégrée au catalogue CISA KEV ; la date limite de remédiation est fixée au 8 avril 2026.

**Recommandations :**
*   **Hygiène CI/CD :** Déployer les règles de détection comportementale de Palo Alto Networks et surveiller les comportements anormaux des runners (lecture de mémoire de processus, création d'archives suspectes).
*   **Sécurisation Kubernetes :** Appliquer les recommandations de la Cloud Security Alliance (CSA) : interdire les *DaemonSets* privilégiés et restreindre l'accès en écriture au système de fichiers hôte (`hostPath /`).
*   **Réponse aux incidents :** Maintenir une vigilance accrue et procéder immédiatement à la rotation des identifiants et au nettoyage des systèmes si ce n'est pas déjà fait.
*   **Surveillance :** Surveiller prioritairement toute activité liée au ransomware Vect et les déploiements non autorisés sur les pipelines CI/CD.

---
[Source](https://isc.sans.edu/diary/rss/32842){:target="_blank"}
