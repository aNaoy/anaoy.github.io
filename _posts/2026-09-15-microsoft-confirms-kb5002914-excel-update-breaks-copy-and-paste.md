---
title: 'Microsoft confirms KB5002914 Excel update breaks copy and paste'
date: 2026-09-15
permalink: /posts/2026/09/15/microsoft-confirms-kb5002914-excel-update-breaks-copy-and-paste/
tags:
- veille-cyber
- bleepingcomp
---
### Dysfonctionnement de la fonction "Copier-Coller" dans Excel suite à la mise à jour KB5002914

La mise à jour de sécurité de septembre 2026 (KB5002914) provoque une régression de code affectant Microsoft Excel (versions 2016, 2019, 2021 et 2024). Cette défaillance empêche le bon fonctionnement du copier-coller, du remplissage automatique et du glissement de formules, sans générer de message d'erreur pour l'utilisateur.

**Points clés :**
*   **Impact :** L'échec du copier-coller est silencieux ; le contenu source reste sélectionné et la destination demeure inchangée.
*   **Cause :** Une régression logicielle introduite par le correctif de sécurité du "Patch Tuesday" de septembre 2026.
*   **Vulnérabilités :** Bien que la mise à jour KB5002914 visait à corriger plusieurs vulnérabilités d'exécution de code à distance (RCE) et de divulgation d'informations, aucune CVE spécifique n'est mentionnée comme étant directement liée à ce bug fonctionnel.

**Recommandations :**
*   **Solution de contournement :** La désinstallation de la mise à jour KB5002914 rétablit les fonctionnalités sur les systèmes impactés.
*   **Procédure :** Microsoft fournit des commandes spécifiques via l'invite de commande (en mode administrateur) pour revenir à une version précédente selon la suite Office utilisée :
    *   **Office 2016 :** Utiliser `Oarpmany.exe /removereleaseinpatch` avec le code produit correspondant.
    *   **Office 2019 :** Exécuter `OfficeC2RClient.exe` avec le paramètre `updatetoversion=16.0.10417.20197`.
    *   **Office 2021 & 2024 :** Exécuter `OfficeC2RClient.exe` avec le paramètre `updatetoversion=16.0.20326.20132`.
*   **Suivi :** Il est conseillé de surveiller les communications officielles de Microsoft pour l'annonce d'un correctif définitif.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-september-kb5002914-security-update-breaks-excel-copy-and-paste/){:target="_blank"}
