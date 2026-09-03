---
title: 'HPE patches critical ArubaOS-CX remote code execution flaw'
date: 2026-09-03
permalink: /posts/2026/09/03/hpe-patches-critical-arubaos-cx-remote-code-execution-flaw/
tags:
- veille-cyber
- bleepingcomp
---
### Vulnérabilités critiques dans ArubaOS-CX : HPE publie des correctifs

HPE a corrigé une faille critique de type dépassement de tampon dans son système d'exploitation réseau ArubaOS-CX, ainsi que 23 autres vulnérabilités de sécurité. Ces failles affectent les commutateurs réseau destinés aux grandes entreprises, centres de données et organisations gouvernementales. Aucune exploitation active n'a été signalée à ce jour.

**Points clés :**
*   La vulnérabilité principale permet à un attaquant distant non authentifié d'exécuter du code arbitraire avec des privilèges élevés via l'envoi de paquets malveillants.
*   Le bulletin de sécurité inclut une série d'autres vulnérabilités (scores de sévérité entre 8.1 et 8.8) permettant, selon les cas, le déni de service, l'escalade de privilèges, l'exécution de commandes arbitraires, ou le contournement de l'authentification.
*   Les vecteurs d'attaque incluent l'interface de gestion web, les API et le terminal (CLI).

**Vulnérabilités majeures identifiées :**
*   **CVE-2026-73749 :** Dépassement de tampon (RCE critique).
*   **CVE-2026-73751 / CVE-2026-73753 :** Exécution de commandes arbitraires par des utilisateurs authentifiés à faibles privilèges.
*   **CVE-2026-73752 / CVE-2026-73782 :** RCE via API ou CLI (accès réseau adjacent).
*   **CVE-2026-73778 :** Utilisation de mots de passe par défaut pour obtenir un contrôle administratif total.
*   **CVE-2026-73779 :** Contournement des contrôles d'authentification.

**Recommandations :**
*   Appliquer immédiatement les mises à jour du firmware vers les versions corrigées listées par HPE (ex: 10.18.1002+, 10.17.1030+, 10.16.1060+, 10.13.1190+, 10.10.1181+).
*   Vérifier la configuration des équipements sortant d'usine pour s'assurer que les mots de passe par défaut ont été modifiés.
*   Restreindre l'accès aux interfaces de gestion et aux API aux seuls réseaux de confiance.

---
[Source](https://www.bleepingcomputer.com/news/security/hpe-patches-critical-arubaos-cx-remote-code-execution-flaw/){:target="_blank"}
