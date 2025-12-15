---
title: 'Phantom Stealer Spread by ISO Phishing Emails Hitting Russian Finance Sector'
date: 2025-12-15
permalink: /posts/2025/12/15/phantom-stealer-spread-by-iso-phishing-emails-hitting-russian-finance-sector/
tags:
- veille-cyber
- hackernews
---
**Campagnes de Phishing Ciblant le Secteur Financier Russe**

Une campagne de phishing active exploite des emails frauduleux se faisant passer pour des confirmations de paiement afin de diffuser le logiciel malveillant Phantom Stealer. Ce dernier est distribué via des fichiers ISO contenant des DLL malveillantes qui, une fois exécutées, déploient le chargeur. Phantom Stealer est capable de voler des informations sensibles comme les identifiants de portefeuilles de cryptomonnaies, les mots de passe de navigateurs, les cookies, les détails de cartes bancaires, et d'enregistrer les frappes au clavier. Il communique les données volées via Telegram ou des webhooks Discord. Des campagnes similaires visent également d'autres secteurs en Russie, utilisant divers malwares comme DUPERUNNER (associé à AdaptixC2), Cobalt Strike, Formbook et DarkWatchman. Certaines de ces attaques sont attribuées à des groupes hacktivistes liés au conflit en Ukraine, et exploitent des méthodes avancées comme le système de fichiers interplanétaire (IPFS) pour rediriger vers des pages de phishing.

**Points Clés :**

*   **Ciblage Principal :** Secteur financier et comptable en Russie.
*   **Méthode de Diffusion :** Emails de phishing contenant des archives ZIP, qui déploient des fichiers ISO.
*   **Malware Principal :** Phantom Stealer, un voleur d'informations sophistiqué.
*   **Autres Malwares Identifiés :** DUPERUNNER, AdaptixC2, Cobalt Strike, Formbook, DarkWatchman.
*   **Techniques d'Évasion :** Détection d'environnements virtuels et de sandboxes.
*   **Exfiltration des Données :** Telegram, Discord, serveurs FTP, et pages de connexion sur IPFS/Vercel.
*   **Attribution Potentielle :** Groupes hacktivistes alignés sur les intérêts ukrainiens.

**Vulnérabilités :**

*   Bien que l'article ne détaille pas de vulnérabilités logicielles spécifiques avec des identifiants CVE, le succès de ces attaques repose sur l'ingénierie sociale et la capacité à exécuter des fichiers depuis des images disque montées. La mise en œuvre de mesures de sécurité contre l'exécution de fichiers non fiables et la vigilance des utilisateurs sont primordiales.

**Recommandations :**

*   **Vigilance Accrue :** Les utilisateurs doivent se méfier des emails inattendus, en particulier ceux liés à des transactions financières ou nécessitant des confirmations.
*   **Analyse des Pièces Jointes :** Éviter d'ouvrir les pièces jointes suspectes, en particulier les archives et les fichiers ISO.
*   **Mises à Jour de Sécurité :** Maintenir les systèmes d'exploitation et les logiciels antivirus à jour.
*   **Sensibilisation à la Cybersécurité :** Former les employés aux tactiques courantes de phishing et aux bonnes pratiques de sécurité.
*   **Filtrage des Emails :** Utiliser des solutions de filtrage d'emails robustes pour bloquer les messages suspects avant qu'ils n'atteignent les utilisateurs.
*   **Surveillance des Activités Réseau :** Mettre en place une surveillance pour détecter les communications anormales vers des serveurs externes suspects.

---
[Source](https://thehackernews.com/2025/12/phantom-stealer-spread-by-iso-phishing.html){:target="_blank"}
