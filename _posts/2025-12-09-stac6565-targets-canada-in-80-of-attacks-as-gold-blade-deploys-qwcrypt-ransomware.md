---
title: 'STAC6565 Targets Canada in 80% of Attacks as Gold Blade Deploys QWCrypt Ransomware'
date: 2025-12-09
permalink: /posts/2025/12/09/stac6565-targets-canada-in-80-of-attacks-as-gold-blade-deploys-qwcrypt-ransomware/
tags:
- veille-cyber
- hackernews
---
## L'Évolution de Gold Blade : Du Cyber-espionnage au Ransomware Ciblé

Une campagne de cybercriminalité, menée par un groupe identifié sous le nom de STAC6565 et présentant de fortes similitudes avec le groupe Gold Blade (également connu sous les noms de RedCurl, Earth Kapre, et Red Wolf), a ciblé de manière disproportionnée les organisations canadiennes, représentant environ 80% des intrusions observées entre février 2024 et août 2025.

Le groupe, actif depuis fin 2018, a initialement concentré ses activités sur l'espionnage commercial, utilisant des emails de phishing pour mener ses opérations. Cependant, il a récemment diversifié ses méthodes en déployant une souche de ransomware inédite, baptisée QWCrypt. Cette évolution marque un passage d'une approche axée sur la collecte d'informations à une stratégie hybride combinant vol de données et déploiement de ransomware.

### Points Clés :

*   **Ciblage Géographique Étroit :** Les organisations canadiennes sont devenues la principale cible de cette campagne, représentant la grande majorité des attaques.
*   **Évolution des Tactiques :** Le groupe Gold Blade a fait évoluer ses méthodes, passant de l'espionnage à une stratégie incluant le déploiement de ransomware.
*   **Ransomware QWCrypt :** Une nouvelle souche de ransomware, QWCrypt, est activement utilisée dans cette campagne.
*   **Modèle "Hack-for-hire" :** Le groupe opère potentiellement sous un modèle de "piratage pour emploi", réalisant des intrusions personnalisées pour des clients tout en monétisant les accès via le ransomware.
*   **Sophistication Opérationnelle :** Les cybercriminels font preuve d'une maturité opérationnelle notable, affinant leurs techniques et utilisant un ensemble d'outils variés.
*   **Attaques sur les Hyperviseurs :** Une tendance croissante observée est le ciblage direct des hyperviseurs, permettant de contourner les protections traditionnelles des points d'extrémité.

### Vulnérabilités et Méthodes d'Attaque :

*   **Phishing Ciblé :** Les attaques débutent par des emails de spear-phishing adressés au personnel des ressources humaines, incitant à ouvrir des documents malveillants déguisés en CV ou lettres de motivation.
*   **Exploitation des Plateformes de Recrutement :** Les cybercriminels utilisent des plateformes de recherche d'emploi légitimes (Indeed, JazzHR, ADP WorkforceNow) pour héberger des CV piégés, augmentant la probabilité qu'ils soient ouverts et échappant aux filtres d'email.
*   **RedLoader :** Ce malware collecte des informations sur l'hôte infecté et exécute des scripts PowerShell pour recueillir des détails sur l'environnement Active Directory compromis.
*   **Chaînes de Livraison Multi-étapes :** Les attaques impliquent des chaînes de livraison complexes utilisant des archives ZIP, des raccourcis Windows (LNK) se faisant passer pour des PDF, et exploitant `rundll32.exe` et `pcalua.exe` pour l'exécution du code.
*   **Abus de Pilotes Légitimes (BYOVD) :** Utilisation d'une version personnalisée de l'outil Terminator, exploitant un pilote Zemana AntiMalware signé pour désactiver les processus liés à la protection antivirus.
*   **Déploiement du Ransomware :** Les scripts de déploiement de QWCrypt sont adaptés à l'environnement cible, désactivent les mécanismes de récupération et s'attaquent aux hyperviseurs et aux machines virtuelles.
*   **Nettoyage des Traces :** Les scripts de nettoyage visent à supprimer les copies de l'ombre et l'historique des consoles PowerShell pour entraver la récupération forensique.
*   **Outils de Communication :** Utilisation de RPivot (proxy inverse open-source) et Chisel SOCKS5 pour les communications C2.

Il n'y a pas de CVE spécifiques mentionnées dans l'article pour ces attaques.

### Recommandations :

*   **Sécurité des Points d'Entrée :** Renforcer la détection et la prévention des emails de phishing, et sensibiliser le personnel aux risques liés aux pièces jointes et aux liens suspects.
*   **Sécurisation des Plateformes de Recrutement :** Mettre en place des politiques de sécurité strictes pour les documents téléchargés sur les plateformes de recrutement.
*   **Gestion des Identifiants et des Accès :** Mettre en œuvre des politiques de mots de passe robustes et l'authentification multifacteur (MFA).
*   **Sécurisation des Hyperviseurs :**
    *   Utiliser des comptes locaux ESXi.
    *   Appliquer une politique de mots de passe forte.
    *   Segmenter le réseau de gestion des hyperviseurs du réseau de production et des utilisateurs.
    *   Déployer une "jump box" pour auditer l'accès administrateur.
    *   Limiter l'accès au plan de contrôle.
    *   Restreindre l'accès à l'interface de gestion ESXi aux appareils administratifs spécifiques.
*   **Surveillance et Détection :** Mettre en place une surveillance proactive pour détecter les activités suspectes, notamment l'exécution de scripts non autorisés et les tentatives de désactivation de la sécurité.
*   **Mises à Jour et Patchs :** Maintenir les systèmes à jour avec les derniers correctifs de sécurité.

---
[Source](https://thehackernews.com/2025/12/stac6565-targets-canada-in-80-of.html){:target="_blank"}
