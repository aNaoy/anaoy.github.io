---
title: 'Konni Hackers Deploy AI-Generated PowerShell Backdoor Against Blockchain Developers'
date: 2026-01-26
permalink: /posts/2026/01/26/konni-hackers-deploy-ai-generated-powershell-backdoor-against-blockchain-developers/
tags:
- veille-cyber
- hackernews
---
### Le groupe Konni exploite l'IA pour cibler les développeurs blockchain

Le groupe de pirates informatiques nord-coréen Konni a étendu sa portée géographique et ses tactiques, ciblant désormais des développeurs et des équipes d'ingénierie dans le secteur de la blockchain. Les attaques, qui ont touché le Japon, l'Australie et l'Inde, impliquent des e-mails d'hameçonnage sophistiqués utilisant des liens publicitaires déguisés pour distribuer un cheval de Troie d'accès à distance nommé EndRAT.

Une particularité de ces attaques est l'utilisation potentielle d'outils d'intelligence artificielle pour générer des malwares PowerShell. Cette méthode permettrait d'accélérer le développement et de standardiser le code, tout en conservant des méthodes de distribution éprouvées basées sur l'ingénierie sociale. Les malwares sont conçus pour échapper aux analyses, établir une persistance via des tâches planifiées et contourner le contrôle de compte utilisateur (UAC). L'objectif semble être d'obtenir un accès aux environnements de développement pour une compromission plus large des projets et services.

**Points clés :**

*   **Acteur malveillant :** Groupe Konni (également connu sous les noms d'Earth Imp, Opal Sleet, Osmium, TA406, Vedalia).
*   **Cible :** Développeurs et équipes d'ingénierie du secteur de la blockchain.
*   **Zone géographique étendue :** Japon, Australie, Inde (en plus des cibles antérieures comme la Corée du Sud, la Russie et l'Ukraine).
*   **Nouvelle tactique :** Utilisation potentielle d'outils d'IA pour générer des malwares PowerShell.
*   **Méthode de livraison :** Campagnes d'hameçonnage ciblant des liens publicitaires (Google, Naver) et distribution de fichiers ZIP via des sites WordPress ou Discord CDN.
*   **Malware principal :** EndRAT (un cheval de Troie d'accès à distance).
*   **Objectif :** Établir une présence dans les environnements de développement pour un accès étendu.

**Vulnérabilités exploitées :**

*   Mécanismes de redirection d'URL légitimes pour les publicités (par exemple, `ad.doubleclick[.]net`) détournés pour héberger des fichiers malveillants.
*   Technique de contournement UAC : FodHelper.
*   Exploitation de la confiance des utilisateurs via des emails déguisés en notifications financières ou en demandes de transfert.

**Recommandations :**

*   Sensibiliser les développeurs aux techniques d'hameçonnage, y compris celles qui imitent des liens publicitaires ou des documents.
*   Vérifier attentivement les liens et les expéditeurs d'e-mails, en particulier ceux contenant des pièces jointes inattendues ou provenant de sources non vérifiées.
*   Maintenir les systèmes à jour avec les derniers correctifs de sécurité.
*   Mettre en place et vérifier les configurations de sécurité des e-mails pour bloquer les e-mails d'hameçonnage.
*   Utiliser des solutions de sécurité endpoint robustes pour détecter et bloquer les malwares.
*   Faire preuve de vigilance face aux invitations à télécharger des fichiers, même s'ils proviennent de plateformes légitimes comme Discord.

---
[Source](https://thehackernews.com/2026/01/konni-hackers-deploy-ai-generated.html){:target="_blank"}
