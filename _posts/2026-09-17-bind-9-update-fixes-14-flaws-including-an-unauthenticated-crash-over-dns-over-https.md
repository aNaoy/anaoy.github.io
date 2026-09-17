---
title: 'BIND 9 Update Fixes 14 Flaws, Including an Unauthenticated Crash Over DNS-over-HTTPS'
date: 2026-09-17
permalink: /posts/2026/09/17/bind-9-update-fixes-14-flaws-including-an-unauthenticated-crash-over-dns-over-https/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans BIND 9 : 14 failles corrigées

L'Internet Systems Consortium (ISC) a publié des mises à jour correctives (versions 9.20.29 et 9.21.26) pour BIND 9, résolvant 14 vulnérabilités de sécurité. Bien qu'aucune exploitation active ne soit signalée, l'ISC souligne que les tests de reproduction des failles sont publics, facilitant potentiellement la création d'outils d'attaque.

**Points clés :**
*   **Gravité :** Sept vulnérabilités sont classées "Hautes" (score CVSS de 7,5), les sept autres sont classées "Moyennes".
*   **Impact :** Les failles permettent des dénis de service (crashs du processus `named`), une consommation excessive de ressources (CPU/mémoire), ou des empoisonnements de cache DNS.
*   **Fin de support :** La branche 9.18 n'est plus supportée et reste vulnérable à 12 de ces 14 failles.

**Vulnérabilités notables :**
*   **CVE-2026-77692 :** Crash du serveur via une requête DNS-over-HTTPS (DoH) non authentifiée utilisant une signature SIG(0) invalide.
*   **CVE-2026-76163 :** Crash lors d'une requête TKEY si aucune configuration globale n'est définie dans `named.conf`.
*   **CVE-2026-19667 / 19666 / 80274 :** Divers vecteurs de crash ciblant les résolveurs récursifs via des réponses DNS spécialement forgées.
*   **CVE-2026-81563 / 81736 :** Épuisement des ressources (cache/CPU) via des enregistrements alias SVCB/HTTPS.
*   **CVE-2026-19941 / 77119 :** Empoisonnement de cache via des preuves DNSSEC malicieuses.

**Recommandations :**
*   **Mise à jour immédiate :** Passer à BIND 9.20.29 (branche stable) ou 9.21.26 (branche développement).
*   **Abandon des versions EOL :** Les utilisateurs des versions antérieures (notamment la 9.18) doivent migrer vers la version 9.20 sans délai, car elles ne bénéficieront d'aucun correctif.
*   **Surveillance :** Aucune solution de contournement n'étant disponible, l'application des correctifs est la seule mesure de protection efficace.

---
[Source](https://thehackernews.com/2026/09/bind-9-update-fixes-14-flaws-including.html){:target="_blank"}
