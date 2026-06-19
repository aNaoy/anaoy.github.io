---
title: 'Apple Patches Beats Studio Buds Flaw Letting Nearby Attackers Spy via Microphone'
date: 2026-06-19
permalink: /posts/2026/06/19/apple-patches-beats-studio-buds-flaw-letting-nearby-attackers-spy-via-microphone/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques chez Apple : Écoute clandestine sur Beats et faille matérielle sur puces A12/A13

**Faille de sécurité sur les Beats Studio Buds**
Apple a corrigé une vulnérabilité critique affectant le SDK Bluetooth Airoha des écouteurs Beats Studio Buds. Cette faille permet à un attaquant situé à proximité d'appairer les écouteurs sans consentement et d'écouter via le microphone sans interaction de l'utilisateur.

*   **Vulnérabilité :** CVE-2025-20701 (Score CVSS : 8.8) – Défaut d'autorisation dans le SDK Airoha.
*   **Impact :** Élévation de privilèges à distance, accès complet au microphone et possibilité de compromettre des appareils déjà appairés.
*   **Recommandation :** Mettre à jour les écouteurs vers la version de firmware **1B211**.

**Faille matérielle inhérente aux puces A12 et A13 (usbliter8)**
Une nouvelle vulnérabilité matérielle de type *BootROM* a été découverte dans les contrôleurs USB des puces Apple A12 et A13. Le défaut, baptisé *usbliter8*, permet d'injecter du code malveillant en exploitant un dépassement de tampon (*buffer underflow*) lié à une mauvaise configuration du mode "bypass" du contrôleur USB.

*   **Vulnérabilité :** Défaut matériel (non patchable par logiciel).
*   **Impact :** Exécution de code arbitraire au niveau du *SecureROM*, brisant la chaîne de confiance de l'appareil.
*   **Recommandation :** Cette faille résidant dans le matériel immuable, aucune correction logicielle n'est possible. La seule mitigation efficace pour les utilisateurs concernés est la migration vers des modèles d'appareils plus récents (équipés de puces A14 ou ultérieures).

---
[Source](https://thehackernews.com/2026/06/apple-patches-beats-studio-buds-flaw.html){:target="_blank"}
