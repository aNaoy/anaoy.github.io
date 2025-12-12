---
title: 'New Advanced Phishing Kits Use AI and MFA Bypass Tactics to Steal Credentials at Scale'
date: 2025-12-12
permalink: /posts/2025/12/12/new-advanced-phishing-kits-use-ai-and-mfa-bypass-tactics-to-steal-credentials-at-scale/
tags:
- veille-cyber
- hackernews
---
**Les Kits de Phishing Évolués : IA et Contournement de la MFA pour le Vol d'Identifiants à Grande Échelle**

Des chercheurs en cybersécurité ont identifié quatre nouveaux kits de phishing, BlackForce, GhostFrame, InboxPrime AI et Spiderman, conçus pour voler des identifiants à grande échelle. Ces outils exploitent des techniques avancées, notamment l'intelligence artificielle (IA) et le contournement de l'authentification multifacteur (MFA).

**Points Clés :**

*   **Automatisation et IA :** InboxPrime AI se distingue par son utilisation de l'IA pour automatiser les campagnes d'envoi d'emails de masse, imitant le comportement humain et exploitant l'interface Gmail pour échapper aux filtres. Il propose une licence perpétuelle et l'accès au code source.
*   **Contournement de la MFA :** BlackForce et Spiderman sont capables de contourner la MFA. BlackForce utilise des attaques "Man-in-the-Browser" (MitB) pour capturer les codes OTP et les présenter sous forme de fausses pages d'authentification MFA. Spiderman peut également intercepter des codes OTP et des codes PhotoTAN.
*   **Techniques d'Évasion :** Ces kits emploient diverses méthodes pour échapper à la détection, comme des listes noires filtrant les outils de sécurité, le "cache busting" pour forcer le téléchargement de scripts malveillants, et des iframes dissimulant le contenu malveillant. GhostFrame utilise des iframes pour masquer son comportement malveillant et changer facilement de contenu de phishing.
*   **Ciblage Spécifique :** Spiderman se spécialise dans la création de répliques de sites bancaires européens et de portails gouvernementaux, ciblant principalement l'Allemagne, l'Autriche, la Suisse et la Belgique. Il peut également voler des phrases clés de portefeuille de cryptomonnaies et des données de carte de crédit.
*   **Industrialisation du Phishing :** L'émergence de ces kits, souvent vendus comme services (MaaS), abaisse le seuil d'entrée pour les cybercriminels, permettant le lancement de campagnes plus volumineuses, mieux ciblées et professionnelles sans expertise technique poussée.
*   **Kits Hybrides :** Des combinaisons de kits, comme un hybride Salty-Tycoon, sont observées, rendant l'attribution plus complexe et affaiblissant les règles de détection spécifiques à chaque kit.

**Vulnérabilités exploitées (sans CVE spécifiques mentionnées dans l'article) :**

*   **Vulnérabilités liées au contournement de l'authentification multifacteur (MFA) :** Les techniques MitB et la présentation de fausses pages MFA permettent de voler les codes d'authentification à usage unique.
*   **Vulnérabilités dans la gestion des sessions et des données sensibles :** La capacité à capturer des identifiants, des codes OTP, des codes PhotoTAN, des phrases clés de portefeuille de cryptomonnaies et des données de carte de crédit.
*   **Vulnérabilités dans les mécanismes de livraison de contenu web :** L'utilisation d'iframes et de scripts pour masquer le contenu malveillant et rediriger les victimes.
*   **Vulnérabilités dans les systèmes de filtrage d'email :** L'utilisation de l'IA et l'imitation du comportement d'envoi légitime visent à contourner les filtres anti-spam traditionnels.

**Recommandations :**

*   **Vigilance accrue face aux emails et liens suspects :** Les utilisateurs doivent être particulièrement prudents avec les emails, surtout ceux demandant des informations personnelles, des identifiants ou des codes d'authentification.
*   **Utilisation d'outils de sécurité robustes :** Maintenir à jour les logiciels antivirus, les pare-feu et les solutions de détection d'intrusion.
*   **Authentification multifacteur (MFA) :** Bien que ciblée par certains kits, la MFA reste une couche de sécurité essentielle. Il est recommandé d'utiliser des méthodes d'authentification plus résilientes lorsque disponibles.
*   **Formation et sensibilisation à la cybersécurité :** Eduquer les employés et les particuliers sur les tactiques de phishing actuelles.
*   **Surveillance des journaux et des alertes de sécurité :** Pour les organisations, une surveillance attentive des journaux d'accès et des alertes peut aider à détecter des activités suspectes.
*   **Mise à jour régulière des logiciels :** S'assurer que tous les logiciels, navigateurs inclus, sont à jour pour bénéficier des derniers correctifs de sécurité.

---
[Source](https://thehackernews.com/2025/12/new-advanced-phishing-kits-use-ai-and.html){:target="_blank"}
