---
title: 'Microsoft: Windows Task Manager won’t quit after KB5067036 update'
date: 2025-11-03
permalink: /posts/2025/11/03/microsoft-windows-task-manager-wont-quit-after-kb5067036-update/
tags:
- veille-cyber
- bleepingcomp
---
**Problème de fermeture du Gestionnaire des tâches sous Windows 11**

Une mise à jour optionnelle de Windows 11, KB5067036, publiée le 28 octobre 2025, a introduit un bug empêchant le Gestionnaire des tâches de se fermer complètement. Même après avoir utilisé le bouton "Fermer", des instances de `taskmgr.exe` continuent de s'exécuter en arrière-plan. Cela peut entraîner une consommation excessive de ressources système et une dégradation des performances, se manifestant par des ralentissements et des blocages.

**Points Clés :**

*   L'installation de la mise à jour KB5067036 sur Windows 11 peut causer des problèmes de fermeture du Gestionnaire des tâches.
*   Des processus `taskmgr.exe` persistent en arrière-plan sans fenêtre visible.
*   Une accumulation de ces processus peut dégrader les performances du système.

**Vulnérabilités :**

*   Aucune vulnérabilité spécifique avec un identifiant CVE n'est mentionnée dans cet article. Le problème est décrit comme un "bug" ou un "problème connu".

**Recommandations :**

*   **Solution Temporaire :**
    *   **Manuellement :** Ouvrir une nouvelle instance du Gestionnaire des tâches, sélectionner les processus `taskmgr.exe` en arrière-plan et cliquer sur "Fin de tâche".
    *   **Via l'invite de commandes :** Lancer l'invite de commandes en tant qu'administrateur et exécuter la commande `taskkill.exe /im taskmgr.exe /f`.
*   Microsoft travaille à la résolution de ce problème, mais aucune date de publication pour le correctif n'est précisée.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-windows-task-manager-wont-quit-after-kb5067036-update/){:target="_blank"}
