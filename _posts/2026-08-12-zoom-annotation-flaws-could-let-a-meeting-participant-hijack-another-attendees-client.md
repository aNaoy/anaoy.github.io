---
title: 'Zoom Annotation Flaws Could Let a Meeting Participant Hijack Another Attendees Client'
date: 2026-08-12
permalink: /posts/2026/08/12/zoom-annotation-flaws-could-let-a-meeting-participant-hijack-another-attendees-client/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans l'outil d'annotation de Zoom

Des failles de sécurité découvertes dans la fonctionnalité d'annotation de Zoom permettaient à un participant de prendre le contrôle à distance de l'ordinateur d'autres utilisateurs sans aucune interaction de leur part (attaque "zero-click"). Le problème résidait dans une gestion défaillante des données structurées transmises lors des annotations, permettant notamment des dépassements de tampon (*buffer overflow*) et l'exécution de code arbitraire.

**Points clés :**
*   **Mécanisme d'attaque :** L'attaquant envoyait des messages malformés qui étaient traités par le client de la victime sans vérification de l'origine ou de la taille des données.
*   **Rapidité d'exploitation :** Les chercheurs ont pu concevoir un exploit fonctionnel en moins d'une journée en utilisant des modèles d'IA.
*   **Absence de preuve d'exploitation :** Bien que critiques, ces vulnérabilités n'ont pas été exploitées dans la nature avant leur correction.

**Vulnérabilités identifiées :**
*   **CVE-2026-53413 :** Dépassement de tampon (Score CVSS 8.3).
*   **CVE-2026-53414 :** Dépassement de lecture (Score CVSS 6.5).
*   **CVE-2026-53415 :** Utilisation après libération (*Use-after-free*) (Score CVSS 8.3).

**Recommandations :**
*   **Mise à jour immédiate :** S'assurer que les clients Zoom sont mis à jour vers les versions correctives publiées entre juin et juillet 2026.
*   **Versions cibles :** 
    *   **Zoom Workplace :** Versions 7.1.5 ou 7.0.6 (selon les branches).
    *   **Zoom Workplace VDI (Windows) :** Versions 7.0.11 ou 6.6.16.
    *   **Zoom Rooms et SDK :** Version 7.1.0 (ou 7.1.5 pour la troisième faille).

---
[Source](https://thehackernews.com/2026/08/zoom-annotation-flaws-could-let-meeting.html){:target="_blank"}
