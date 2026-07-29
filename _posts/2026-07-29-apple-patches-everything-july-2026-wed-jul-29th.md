---
title: 'Apple Patches Everything (July 2026), (Wed, Jul 29th)'
date: 2026-07-29
permalink: /posts/2026/07/29/apple-patches-everything-july-2026-wed-jul-29th/
tags:
- veille-cyber
- sans-isc
---
### Mise à jour de sécurité massive chez Apple : Juillet 2026

Apple a publié des mises à jour correctives pour l'ensemble de ses systèmes d'exploitation (iOS, iPadOS, macOS, tvOS, watchOS, visionOS) ainsi que pour Safari, traitant un total de **187 vulnérabilités**. Aucune de ces failles n'est connue comme étant actuellement exploitée.

#### Points clés
*   **Portée :** Les correctifs concernent principalement les versions actuelles (26), tandis que les versions plus anciennes (macOS 14 et 15) ont également bénéficié de mises à jour.
*   **Objectif :** En plus de corriger des failles classiques (déni de service, élévation de privilèges, WebKit), ces mises à jour préparent les systèmes aux futures versions majeures prévues pour l'automne, notamment par des ajustements de Spotlight.

#### Vulnérabilités notables
L'article met en avant plusieurs CVE critiques liées au contournement des contrôles Gatekeeper via des archives ZIP malveillantes :
*   **CVE-2026-28849** (BOM)
*   **CVE-2026-28900** (libarchive)
*   **CVE-2026-28914** (zip)

D'autres types de vulnérabilités récurrentes incluent :
*   **Élévation de privilèges / Root :** CVE-2026-28912, CVE-2026-39874, CVE-2026-39875, CVE-2026-43693, CVE-2026-43698.
*   **Contournement de la Sandbox :** CVE-2026-28973, CVE-2026-43772, CVE-2026-64702, CVE-2026-64731, CVE-2026-64737, CVE-2026-64738, CVE-2026-64740.
*   **Exécution de code arbitraire :** CVE-2026-28981 (HFS), CVE-2026-43776 (AppleDouble), CVE-2026-64747 (AVEVideoEncoder).
*   **Multiples vulnérabilités WebKit :** Touchant la gestion de la mémoire, les plantages de processus et l'exfiltration de données (ex: CVE-2026-43700, CVE-2026-43701, CVE-2026-43705, CVE-2026-43708, CVE-2026-43713).

#### Recommandations
*   **Application immédiate :** Mettre à jour tous les appareils Apple vers les versions 26.6 ou les versions spécifiques de correctifs de sécurité (Sequoia 15.7.8, Sonoma 14.8.8) pour bénéficier des patchs.
*   **Vigilance sur les fichiers :** La présence de failles exploitant des archives ZIP malveillantes pour contourner Gatekeeper souligne l'importance de ne télécharger des fichiers que depuis des sources fiables.
*   **Surveillance :** Étant donné le nombre élevé de failles touchant le noyau (Kernel) et les pilotes, l'installation rapide des correctifs est essentielle pour limiter les risques d'élévation de privilèges locaux.

---
[Source](https://isc.sans.edu/diary/rss/33196){:target="_blank"}
