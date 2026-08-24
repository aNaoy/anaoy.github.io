---
title: 'Microsoft: August updates break printing, PDF export in WPF apps'
date: 2026-08-24
permalink: /posts/2026/08/24/microsoft-august-updates-break-printing-pdf-export-in-wpf-apps/
tags:
- veille-cyber
- bleepingcomp
---
### Dysfonctionnements d'impression et d'export PDF dans les applications WPF

La mise à jour cumulative du .NET Framework d'août 2026 provoque des erreurs système (`System.IO.FileFormatException`) lors de l'impression ou de l'exportation de fichiers (PDF/XPS) au sein d'applications utilisant le framework WPF (Windows Presentation Foundation), notamment lors de l'utilisation de polices comme Calibri.

**Points clés :**
*   **Périmètre :** Le problème touche toutes les versions de Windows 10, Windows 11 et Windows Server (de 2012 à 2025).
*   **Origine :** Une incompatibilité introduite par la mise à jour de sécurité d'août 2026 au niveau de la gestion des polices dans les applications WPF.

**Vulnérabilités :**
*   Aucune CVE spécifique n'a été attribuée à cet incident, mais l'utilisation du contournement temporaire proposé par Microsoft réactive des vulnérabilités que la mise à jour initiale visait précisément à corriger.

**Recommandations :**
*   **Usage restreint :** Microsoft conseille d'utiliser le correctif temporaire uniquement si l'activité métier est critique et ne peut être interrompue.
*   **Contournement temporaire :** Pour rétablir les fonctionnalités d'impression, il est nécessaire d'ajouter la configuration suivante au fichier de configuration de l'application (`App.config`) :
    ```xml
    <configuration>
     <runtime>
       <AppContextSwitchOverrides
         value="Switch.MS.Internal.TtfDelta.DisableCmapAndSbitOverflowProtection=true"/>
     </runtime>
    </configuration>
    ```
*   **Risque de sécurité :** L'activation de ce paramètre expose le système à des attaques exploitant les vulnérabilités patchées en août 2026. Il est impératif de retirer cette modification dès qu'un correctif permanent sera déployé par Microsoft.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-august-updates-break-printing-pdf-export-in-wpf-apps/){:target="_blank"}
