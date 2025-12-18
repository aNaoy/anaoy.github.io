---
title: 'Amazon: Ongoing cryptomining campaign uses hacked AWS accounts'
date: 2025-12-18
permalink: /posts/2025/12/18/amazon-ongoing-cryptomining-campaign-uses-hacked-aws-accounts/
tags:
- veille-cyber
- bleepingcomp
---
**Campagne de cryptominage exploitant des comptes AWS compromis**

Une campagne de cryptominage active exploite des identifiants compromis pour accéder aux services Amazon Web Services (AWS), spécifiquement Elastic Compute Cloud (EC2) et Elastic Container Service (ECS). L'objectif est de générer des revenus pour les attaquants en utilisant les ressources de calcul des clients AWS.

**Points Clés :**

*   **Date de début :** La campagne a débuté le 2 novembre.
*   **Méthode d'accès :** Utilisation d'identifiants valides pour les services IAM (Identity and Access Management). Aucune vulnérabilité logicielle n'a été exploitée.
*   **Outil malveillant :** Un conteneur Docker provenant de Docker Hub (image `yenik65958/secret`) contenant un mineur de cryptomonnaie (SBRMiner-MULTI) et un script de démarrage automatique.
*   **Étendue :** Configuration de tâches ECS avec des ressources CPU et mémoire significatives, et création de nombreux groupes d'auto-scaling pour déployer un grand nombre d'instances EC2.
*   **Mécanisme de persistance :** L'attaquant a désactivé la protection contre la résiliation des instances EC2 via l'API (`ModifyInstanceAttribute`), rendant plus difficile et plus lent pour les administrateurs de stopper les opérations de minage.
*   **Rapidité :** Le cryptominage a commencé moins de 10 minutes après l'accès initial, suite à une reconnaissance des quotas de service EC2 et des permissions IAM.

**Vulnérabilités et Recommandations :**

*   **Vulnérabilité :** Aucune vulnérabilité logicielle spécifique (CVE) n'est mentionnée. Le vecteur d'attaque repose sur la compromission d'identifiants IAM valides.
*   **Recommandations :**
    *   **Rotation des identifiants IAM :** Les clients concernés ont été alertés par AWS et doivent impérativement renouveler leurs identifiants IAM compromis.
    *   **Surveillance des activités suspectes :** Maintenir une vigilance accrue sur l'utilisation des ressources et les configurations inhabituelles des services AWS.
    *   **Gestion des permissions IAM :** Appliquer le principe du moindre privilège pour limiter les actions possibles en cas de compromission d'un compte.
    *   **Protection contre la résiliation :** Être conscient de l'impact des protections contre la résiliation des instances et s'assurer que les procédures de réponse aux incidents tiennent compte de ces paramètres.
    *   **Vigilance sur les dépôts d'images :** Les acteurs malveillants peuvent réutiliser des techniques avec des images similaires sous de nouveaux noms ou identifiants de développeur.

---
[Source](https://www.bleepingcomputer.com/news/security/amazon-ongoing-cryptomining-campaign-uses-hacked-aws-accounts/){:target="_blank"}
