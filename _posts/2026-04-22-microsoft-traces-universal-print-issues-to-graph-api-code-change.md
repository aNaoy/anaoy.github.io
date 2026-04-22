---
title: 'Microsoft traces Universal Print issues to Graph API code change'
date: 2026-04-22
permalink: /posts/2026/04/22/microsoft-traces-universal-print-issues-to-graph-api-code-change/
tags:
- veille-cyber
- bleepingcomp
---
### Défaillance du service Microsoft Universal Print liée à l'API Graph

Microsoft a identifié une anomalie technique affectant la création de partages d'imprimantes dans sa solution cloud *Universal Print*. Ce dysfonctionnement fait suite à une mise à jour du code de l'API Microsoft Graph, laquelle a engendré une latence accrue dans la réplication de l'annuaire Entra ID. Cette latence a révélé une condition de concurrence (*race condition*) dans le processus de création des partages, entraînant des échecs récurrents pour les utilisateurs.

**Points clés :**
* **Service impacté :** Universal Print (référence incident : UP1287359).
* **Cause racine :** Mise à jour de l'API Graph provoquant une erreur de code et une latence de réplication dans Entra ID.
* **Comportement :** Échec aléatoire du partage d'imprimantes lors de l'utilisation des options par défaut ("Autoriser tous les utilisateurs" ou sélection de groupes spécifiques lors de la création).

**Vulnérabilités :**
* Aucune CVE associée ; il s'agit d'un incident de service technique lié à une régression logicielle interne et non d'une faille de sécurité exploitable.

**Recommandations de contournement :**
En attendant le déploiement du correctif définitif, Microsoft préconise une méthode de partage en deux étapes :
1. **Création initiale :** Créer le partage d'imprimante sans sélectionner aucun utilisateur ni groupe, et sans cocher l'option "Autoriser tous les utilisateurs de mon organisation".
2. **Configuration des accès :** Patienter 30 secondes, puis accéder à l'onglet "Membres" (ou "Contrôle d'accès") du partage nouvellement créé pour ajouter manuellement les utilisateurs ou groupes de sécurité nécessaires.
3. **Patience :** En cas d'échec, attendre 1 à 2 minutes avant de réitérer l'opération.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-graph-api-code-change-causes-universal-print-share-issues/){:target="_blank"}
