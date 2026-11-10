---
title: 'France Blames Iran for Sabotage Attack on Refrigeration Controllers at About 700 Retail Sites'
date: 2026-11-10
permalink: /posts/2026/11/10/france-blames-iran-for-sabotage-attack-on-refrigeration-controllers-at-about-700-retail-sites/
tags:
- veille-cyber
- hackernews
---
### Sabotage informatique : Attaque iranienne contre les systèmes de réfrigération en France

La France a formellement attribué une campagne de sabotage cybernétique, survenue en octobre, à l'unité iranienne « Shahid Kaveh », liée au Corps des Gardiens de la révolution islamique (CGRI). Cette opération, opérant sous les bannières de hacktivistes comme *CyberAveng3rs*, a ciblé les interfaces web de contrôleurs de réfrigération industrielle, causant des pertes alimentaires majeures et une vingtaine d'incendies dans environ 700 sites de vente au détail (notamment la grande distribution).

#### Points clés
*   **Mode opératoire :** Les attaquants ont exploité des interfaces web exposées pour modifier les cycles de dégivrage, désactiver les alarmes de sécurité des sondes de température et provoquer des surchauffes.
*   **Cibles :** Équipements Danfoss, Dixell, Copeland et Schneider Electric.
*   **Enquête :** La justice française a ouvert une enquête pour interférence illégale dans des systèmes informatiques et mise en danger de la vie d'autrui, avec demande de mandats d'arrêt internationaux.
*   **Contexte :** Il s'agit de la première campagne offensive de sabotage cybernétique documentée sur le territoire français.

#### Vulnérabilités identifiées
L'attaque repose principalement sur l'**exposition directe d'interfaces de gestion à Internet**. Aucun CVE spécifique n'est mentionné, mais l'utilisation de configurations par défaut et l'absence de mises à jour de sécurité sur des systèmes en fin de vie (EOL) facilitent la ré-infection immédiate après une réinitialisation.

#### Recommandations de sécurité (CERT-FR)
*   **Isolation réseau :** Supprimer immédiatement l'exposition directe des contrôleurs sur Internet. L'accès distant doit exclusivement passer par un VPN sécurisé ou un réseau protégé.
*   **Hygiène des systèmes :**
    *   Réinitialiser les appareils compromis aux paramètres d'usine et reconfigurer intégralement les paramètres de sécurité.
    *   Modifier systématiquement les mots de passe par défaut.
    *   Appliquer les mises à jour de firmware recommandées par les constructeurs.
*   **Mesures d'urgence :** Le filtrage IP par pare-feu est une mesure temporaire insuffisante ; seule une isolation réseau réelle est préconisée.
*   **Gestion des risques :** Vérifier les conditions contractuelles d'assurance avant toute interruption de flux de données et remplacer tout matériel arrivé en fin de vie ne recevant plus de correctifs de sécurité.

---
[Source](https://thehackernews.com/2026/11/france-blames-iran-for-sabotage-attack.html){:target="_blank"}
