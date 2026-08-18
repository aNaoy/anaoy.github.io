---
title: 'Microsoft starts removing WMIC tool used by cybercriminals'
date: 2026-08-18
permalink: /posts/2026/08/18/microsoft-starts-removing-wmic-tool-used-by-cybercriminals/
tags:
- veille-cyber
- bleepingcomp
---
### Fin du support de l'outil WMIC par Microsoft

Microsoft a officiellement retiré l'utilitaire en ligne de commande **WMIC** (Windows Management Instrumentation Command-line) à partir des versions Windows 11 24H2 et 25H2. Ce composant hérité, qui n'est désormais plus disponible en tant que fonctionnalité à la demande (FoD), était progressivement déprécié depuis 2016.

**Points clés :**
* **Nature de l'outil :** WMIC est une interface textuelle permettant d'interagir avec le système WMI.
* **Sécurité :** L'outil était largement utilisé comme *LOLBIN* (Living-off-the-Land Binary). Il permettait aux attaquants d'exécuter des commandes malveillantes en utilisant un binaire légitime signé par Microsoft, rendant la détection difficile.
* **Portée :** Seul l'outil WMIC est concerné ; l'infrastructure WMI (Windows Management Instrumentation) elle-même reste pleinement opérationnelle.

**Vecteurs d'attaques associés :**
WMIC était fréquemment détourné pour des activités malveillantes, notamment :
* Suppression des clichés instantanés (*Shadow Volume Copies*) par les ransomwares pour empêcher la restauration des données.
* Désactivation ou désinstallation de solutions antivirus et de sécurité.
* Ajout d'exclusions dans Microsoft Defender pour masquer des processus malveillants.

**Recommandations pour les administrateurs :**
* Migrer les scripts et tâches automatisées basés sur WMIC vers des alternatives modernes.
* Privilégier l'utilisation de **PowerShell**, des API COM de WMI, des bibliothèques .NET ou d'autres langages de script actuels pour la gestion du système.
* Consulter la documentation officielle de Microsoft pour obtenir des guides de transition détaillés.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-removes-wmic-lolbin-tool-in-windows-11-beta-builds/){:target="_blank"}
