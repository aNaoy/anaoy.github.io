---
title: 'Askul confirms theft of 740k customer records in ransomware attack'
date: 2025-12-16
permalink: /posts/2025/12/16/askul-confirms-theft-of-740k-customer-records-in-ransomware-attack/
tags:
- veille-cyber
- bleepingcomp
---
**Attaque RansomHouse sur Askul : Vol massif de données clients**

Le géant japonais du commerce électronique Askul a confirmé qu'une attaque par ransomware par le groupe RansomHouse a entraîné le vol d'environ 740 000 enregistrements clients. L'incident, survenu en octobre, a causé une panne des systèmes informatiques, impactant les expéditions et affectant des partenaires tels que Muji. Les données compromises incluent des informations relatives aux clients professionnels et individuels, aux partenaires commerciaux, ainsi qu'aux dirigeants et employés.

**Points Clés :**

*   **Victime :** Askul Corporation, géant japonais du commerce électronique.
*   **Attaquant :** RansomHouse.
*   **Type d'attaque :** Ransomware et vol de données.
*   **Données volées :** Environ 740 000 enregistrements (clients professionnels et individuels, partenaires, employés).
*   **Conséquences immédiates :** Panne des systèmes IT, suspension des expéditions, impacts sur les partenaires.
*   **Ransomware :** Utilisation de multiples variantes, certaines ayant contourné les protections EDR. Les sauvegardes ont été effacées.

**Vulnérabilités Identifiées :**

*   **Credentials compromise :** L'intrusion initiale a eu lieu via des identifiants d'authentification compromis d'un compte administrateur d'un partenaire externalisé.
*   **Absence de MFA :** Le compte du partenaire externalisé ne disposait pas de l'authentification multi-facteurs (MFA), facilitant l'accès initial.
*   **Désactivation des protections :** Les attaquants ont désactivé les logiciels de contre-mesure aux vulnérabilités, tels que l'EDR.

**Recommandations et Mesures prises par Askul :**

*   **Notification :** Notification aux clients et partenaires affectés, ainsi qu'à la Commission de Protection des Informations Personnelles du Japon.
*   **Surveillance :** Mise en place d'une surveillance à long terme pour prévenir la mauvaise utilisation des informations volées.
*   **Restauration des systèmes :** Travail en cours pour rétablir complètement les systèmes.
*   **Contrôles de sécurité renforcés :**
    *   Application de la MFA sur tous les systèmes clés.
    *   Réinitialisation des mots de passe de tous les comptes administrateurs.
    *   Mise à jour des signatures EDR.
*   **Isolation :** Déconnexion physique des réseaux infectés, isolement des appareils affectés, coupure des communications entre les centres de données et les centres logistiques.

À ce jour, les expéditions de commandes sont toujours impactées, et l'évaluation complète de l'impact financier est en cours.

---
[Source](https://www.bleepingcomputer.com/news/security/askul-confirms-theft-of-740k-customer-records-in-ransomhouse-attack/){:target="_blank"}
