---
title: 'Microsoft Legal Action Disrupts RedVDS Cybercrime Infrastructure Used for Online Fraud'
date: 2026-01-15
permalink: /posts/2026/01/15/microsoft-legal-action-disrupts-redvds-cybercrime-infrastructure-used-for-online-fraud/
tags:
- veille-cyber
- hackernews
---
## Perturbation d'une Infrastructure de Cybercriminalité par Microsoft

Microsoft a mené une action juridique coordonnée aux États-Unis et au Royaume-Uni pour démanteler RedVDS, un service d'abonnement utilisé par les cybercriminels pour faciliter la fraude en ligne. Le service proposait des machines virtuelles à bas coût, permettant aux criminels de mener des activités frauduleuses à grande échelle et de manière anonyme.

**Points Clés :**

*   **Service RedVDS :** Proposait des machines virtuelles (ordinateurs virtuels jetables) sous licence Windows non autorisée pour un abonnement mensuel aussi bas que 24 USD. Ces machines permettaient aux criminels de mener diverses activités frauduleuses de manière difficilement traçable.
*   **Impact Financier :** L'activité facilitée par RedVDS a entraîné environ 40 millions USD de pertes frauduleuses déclarées aux États-Unis depuis mars 2025. Plus de 191 000 organisations ont été compromises ou ont subi un accès frauduleux depuis septembre 2025.
*   **Modèle Économique :** RedVDS s'inscrit dans le modèle "Crimeware-as-a-Service" (CaaS), rendant la cybercriminalité accessible même aux acteurs peu expérimentés.
*   **Fonctionnalités :** Le service permettait de louer des serveurs RDP Windows avec contrôle administrateur illimité, offrant un accès via une interface conviviale et un bot Telegram. Il ne conservait pas de journaux d'activité.
*   **Technologie et Exploitation :** Les machines virtuelles étaient générées à partir d'une seule image Windows Server 2022 clonée, utilisant une licence volée pour réduire les coûts. Cette approche permettait de déployer rapidement de nouveaux hôtes RDP.
*   **Utilisation d'IA :** RedVDS était combiné avec des outils d'IA générative pour identifier des cibles, créer des e-mails réalistes et même utiliser des techniques comme le deepfake et le clonage vocal pour des escroqueries par usurpation d'identité.
*   **Secteurs Visés :** Divers secteurs ont été ciblés, notamment juridique, construction, fabrication, immobilier, santé et éducation, dans plusieurs pays.
*   **Outils Associés :** L'infrastructure était utilisée pour héberger des outils de spam/phishing, des extracteurs d'adresses e-mail, des outils de confidentialité (VPN) et des outils d'accès à distance.

**Vulnérabilités et Exploitation :**

Bien que l'article ne mentionne pas de CVE spécifiques, la vulnérabilité réside dans la mise à disposition facile d'une infrastructure clé en main permettant :

*   **Envoyer des e-mails de phishing à haut volume.**
*   **Héberger des infrastructures d'arnaque.**
*   **Mener des escroqueries par compromission de la messagerie professionnelle (BEC).**
*   **Réaliser des prises de contrôle de comptes.**
*   **Faciliter la fraude financière.**
*   **Utiliser des outils de manipulation d'identité (deepfakes, clonage vocal).**
*   **Exploiter des licences Windows non autorisées pour réduire les coûts.**

**Recommandations :**

L'action de Microsoft vise à perturber l'infrastructure. Pour les utilisateurs et les organisations, les recommandations implicites sont :

*   **Prudence face aux e-mails et communications suspectes :** Vérifier l'authenticité des expéditeurs, surtout en cas de demandes financières inhabituelles ou d'informations sensibles.
*   **Sécurisation des comptes :** Utiliser l'authentification multifacteur (MFA) et renforcer les politiques de mots de passe.
*   **Vigilance face aux tentatives d'ingénierie sociale :** Être conscient des techniques d'usurpation d'identité, notamment celles amplifiées par l'IA.
*   **Maintenir les logiciels à jour :** Bien que RedVDS proposait des logiciels non licenciés, il est crucial pour les organisations d'utiliser des logiciels légitimes et patchés pour éviter les vulnérabilités connues.
*   **Formation à la cybersécurité :** Éduquer les employés sur les menaces actuelles, y compris les risques liés au phishing et aux escroqueries BEC.

---
[Source](https://thehackernews.com/2026/01/microsoft-legal-action-disrupts-redvds.html){:target="_blank"}
