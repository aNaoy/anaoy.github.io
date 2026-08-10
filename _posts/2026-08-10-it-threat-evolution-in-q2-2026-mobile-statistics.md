---
title: 'IT threat evolution in Q2 2026. Mobile statistics'
date: 2026-08-10
permalink: /posts/2026/08/10/it-threat-evolution-in-q2-2026-mobile-statistics/
tags:
- veille-cyber
- securelist
---
### Évolution des menaces mobiles : Rapport Q2 2026

Le second trimestre 2026 marque une tendance à la baisse des attaques sur terminaux mobiles, avec 1 996 823 incidents enregistrés contre 2 676 328 au trimestre précédent. Cette diminution est notamment attribuée au déploiement de correctifs sur le micrologiciel (firmware) des appareils, réduisant l'efficacité des chevaux de Troie préinstallés.

#### Points clés
*   **Volume de menaces :** 304 128 nouveaux packages d'installation malveillants ont été détectés.
*   **Dominance des banquiers :** Les chevaux de Troie bancaires restent la menace la plus répandue (30,77 % des applications détectées), bien que leur volume global diminue.
*   **Évolution des tactiques :** Les attaquants privilégient désormais les "Trojan-Droppers" pour distribuer des charges utiles malveillantes, une méthode permettant de contourner plus efficacement les processus de vérification des boutiques d'applications (ex: Google Play).
*   **Ciblage précis :** Utilisation de serveurs de commande et de contrôle (C2) qui vérifient la source d'installation via des SDK d'analyse pour ne déployer la charge malveillante que sur des cibles spécifiques, évitant ainsi la détection par les scanners automatiques.

#### Vulnérabilités et familles de malwares
Le rapport ne mentionne pas de CVE spécifique, mais met en lumière des vecteurs d'attaque persistants :
*   **Familles prédominantes :** *Backdoor.AndroidOS.Triada* reste omniprésent, suivi par les diverses variantes de *Trojan-Banker.AndroidOS.Mamont*, qui font l'objet d'un développement actif et d'itérations fréquentes.
*   **Techniques de contournement :** Utilisation d'applications légitimes (ex: lecteurs PDF) "trojanisées" pour télécharger des malwares bancaires (ex: Anatsa) après l'installation, en demandant de fausses mises à jour.

#### Recommandations
*   **Mise à jour du système :** Installer systématiquement les correctifs de sécurité fournis par les constructeurs pour limiter les risques liés aux malwares préinstallés.
*   **Vigilance post-installation :** Se méfier des applications demandant des mises à jour immédiates ou des autorisations inhabituelles après leur lancement, même si elles proviennent de sources officielles.
*   **Analyse des permissions :** Limiter l'accès aux fonctionnalités sensibles (Accessibilité, lecture des SMS) des applications installées sur Android.
*   **Utilisation d'outils de sécurité :** Maintenir des solutions de protection mobile à jour pour détecter les objets malveillants génériques et les comportements suspects de type "Dropper".

---
[Source](https://securelist.com/malware-report-q2-2026-mobile-statistics/120948/){:target="_blank"}
