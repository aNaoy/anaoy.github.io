---
title: 'Hundreds of leaked AWS keys give full control over corporate accounts'
date: 2026-08-21
permalink: /posts/2026/08/21/hundreds-of-leaked-aws-keys-give-full-control-over-corporate-accounts/
tags:
- veille-cyber
- bleepingcomp
---
### Risque critique : Plus de 9 000 clés AWS exposées publiquement

Une vaste campagne de fuite de données a révélé que plus de 9 300 clés d'accès AWS, exposées entre 2022 et 2026, demeurent actives. Cette vulnérabilité concerne des centaines d'entreprises, avec un risque élevé d'accès non autorisé aux infrastructures cloud.

**Points clés :**
*   **Volume d'exposition :** 9 300 clés actives identifiées, dont 817 appartiennent à des entreprises.
*   **Niveau de privilège :** 526 clés sont des clés "root" (accès total illimité) et 242 sont associées à des utilisateurs IAM avec des droits d'administrateur.
*   **Origine des fuites :** Les clés ont été retrouvées dans des dépôts de code, des logs CI, des images Docker et des plateformes comme Hugging Face.
*   **Absence de rotation :** La durée de vie médiane des clés est extrêmement longue (plus de 5 ans), témoignant d'une négligence généralisée en matière de gestion des secrets.
*   **Conséquences :** Un attaquant peut exfiltrer des données, supprimer des ressources, créer des comptes administrateurs fantômes ou déployer des mineurs de cryptomonnaies aux frais de l'entreprise.

**Vulnérabilités :**
*   Il ne s'agit pas d'une faille logicielle (CVE), mais d'une **mauvaise configuration et d'une gestion inadéquate des secrets** (fuites de credentials dans les référentiels de code publics).

**Recommandations :**
*   **Suppression immédiate :** Éliminer tous les accès "root" inutiles.
*   **Rotation systématique :** Révoquer et renouveler immédiatement toute clé ayant été exposée ou présente dans un dépôt de code (considérer toute clé publique comme compromise).
*   **Audit IAM :** Examiner régulièrement les identifiants en fonction de leur ancienneté et supprimer les clés inutilisées.
*   **Surveillance budgétaire :** Configurer des alertes de budget AWS pour détecter rapidement toute activité anormale liée à des coûts imprévus (ex: cryptomining).
*   **Gestion des secrets :** Mettre en œuvre des outils de scan automatisés pour empêcher le commit de clés secrètes dans les dépôts de code.

---
[Source](https://www.bleepingcomputer.com/news/security/hundreds-of-leaked-aws-keys-give-full-control-over-corporate-accounts/){:target="_blank"}
