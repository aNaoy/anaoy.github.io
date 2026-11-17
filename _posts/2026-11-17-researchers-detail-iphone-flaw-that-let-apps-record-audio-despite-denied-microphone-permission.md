---
title: 'Researchers Detail iPhone Flaw That Let Apps Record Audio Despite Denied Microphone Permission'
date: 2026-11-17
permalink: /posts/2026/11/17/researchers-detail-iphone-flaw-that-let-apps-record-audio-despite-denied-microphone-permission/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique sur iOS : Contournement des permissions du microphone

Une faille de sécurité majeure, désormais corrigée, permettait à des applications tierces d'enregistrer le microphone sur iPhone et iPad, même lorsque l'utilisateur avait explicitement refusé l'autorisation.

**Points clés :**
* **Mécanisme de l'attaque :** Le service audio `audiomxd` se fiait au jeton d'audit fourni par l'application pour vérifier son identité. Les applications malveillantes pouvaient usurper l'identité du service lui-même, forçant le système à autoriser l'enregistrement sans passer par le contrôle de confidentialité (TCC).
* **Indicateur visuel :** Dans certaines configurations, l'indicateur orange (signalant l'usage du micro) n'apparaissait pas, rendant l'enregistrement totalement invisible pour l'utilisateur.
* **Persistance :** Une fois lancé, l'enregistrement pouvait se poursuivre en arrière-plan et même lorsque l'appareil était verrouillé.
* **Absence d'exploitation connue :** Aucun cas d'exploitation malveillante n'a été signalé.

**Vulnérabilité :**
* **CVE-2026-65339 :** Score CVSS de 5.0. Cette faille permettait de contourner les permissions de confidentialité liées au microphone.

**Recommandations :**
* **Mise à jour immédiate :** L'installation des correctifs Apple est la seule protection contre cette faille. Assurez-vous que vos appareils (iPhone, iPad, Mac, Apple TV, Apple Watch et Vision Pro) sont à jour avec les versions déployées à partir d'août 2026 (ex: iOS 26.6.1 ou 18.7.11).
* **Vigilance :** Bien que le correctif soit en place, il est recommandé de surveiller régulièrement les autorisations d'accès au microphone dans les réglages de confidentialité de vos appareils.

---
[Source](https://thehackernews.com/2026/11/researchers-detail-iphone-flaw-that-let.html){:target="_blank"}
