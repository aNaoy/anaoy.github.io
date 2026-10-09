---
title: 'TP-Link Sued by Four More U.S. States Over Router Security and China Ties'
date: 2026-10-09
permalink: /posts/2026/10/09/tp-link-sued-by-four-more-us-states-over-router-security-and-china-ties/
tags:
- veille-cyber
- hackernews
---
### Actions en justice contre TP-Link : enjeux de sécurité et liens avec la Chine

Plusieurs États américains ont engagé des poursuites judiciaires contre TP-Link, accusant le fabricant de router de tromper les consommateurs sur la sécurité de ses équipements et sur son indépendance vis-à-vis de la Chine. TP-Link conteste ces allégations, affirmant être une entreprise indépendante dont les produits destinés au marché américain sont fabriqués au Vietnam.

**Points clés :**
* **Pratiques commerciales :** Les poursuites dénoncent une publicité mensongère concernant la protection « HomeShield » et le manque de transparence sur les risques liés aux lois sur le renseignement chinois (accès potentiel aux données des applications Tether, Tapo, Deco et Kasa).
* **Risques d'espionnage :** Les plaintes soulignent l'utilisation passée de routeurs TP-Link par des acteurs étatiques (campagnes de piratage, botnets) et s'inquiètent de la dépendance de la chaîne d'approvisionnement envers la Chine.
* **Pression réglementaire :** 21 procureurs généraux ont alerté la FCC, demandant une vigilance accrue avant d'autoriser de nouveaux modèles de routeurs TP-Link sur le territoire américain.

**Vulnérabilités majeures (série Aginet) :**
Des chercheurs ont révélé cinq vulnérabilités critiques affectant 65 modèles (gammes HB, HX, HC, EB, EC, EX, XC, XX et VX) permettant une prise de contrôle totale par un attaquant authentifié ou non (selon la faille) :
* **CVE-2025-30237 (Score 8.7) :** Contournement de l'authentification sur l'interface web (accès administrateur sans mot de passe).
* **CVE-2025-30238 (Score 8.6) :** Élévation de privilèges permettant la création d'un compte super-admin et l'activation SSH.
* **CVE-2025-30239 (Score 8.5) :** Déchiffrement de mots de passe stockés via des clés codées en dur.
* **CVE-2025-30240 (Score 5.1) :** Lecture de fichiers via un périphérique USB malveillant.
* **CVE-2025-30241 (Score 8.6) :** Exécution de commandes système avec privilèges élevés.

**Recommandations :**
* **Mise à jour immédiate :** Vérifier l'interface de gestion du routeur ou l'application dédiée pour installer les correctifs de firmware.
* **Contact FAI :** Pour les appareils fournis par un fournisseur d'accès internet (FAI), si aucune mise à jour n'est disponible via l'interface, contacter directement le support technique du FAI, car les firmwares personnalisés ne sont parfois pas diffusés publiquement par TP-Link.

---
[Source](https://thehackernews.com/2026/10/tp-link-sued-by-four-more-us-states.html){:target="_blank"}
