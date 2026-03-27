---
title: 'Bearlyfy Hits Russian Firms with Custom GenieLocker Ransomware'
date: 2026-03-27
permalink: /posts/2026/03/27/bearlyfy-hits-russian-firms-with-custom-genielocker-ransomware/
tags:
- veille-cyber
- hackernews
---
### Offensive cybernétique : Le groupe Bearlyfy cible les entreprises russes avec GenieLocker

Le groupe pro-ukrainien **Bearlyfy** (alias Labubu) mène une campagne active contre des entreprises russes depuis début 2025. Initialement axé sur l'utilisation de souches existantes (LockBit 3, Babuk, PolyVice), le groupe a récemment développé son propre ransomware baptisé **GenieLocker**, dont le mécanisme de chiffrement s'inspire des familles Venus et Trinity. Avec plus de 70 attaques à son actif, le groupe adopte une double stratégie d'extorsion financière et de sabotage.

**Points clés :**
*   **Évolution tactique :** Le groupe a gagné en sophistication, passant d'attaques opportunistes contre des PME à des opérations visant de grandes entreprises.
*   **Mode opératoire :** Accès initial via l'exploitation de services externes et d'applications vulnérables, suivi du déploiement de **MeshAgent** pour la persistance et le contrôle à distance.
*   **Absence d'automatisation :** Contrairement aux ransomwares classiques, les demandes de rançon ne sont pas générées par le logiciel, mais rédigées manuellement par les attaquants pour accentuer la pression psychologique.
*   **Alliances :** Des recoupements ont été observés avec les groupes PhantomCore et Head Mare.

**Vulnérabilités :**
*   L'article ne mentionne pas de CVE spécifiques, mais souligne que l'entrée initiale repose sur l'exploitation systématique des **services exposés sur Internet** et des **vulnérabilités d'applications**.

**Recommandations :**
*   **Gestion des surfaces d'exposition :** Auditer et restreindre rigoureusement l'accès aux services exposés sur Internet (VPN, portails RDP, interfaces d'administration).
*   **Gestion des vulnérabilités :** Appliquer une politique stricte de mise à jour (patch management) pour toutes les applications accessibles depuis l'extérieur.
*   **Détection d'outils d'administration à distance :** Surveiller et détecter l'utilisation non autorisée d'outils de gestion légitimes (comme MeshAgent) souvent détournés par les attaquants pour maintenir leur présence.
*   **Stratégie de sauvegarde :** Maintenir des sauvegardes immuables et déconnectées du réseau principal pour limiter l'impact des activités de chiffrement.

---
[Source](https://thehackernews.com/2026/03/bearlyfy-hits-70-russian-firms-with.html){:target="_blank"}
