---
title: 'New WrtHug campaign hijacks thousands of end-of-life ASUS routers'
date: 2025-11-19
permalink: /posts/2025/11/19/new-wrthug-campaign-hijacks-thousands-of-end-of-life-asus-routers/
tags:
- veille-cyber
- bleepingcomp
---
## Opération WrtHug : Des milliers de routeurs ASUS compromis

Une campagne mondiale, baptisée Opération WrtHug, cible et détourne des milliers de routeurs ASUS WRT, majoritairement obsolètes. Ces attaques exploitent six vulnérabilités, affectant près de 50 000 adresses IP uniques dans le monde, avec une concentration notable à Taïwan, mais aussi en Asie du Sud-Est, en Russie, en Europe centrale et aux États-Unis. Les chercheurs suggèrent un lien possible avec la campagne AyySSHush, basée sur les méthodes d'attaque et le ciblage.

**Points Clés :**

*   **Cible :** Routeurs ASUS WRT, souvent obsolètes.
*   **Activité :** Détournement de milliers d'appareils à l'échelle mondiale.
*   **Mécanisme d'attaque :** Exploitation de vulnérabilités, notamment via le service AiCloud.
*   **Indicateur de compromission :** Présence d'un certificat TLS auto-signé de 100 ans dans les services AiCloud, remplaçant le certificat ASUS original.
*   **Modèles affectés :** Divers modèles des séries AC et AX, dont 4G-AC55U, 4G-AC860U, DSL-AC68U, GT-AC5300, GT-AX11000, RT-AC1200HP, RT-AC1300GPLUS, RT-AC1300UHP.
*   **Objectif présumé :** Utilisation des routeurs compromis comme relais pour masquer des opérations de piratage chinoises.

**Vulnérabilités exploitées :**

*   **CVE-2023-41345, CVE-2023-41346, CVE-2023-41347, CVE-2023-41348 :** Injection de commandes OS via modules de token.
*   **CVE-2023-39780 :** Défaut majeur d'injection de commandes (également utilisé dans AyySSHush).
*   **CVE-2024-12912 :** Exécution de commandes arbitraires.
*   **CVE-2025-2492 :** Contrôle d'authentification inapproprié menant à une exécution non autorisée de fonctions (qualifié de critique par ASUS).

**Recommandations :**

*   **Mise à jour du firmware :** Installer la dernière version disponible pour corriger les vulnérabilités.
*   **Remplacement des appareils obsolètes :** Pour les routeurs qui ne sont plus pris en charge par des mises à jour.
*   **Désactivation de l'accès à distance :** Si le remplacement n'est pas immédiat.

---
[Source](https://www.bleepingcomputer.com/news/security/new-wrthug-campaign-hijacks-thousands-of-end-of-life-asus-routers/){:target="_blank"}
