---
title: 'International joint action disrupts world’s largest DDoS botnets'
date: 2026-03-20
permalink: /posts/2026/03/20/international-joint-action-disrupts-worlds-largest-ddos-botnets/
tags:
- veille-cyber
- bleepingcomp
---
### Démantèlement des plus grands botnets DDoS mondiaux

Une opération internationale impliquant les États-Unis, l'Allemagne et le Canada a neutralisé les infrastructures de commande et de contrôle (C2) des botnets **Aisuru, KimWolf, JackSkid et Mossad**. Ces réseaux, responsables d'attaques DDoS massives atteignant des records mondiaux, exploitaient plus de trois millions d'appareils IoT (caméras, enregistreurs vidéo, routeurs Wi-Fi) pour mener des campagnes d'extorsion et de sabotage.

**Points clés :**
*   **Capacité destructive :** Le botnet Aisuru a établi un record mondial avec une attaque de 31,4 Tbps.
*   **Modèle économique :** Les opérateurs utilisaient un modèle de « cybercriminalité à la demande », louant l'accès aux botnets à des tiers pour paralyser des infrastructures critiques, incluant des réseaux du Département de la Défense américain.
*   **Volume d'activité :** Plus de 300 000 commandes d'attaques ont été émises collectivement par ces quatre groupes.
*   **Collaboration :** L'action a nécessité une coopération entre agences gouvernementales et le secteur privé, notamment la société Akamai.

**Vulnérabilités :**
*   Bien qu'aucune CVE spécifique ne soit citée dans l'article, ces botnets exploitent la **faible sécurité par défaut des appareils IoT** (identifiants codés en dur, vulnérabilités logicielles non patchées, accès distants mal sécurisés).

**Recommandations :**
*   **Mise à jour régulière :** Appliquer systématiquement les correctifs de sécurité sur tous les objets connectés (IoT).
*   **Durcissement des configurations :** Modifier les identifiants et mots de passe par défaut lors de la mise en service de tout équipement.
*   **Segmentation réseau :** Isoler les appareils IoT sur des segments de réseau séparés pour limiter le risque de propagation en cas de compromission.
*   **Désactivation des services inutiles :** Fermer les ports et services distants (comme Telnet ou SSH) s'ils ne sont pas strictement nécessaires au fonctionnement de l'appareil.

---
[Source](https://www.bleepingcomputer.com/news/security/aisuru-kimwolf-jackskid-and-mossad-botnets-disrupted-in-joint-action/){:target="_blank"}
