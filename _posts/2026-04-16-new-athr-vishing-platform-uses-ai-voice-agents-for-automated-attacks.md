---
title: 'New ATHR vishing platform uses AI voice agents for automated attacks'
date: 2026-04-16
permalink: /posts/2026/04/16/new-athr-vishing-platform-uses-ai-voice-agents-for-automated-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### ATHR : Une nouvelle plateforme de vishing automatisée par IA

La plateforme cybercriminelle ATHR industrialise les attaques de type « TOAD » (*Telephone-Oriented Attack Delivery*). Commercialisée sur des forums clandestins, elle permet à des attaquants, même peu techniciens, de mener des campagnes de hameçonnage vocal (vishing) entièrement automatisées grâce à des agents conversationnels basés sur l'IA.

**Points clés :**
*   **Automatisation complète :** La plateforme gère l'intégralité de la chaîne d'attaque, de l'envoi d'emails frauduleux personnalisés à la récolte de données via des appels vocaux automatisés.
*   **Ingénierie sociale par IA :** Les agents vocaux simulent des procédures de support légitimes pour inciter les victimes à divulguer des codes de vérification à usage unique (MFA).
*   **Cibles :** Le service vise les accès à des comptes sensibles, notamment Google, Microsoft, Coinbase, Binance et Yahoo.
*   **Modèle économique :** Disponible pour 4 000 $ avec une commission de 10 % sur les profits réalisés.

**Vulnérabilités :**
*   Aucune CVE spécifique n'est associée, car il s'agit d'une plateforme d'ingénierie sociale exploitant le facteur humain plutôt que des failles logicielles. L'attaque repose sur la capacité des emails à contourner les filtres d'authentification technique (SPF, DKIM, DMARC) en imitant des alertes de sécurité légitimes.

**Recommandations :**
*   **Détection comportementale :** Mettre en œuvre des solutions capables d'analyser les modèles de communication au sein de l'organisation pour détecter des anomalies plutôt que de se fier uniquement au contenu des emails.
*   **Surveillance contextuelle :** Surveiller l'apparition soudaine de plusieurs emails suspects contenant des numéros de téléphone similaires ciblant différents employés.
*   **Sensibilisation :** Former les utilisateurs à la méfiance vis-à-vis des notifications urgentes incitant à appeler un numéro, et rappeler qu'aucun service légitime ne demande un code de vérification par téléphone lors d'une procédure de récupération de compte.

---
[Source](https://www.bleepingcomputer.com/news/security/new-athr-vishing-platform-uses-ai-voice-agents-for-automated-attacks/){:target="_blank"}
