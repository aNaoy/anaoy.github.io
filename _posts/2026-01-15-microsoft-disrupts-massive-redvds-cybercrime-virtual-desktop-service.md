---
title: 'Microsoft disrupts massive RedVDS cybercrime virtual desktop service'
date: 2026-01-15
permalink: /posts/2026/01/15/microsoft-disrupts-massive-redvds-cybercrime-virtual-desktop-service/
tags:
- veille-cyber
- bleepingcomp
---
**Interruption d'une Infrastructure Massive de Cybercriminalité : RedVDS**

Microsoft, en collaboration avec Europol et les autorités allemandes, a démantelé RedVDS, une plateforme de cybercriminalité proposant des services de bureau virtuel accessibles aux criminels. Cette opération a conduit à la saisie d'infrastructures malveillantes et à la mise hors ligne du marché et du portail client de RedVDS. L'action en justice a vu la participation de deux victimes, une entreprise pharmaceutique ayant subi une perte de 7,3 millions de dollars et une association de copropriétaires ayant perdu près de 500 000 dollars.

Depuis 2019, RedVDS offrait des accès à des serveurs cloud virtuels Windows sans limite d'usage, pour des tarifs commençant à 24 dollars par mois. Cette facilité d'accès à des ordinateurs virtuels jetables rendait les fraudes peu coûteuses, évolutives et difficiles à tracer. La plateforme a servi de base à de nombreux groupes criminels, notamment ceux identifiés sous les noms de Storm-0259, Storm-2227, Storm-1575 et Storm-1747. L'opérateur de RedVDS, suivi comme Storm-2470, utilisait une image clonée de Windows Server 2022 pour créer toutes les machines virtuelles, laissant une signature technique distinctive (nom d'ordinateur WIN-BUNS25TD77J) qui a aidé les enquêteurs.

Les serveurs loués par RedVDS auprès de fournisseurs d'hébergement à travers le monde permettaient aux criminels de cibler des victimes géographiquement proches et d'éviter les filtres de sécurité basés sur la localisation. Les clients de RedVDS utilisaient ces serveurs pour déployer divers outils malveillants, y compris des utilitaires d'envoi de masse de courriels, des outils de récolte d'adresses e-mail, des outils de confidentialité et des logiciels d'accès à distance.

La plateforme a facilité l'envoi de courriels de phishing de masse, l'hébergement d'infrastructures d'arnaque et la mise en œuvre de schémas frauduleux, tout en garantissant l'anonymat grâce aux paiements en cryptomonnaies. Les serveurs RedVDS ont également été utilisés pour le vol d'identifiants, les prises de contrôle de comptes, les escroqueries par compromission de messagerie professionnelle (BEC) et les escroqueries de détournement de paiements immobiliers, ayant causé des pertes importantes à plus de 9 000 clients au Canada et en Australie.

Microsoft a également constaté que de nombreux clients de RedVDS exploitaient des outils d'intelligence artificielle, tels que ChatGPT, pour générer des courriels de phishing plus convaincants. D'autres utilisaient des technologies de manipulation d'image et de voix pour usurper l'identité d'organisations et de personnes de confiance.

En un mois, des cybercriminels contrôlant plus de 2 600 machines virtuelles RedVDS ont envoyé en moyenne 1 million de messages de phishing par jour aux clients de Microsoft, compromettant près de 200 000 comptes au cours des quatre derniers mois. Depuis septembre 2025, les attaques facilitées par RedVDS ont entraîné la compromission ou l'accès frauduleux de plus de 191 000 organisations dans le monde.

**Points Clés :**

*   Démantèlement de RedVDS, une plateforme massive de cybercriminalité.
*   Service de bureau virtuel (VDS) utilisé pour faciliter les fraudes.
*   Pertes financières importantes signalées, estimées à 40 millions de dollars rien qu'aux États-Unis.
*   Utilisation d'IA et de technologies de manipulation pour des attaques plus sophistiquées.
*   Impact sur des centaines de milliers d'organisations et de comptes.

**Vulnérabilités exploitées :**

Bien qu'aucun CVE spécifique ne soit mentionné pour la plateforme RedVDS elle-même, l'article met en évidence l'exploitation de vulnérabilités logistiques et humaines :

*   **Accessibilité et Scalabilité :** La simplicité et le faible coût des services VDS ont permis aux criminels de lancer des attaques à grande échelle.
*   **Anonymat :** Les paiements en cryptomonnaies et la nature distribuée de l'infrastructure ont rendu le traçage difficile.
*   **Utilisation d'Outils d'IA :** La génération de contenu de phishing plus convaincant via ChatGPT et d'autres outils.
*   **Usurpation d'Identité :** Utilisation de deepfakes (face-swapping, manipulation vidéo et vocale) pour tromper les victimes.
*   **Manque de Vigilance :** Les attaques BEC et les détournements de fonds exploitent souvent des failles dans les processus de vérification des transactions.

**Recommandations :**

*   **Renforcer les processus de vérification :** Mettre en place des procédures strictes pour la validation des transactions financières, notamment les virements importants.
*   **Sensibilisation et formation :** Éduquer les employés sur les risques du phishing, les escroqueries par ingénierie sociale et l'importance de vérifier les demandes inhabituelles.
*   **Adoption de solutions de sécurité avancées :** Utiliser des filtres anti-spam et anti-phishing robustes, des solutions de détection et de réponse sur les points d'extrémité (EDR), et des systèmes de gestion des informations et des événements de sécurité (SIEM).
*   **Authentification multifacteur (MFA) :** Mettre en œuvre l'authentification multifacteur sur tous les comptes, en particulier pour l'accès aux messageries professionnelles et aux systèmes financiers.
*   **Surveillance proactive :** Mettre en place une surveillance continue des réseaux et des systèmes pour détecter les activités suspectes et les anomalies.
*   **Collaboration et partage d'informations :** Soutenir et participer aux efforts de lutte contre la cybercriminalité par le biais du partage d'informations avec les forces de l'ordre et les partenaires de cybersécurité.

---
[Source](https://www.bleepingcomputer.com/news/security/microsoft-seizes-servers-disrupts-massive-redvds-cybercrime-platform/){:target="_blank"}
