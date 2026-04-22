---
title: 'Kyber ransomware gang toys with post-quantum encryption on Windows'
date: 2026-04-22
permalink: /posts/2026/04/22/kyber-ransomware-gang-toys-with-post-quantum-encryption-on-windows/
tags:
- veille-cyber
- bleepingcomp
---
### Le ransomware Kyber intègre le chiffrement post-quantique

Une nouvelle campagne du ransomware Kyber cible simultanément les environnements Windows et VMware ESXi afin de maximiser les dégâts. Bien que les auteurs revendiquent l'utilisation d'une cryptographie post-quantique (Kyber1024), celle-ci n'est réellement implémentée que sur la variante Windows, la version ESXi utilisant des méthodes plus conventionnelles.

**Points clés :**
* **Double vecteurs d'attaque :** Utilisation de deux variantes distinctes pour compromettre les serveurs de fichiers Windows et les infrastructures virtualisées (ESXi).
* **Cryptographie :** La version Windows utilise Kyber1024 et X25519 pour protéger les clés symétriques (AES-CTR), tandis que la version Linux/ESXi s'appuie sur RSA-4096 et ChaCha8.
* **Techniques destructrices :** Suppression des clichés instantanés (shadow copies), désactivation de la réparation au démarrage, arrêt des services critiques (SQL, Exchange, sauvegardes) et nettoyage des journaux d'événements.
* **Ciblage :** Les attaquants visent des entreprises de grande envergure, incluant des prestataires du secteur de la défense.

**Vulnérabilités :**
* Aucune CVE spécifique n'est mentionnée dans l'article. La menace repose sur des techniques d'exécution malveillante et de contournement des protections système plutôt que sur l'exploitation d'une faille logicielle identifiée.

**Recommandations :**
* **Sauvegardes immuables :** Maintenir des sauvegardes hors ligne ou immuables, car le ransomware est conçu pour supprimer les copies locales de récupération.
* **Sécurisation des environnements virtualisés :** Restreindre strictement l'accès aux interfaces de gestion ESXi et Hyper-V.
* **Surveillance des services :** Mettre en place des alertes sur l'arrêt inopiné des services de base de données (SQL, Exchange) ou de sauvegarde, signes avant-coureurs d'une attaque imminente.
* **Hygiène système :** Désactiver les fonctionnalités inutilisées, purger régulièrement les logs de sécurité pour déceler des activités anormales et surveiller la création de mutex suspects.

---
[Source](https://www.bleepingcomputer.com/news/security/kyber-ransomware-gang-toys-with-post-quantum-encryption-on-windows/){:target="_blank"}
