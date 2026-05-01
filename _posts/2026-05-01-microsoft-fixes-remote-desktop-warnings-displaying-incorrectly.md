---
title: 'Microsoft fixes Remote Desktop warnings displaying incorrectly'
date: 2026-05-01
permalink: /posts/2026/05/01/microsoft-fixes-remote-desktop-warnings-displaying-incorrectly/
tags:
- veille-cyber
- bleepingcomp
---
### Correction d'un bug d'affichage critique dans les alertes RDP de Windows

Microsoft a déployé un correctif pour résoudre un problème d'affichage affectant les avertissements de sécurité lors de l'ouverture de fichiers de Bureau à distance (.rdp). Ce bug, apparu suite aux mises à jour de sécurité d'avril 2026, rendait les fenêtres d'alerte illisibles ou impossibles à manipuler sur les configurations multi-écrans avec des paramètres de mise à l'échelle différents.

**Points clés :**
* **Contexte :** Les avertissements de sécurité RDP ont été renforcés pour désactiver par défaut le partage de ressources locales, une mesure de défense contre les campagnes de phishing exploitant ces fichiers pour le vol de données ou d'identifiants (notamment par le groupe APT29).
* **Dysfonctionnement :** Sur les systèmes affectés, les boutons des boîtes de dialogue étaient mal alignés ou masqués, empêchant les utilisateurs d'interagir correctement avec les alertes de sécurité essentielles.
* **Vulnérabilité associée :** Aucune CVE spécifique n'est mentionnée pour ce bug d'affichage, bien que les mesures de sécurité qu'il impacte visent à prévenir l'exécution de code malveillant via des fichiers .rdp non signés.
* **Effets collatéraux :** La mise à jour d'avril (KB5083769) est également signalée comme causant des échecs de logiciels de sauvegarde tiers en raison de délais d'attente (timeout) du service VSS (Volume Shadow Copy Service).

**Recommandations :**
* **Application des correctifs :** Installez la mise à jour cumulative optionnelle **KB5083631** pour Windows 11 afin de restaurer l'affichage correct des fenêtres d'alerte RDP.
* **Vigilance RDP :** Soyez particulièrement attentif aux avertissements "Caution: Unknown remote connection" lors de l'ouverture de fichiers .rdp provenant de sources non vérifiées, car ces fichiers peuvent être utilisés par des attaquants pour détourner des ressources locales.
* **Gestion des sauvegardes :** Si vous utilisez des solutions de sauvegarde tiers, vérifiez la compatibilité après l'installation des correctifs d'avril 2026 et surveillez les journaux d'erreurs liés au service VSS.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-fixes-remote-desktop-warnings-displaying-incorrectly/){:target="_blank"}
