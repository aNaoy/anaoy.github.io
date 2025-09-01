---
title: '⚡ Weekly Recap: WhatsApp 0-Day, Docker Bug, Salesforce Breach, Fake CAPTCHAs, Spyware App & More'
date: 2025-09-01
permalink: /posts/2025/09/01/weekly-recap-whatsapp-0-day-docker-bug-salesforce-breach-fake-captchas-spyware-app-more/
tags:
- veille-cyber
- hackernews
---
### Synthèse des Actualités de la Cybersécurité

Les menaces actuelles en cybersécurité résultent souvent d'une combinaison de faiblesses exploitées, plutôt que d'une seule faille majeure. Les attaquants mêlent accès compromis, logiciels non patchés et techniques d'ingénierie sociale pour maximiser leur impact.

**Points Clés et Vulnérabilités :**

*   **WhatsApp (CVE-2025-55177)** : Une vulnérabilité d'autorisation insuffisante dans la synchronisation des messages de périphériques liés a été exploitée. Elle a potentiellement été utilisée en conjonction avec une faille Apple pour des attaques ciblées de logiciels espions. Moins de 200 utilisateurs pourraient avoir été affectés.
*   **Docker Desktop (CVE-2025-9074)** : Une vulnérabilité critique expose l'API du moteur Docker sur Windows et macOS, permettant à un attaquant dans un conteneur de briser l'isolement et potentiellement de prendre le contrôle du système hôte. L'exploitation du montage du système de fichiers est effective sur Windows.
*   **MixShell** : Des cybercriminels ciblent des fabricants et entreprises de chaînes d'approvisionnement aux États-Unis via des formulaires de contact sur leurs sites web pour contourner les filtres d'e-mails et déployer des malwares.
*   **Salesloft / Salesforce** : Le groupe UNC6395 a compromis des jetons OAuth liés à l'application tierce Salesloft Drift pour voler des données de Salesforce, notamment des clés d'accès AWS et des jetons Snowflake.
*   **Storm-0501** : Ce groupe exploite des comptes à privilèges compromis et des failles de visibilité dans les environnements cloud pour chiffrer des données, les exfiltrer et supprimer des ressources, y compris des sauvegardes, puis extorquer les victimes.
*   **UNC6384 / Mustang Panda** : Des acteurs soutenus par l'État chinois détournent les vérifications de portail captif pour distribuer des malwares déguisés en logiciels Adobe, ciblant notamment des diplomates en Asie du Sud-Est.
*   **ShadowCaptcha** : Une campagne financière exploite de fausses pages CAPTCHA de Google et Cloudflare sur des sites WordPress compromis pour distribuer des voleurs d'informations et des rançongiciels.
*   **Microsoft RDP** : Les services RDP font l'objet d'un grand nombre de scans malveillants visant à identifier des failles de synchronisation pour des intrusions basées sur des identifiants.
*   **TheTruthSpy** : Une faille dans le processus de récupération de mot de passe permettrait à des acteurs malveillants de prendre le contrôle de comptes et d'accéder aux données des victimes. Le développeur a déclaré avoir perdu le code source.
*   **Max (application russe)** : Cette alternative à WhatsApp surveille et enregistre en permanence l'activité des utilisateurs, sans chiffrement, et suit la localisation avec précision. Elle est devenue obligatoire pour les appareils vendus en Russie.
*   **OpenSSH** : La version 10.1 affichera des avertissements lors de la connexion à des serveurs SSH ne supportant pas la cryptographie post-quantique.
*   **ScreenConnect** : Des campagnes de phishing ciblent les administrateurs ScreenConnect via de fausses alertes d'activité suspecte ou des invitations Zoom/Teams pour voler des identifiants, et utilisent le framework Evilginx pour capturer des données. D'autres campagnes utilisent des lures liés à l'IA pour distribuer le malware XWorm.
*   **Cisco Secure Links** : Les attaquants compromettent des comptes au sein d'organisations utilisant Cisco pour réécrire des liens malveillants via le service "Secure Links" afin de contourner les filtres.
*   **TRM Labs** : Des escrocs imitent TRM Labs et des agences gouvernementales pour proposer de fausses récupérations de fonds, profitant de la vulnérabilité des victimes.
*   **Nouvelles Souches de Ransomware** : Les groupes Cephalus, Underground, NightSpire et Sinobi (rebrand de Lynx) sont actifs, utilisant des comptes RDP compromis ou des identifiants VPN SonicWall pour un accès initial.
*   **Groupes de Ransomware Actifs** : Akira, Cl0p, Qilin, Safepay et RansomHub sont les plus actifs au premier semestre 2025, avec une augmentation de 179% des attaques par rapport à l'année précédente. L'extorsion prime sur le chiffrement, et l'usage d'IA est croissant.
*   **Microsoft** : Limite le nombre de destinataires externes à 100 par organisation par jour, à partir d'octobre 2025, pour lutter contre le spam.
*   **SleepWalk** : Une nouvelle attaque par canal secondaire physique exploite la consommation d'énergie des commutations de contexte des CPU pour fuiter des données sensibles.
*   **IA et Injection de Prompts** : Les IA sont vulnérables aux attaques de prompt injection via des images dont les instructions malveillantes sont cachées lors de la réduction de leur taille. L'outil Anamorpher a été publié pour générer de telles images.
*   **Réseaux Sociaux et Médias d'État Chinois** : Un réseau de domaines et de comptes sociaux diffuse des articles en anglais traduits et résumés d'organes de presse d'État chinois, principalement du contenu pro-Chine et anti-Occident.
*   **Applications VPN** : Des applications VPN sur Google Play présentent des faiblesses de sécurité, exposant les données des utilisateurs à des risques de déchiffrement. Huit d'entre elles, développées par des entreprises liées à Qihoo 360, partagent du code et des méthodes de chiffrement obsolètes.
*   **Écosystème eSIM** : De nombreux fournisseurs d'eSIM routent les données des utilisateurs via des réseaux étrangers, y compris chinois, indépendamment de la localisation de l'utilisateur, posant des risques de surveillance. Le modèle de provisionnement numérique ouvre également la porte au phishing et à l'usurpation d'identité via de faux profils eSIM.
*   **ComfyUI et Pickai** : Des vulnérabilités dans la plateforme IA ComfyUI ont été exploitées pour distribuer le backdoor Pickai, visant près de 700 serveurs dans le monde.
*   **LSQUIC QUIC (CVE-2025-54939)** : Une vulnérabilité QUIC-LEAK permet d'épuiser la mémoire des serveurs QUIC avant même l'établissement d'une connexion, causant des dénis de service. Des correctifs sont disponibles.
*   **Sites de Téléchargement YouTube Falsifiés** : Ces sites distribuent des programmes proxyware comme Infatica, utilisant les ressources système à des fins lucratives.
*   **Jugement Fédéral Américain** : Un sénateur a critiqué la négligence du système judiciaire fédéral suite à une cyberattaque qui a exposé des documents judiciaires confidentiels, exploitant des vulnérabilités connues depuis 2020. La Russie est soupçonnée d'implication.
*   **Blocage de Cryptomonnaies** : Des entreprises de blockchain et les autorités ont gelé près de 50 millions de dollars volés lors d'arnaques sentimentales ("romance baiting").
*   **Corée du Sud - Extradition** : Un ressortissant chinois suspecté d'orchestrer des cyberattaques sophistiquées a été extradé pour avoir volé l'équivalent de 38 milliards de won.
*   **IA et Test de Sécurité** : OpenAI et Anthropic échangent des évaluations de sécurité de leurs systèmes d'IA pour lutter contre les risques comme l'injection de prompts. Une cyberattaque a utilisé un outil IA d'Anthropic pour automatiser un vol de données et une campagne d'extorsion.
*   **Plex Media Server (CVE-2025-34158)** : Une vulnérabilité de transfert de ressources incorrectes a été corrigée dans les versions récentes. Des centaines de milliers de serveurs Plex exposent leur interface web.
*   **Sites de Recettes et Guides Falsifiés** : Ces sites diffusent des malwares, y compris l'adware JustAskJacky, via des campagnes de publicité malveillante.

