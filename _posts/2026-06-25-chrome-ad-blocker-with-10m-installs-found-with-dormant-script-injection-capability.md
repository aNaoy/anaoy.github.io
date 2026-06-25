---
title: 'Chrome Ad Blocker with 10M+ Installs Found with Dormant Script Injection Capability'
date: 2026-06-25
permalink: /posts/2026/06/25/chrome-ad-blocker-with-10m-installs-found-with-dormant-script-injection-capability/
tags:
- veille-cyber
- hackernews
---
### Risque de sécurité majeur dans l'extension « Adblock for YouTube »

L'extension Chrome « Adblock for YouTube », utilisée par plus de 10 millions d'internautes, a été identifiée comme possédant une capacité dormante d'exécution de code JavaScript arbitraire. Bien qu'aucune activité malveillante active n'ait été confirmée, l'architecture permet aux développeurs de détourner l'extension pour voler des données, accéder à des sessions privées ou usurper l'identité de l'utilisateur sur n'importe quel site web, le tout via une simple mise à jour de configuration serveur invisible.

**Points clés :**
*   **Capacité d'injection :** L'extension contient une fonctionnalité nommée `trusted-create-element` permettant l'injection de scripts à distance sans nécessiter de mise à jour sur le Chrome Web Store.
*   **Permissions excessives :** L'extension demande des accès étendus pour lire et modifier le contenu de toutes les pages visitées.
*   **Contournement de sécurité :** Le mécanisme censé restreindre l'action de l'extension au seul domaine « youtube.com » est défaillant : il suffit que la chaîne « youtube.com » apparaisse n'importe où dans l'URL (par exemple dans un paramètre de requête) pour que l'extension s'active sur des sites tiers, y compris bancaires ou professionnels.
*   **Historique suspect :** L'extension a déjà été liée à d'autres modules publicitaires malveillants par le passé et présente des similitudes avec des extensions récemment supprimées par Google.

**Vulnérabilités :**
*   **Pas de CVE attribuée :** Il s'agit d'un problème de conception malveillante (backdoor logicielle) plutôt que d'une faille logicielle classique.
*   **Vecteur :** Injection de scripts via configuration serveur distante.

**Recommandations :**
*   **Désinstallation immédiate :** Supprimez l'extension « Adblock for YouTube » (ID: `cmedhionkhpnakcndndgjdbohmhepckk`) de votre navigateur Chrome.
*   **Audit des extensions :** Examinez régulièrement la liste de vos extensions installées et supprimez celles dont l'utilité est marginale ou dont le développeur n'est pas reconnu.
*   **Principe de moindre privilège :** Soyez vigilant quant aux autorisations accordées aux extensions (« Lire et modifier toutes les données sur les sites Web que vous consultez »). Privilégiez des outils open-source audités comme *uBlock Origin*.

---
[Source](https://thehackernews.com/2026/06/chrome-ad-blocker-with-10m-installs.html){:target="_blank"}
