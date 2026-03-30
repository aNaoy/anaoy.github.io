---
title: 'Microsoft pulls KB5079391 Windows update over install issues'
date: 2026-03-30
permalink: /posts/2026/03/30/microsoft-pulls-kb5079391-windows-update-over-install-issues/
tags:
- veille-cyber
- bleepingcomp
---
### Suspension de la mise à jour Windows KB5079391

Microsoft a temporairement retiré la mise à jour facultative **KB5079391** destinée à Windows 11 (versions 24H2 et 25H2). Ce retrait fait suite à la découverte d'une erreur d'installation récurrente empêchant le bon déploiement des correctifs.

**Points clés :**
*   **Problème identifié :** Les utilisateurs rencontrent l'erreur **0x80073712**, indiquant que des fichiers de mise à jour sont manquants ou corrompus.
*   **Contenu de la mise à jour :** Elle incluait des améliorations pour le *Smart App Control*, l'affichage, la fiabilité de Windows Hello (empreinte digitale) et la stabilité de l'environnement de récupération (Windows RE) sur les architectures ARM64.
*   **Contexte instable :** Ce retrait s'ajoute à une série de problèmes récents sur les mises à jour Windows, incluant des bugs de connexion aux comptes Microsoft et des vulnérabilités critiques dans le service RRAS (*Routing and Remote Access Service*).

**Vulnérabilités :**
*   Aucune CVE n'est associée à l'échec de cette mise à jour spécifique, bien que l'article mentionne des correctifs de sécurité récents pour des failles RCE (*Remote Code Execution*) dans le service RRAS.

**Recommandations :**
*   **Action immédiate :** Aucune action n'est requise. La disponibilité de la mise à jour étant limitée par Microsoft via Windows Update, les utilisateurs ne devraient plus être sollicités pour l'installer tant qu'une version corrigée ne sera pas déployée.
*   **Veille :** Surveiller les communications officielles de Microsoft dans les prochaines semaines, une solution étant attendue avant le prochain *Patch Tuesday* prévu le 14 avril.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-pulls-windows-kb5079391-update-over-0x80073712-install-errors/){:target="_blank"}
