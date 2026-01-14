---
title: 'Reprompt attack hijacked Microsoft Copilot sessions for data theft'
date: 2026-01-14
permalink: /posts/2026/01/14/reprompt-attack-hijacked-microsoft-copilot-sessions-for-data-theft/
tags:
- veille-cyber
- bleepingcomp
---
### Risque de vol de données via l'attaque "Reprompt" sur Microsoft Copilot

Une nouvelle méthode d'attaque, nommée "Reprompt", a été découverte, permettant aux cybercriminels de prendre le contrôle de sessions Microsoft Copilot pour dérober des informations sensibles. Cette attaque exploite une vulnérabilité dans la manière dont Copilot traite les requêtes contenues dans les URL.

**Fonctionnement de l'attaque :**

L'attaque Reprompt repose sur trois techniques combinées :

*   **Injection de "Prompt via Paramètre" (P2P) :** Les attaquants insèrent des commandes malveillantes dans le paramètre 'q' d'une URL Copilot légitime. Lorsque l'utilisateur clique sur ce lien, Copilot exécute automatiquement ces commandes, ignorant potentiellement les protections initiales.
*   **Technique du double-requête :** Les mesures de sécurité de Copilot, qui visent à prévenir les fuites de données, ne s'appliquent qu'à la première requête. Les attaquants ordonnent à Copilot d'exécuter une action deux fois. La seconde tentative, non filtrée, permet d'exfiltrer des données qui auraient été bloquées lors de la première.
*   **Technique de la chaîne-requête :** Après l'exécution initiale, Copilot peut continuer à recevoir des instructions dynamiques d'un serveur contrôlé par l'attaquant. Chaque réponse génère la requête suivante, permettant ainsi une exfiltration continue et discrète de données.

Le processus implique généralement un email de phishing présentant un lien Copilot. Une fois le lien activé, l'attaquant maintient une communication avec la session Copilot de la victime, même si l'onglet est fermé, car la session authentifiée reste active. Cette méthode ne nécessite pas de plugins et opère de manière invisible pour l'utilisateur.

**Vulnérabilités :**

L'article ne mentionne pas de CVE spécifiques pour cette attaque, mais souligne que la faille réside dans la gestion des requêtes et des protections contre les fuites de données dans Copilot Personal. Microsoft 365 Copilot, destiné aux entreprises, est considéré comme mieux protégé grâce à des contrôles de sécurité supplémentaires.

**Recommandations :**

Bien que l'exploitation de cette méthode n'ait pas été détectée dans la nature et que Microsoft ait corrigé le problème lors des mises à jour de janvier 2026, il est fortement recommandé d'appliquer les dernières mises à jour de sécurité Windows dès que possible.

---
[Source](https://www.bleepingcomputer.com/news/security/reprompt-attack-let-hackers-hijack-microsoft-copilot-sessions/){:target="_blank"}