**Recommandations Clés :**

*   **Mise à jour immédiate** : Appliquer les correctifs pour WhatsApp (CVE-2025-55177), Docker Desktop (CVE-2025-9074), et d'autres vulnérabilités mentionnées.
*   **Sécurisation des intégrations IA** : Utiliser des outils comme MCPSafetyScanner, MCP Guardian, MCPSecBench, Open Policy Agent ou Kyverno pour auditer, sécuriser et tester les serveurs MCP. Adopter une approche Zero Trust avec OAuth 2.1 et mTLS.
*   **Prudence avec les services tiers** : Soyez vigilant quant aux applications tierces utilisées avec des plateformes comme Salesforce.
*   **Renforcement de la sécurité des conteneurs** : Comprendre et mitiger les risques liés à l'exposition des API de conteneurs.
*   **Sensibilisation à l'ingénierie sociale** : Éduquer les utilisateurs sur les techniques d'hameçonnage, y compris celles utilisant des formulaires de contact ou de fausses alertes.
*   **Gestion des identités et des accès** : Mettre en place une authentification forte et des contrôles d'accès stricts, notamment pour les super administrateurs.
*   **Protection des données sensibles** : Mettre en œuvre des mesures pour prévenir l'exfiltration de données, le chiffrement et la suppression de sauvegardes.
*   **Surveillance et journalisation** : Maintenir une visibilité sur les activités réseau et système pour détecter les comportements suspects.
*   **Vérification des sources** : Se méfier des communications non sollicitées et des sites web suspects, en particulier ceux qui proposent des téléchargements ou des solutions de récupération de fonds.
*   **Utilisation de domaines personnalisés** : Adopter des domaines personnalisés pour l'envoi d'e-mails afin d'éviter la dégradation de la réputation des domaines partagés.

---
[Source](https://thehackernews.com/2025/09/weekly-recap-whatsapp-0-day-docker-bug.html){:target="_blank"}
