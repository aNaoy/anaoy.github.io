---
title: 'Researchers Built a Fake Crypto Startup and Hired Three Suspected North Korean IT Workers'
date: 2026-08-11
permalink: /posts/2026/08/11/researchers-built-a-fake-crypto-startup-and-hired-three-suspected-north-korean-it-workers/
tags:
- veille-cyber
- hackernews
---
### Infiltration par des travailleurs IT nord-coréens : une étude de cas par la tromperie

Des chercheurs en cybersécurité ont mis en place une fausse startup de cryptomonnaie (« Ballena Azul ») pour attirer et observer les méthodes d'opérateurs nord-coréens infiltrant le marché du travail technologique. Ces travailleurs cherchent à obtenir des contrats légitimes pour reverser leurs salaires à des agences gouvernementales nord-coréennes, tout en accédant aux systèmes internes et au code source des entreprises.

**Points clés :**
*   **Techniques d'usurpation :** Les candidats utilisent des documents d'identité falsifiés (générés ou modifiés par IA), des numéros de sécurité sociale volés et des comptes bancaires américains.
*   **Reconnaissance et outils :** Une fois embauchés sur des machines virtuelles surveillées, les opérateurs effectuent des profils système, utilisent des outils d'assistance aux entretiens basés sur l'IA (ex: Final Round AI) et installent des extensions de navigateur pour automatiser leurs tâches.
*   **Infrastructure :** Utilisation intensive d'AstrillVPN pour masquer leur localisation réelle et de services comme `2fa.cn` ou `authenticator.cc` pour intercepter les codes d'authentification à deux facteurs.
*   **Risque majeur :** La menace ne réside pas dans une faille logicielle exploitée, mais dans l'accès autorisé et légitime accordé par l'entreprise à un acteur malveillant.

**Vulnérabilités :**
*   *Pas de CVE spécifique associée* : Il s'agit d'une faille au niveau des processus de recrutement (ingénierie sociale) et de la vérification d'identité numérique (KYC - Know Your Customer/Employee).

**Recommandations :**
*   **Vérification continue :** Ne pas se limiter à une vérification d'identité lors de l'embauche, mais pratiquer des contrôles périodiques.
*   **Authentification rigoureuse :** Exiger des vérifications en personne ou par vidéo sécurisée pour le personnel distant.
*   **Surveillance réseau :** Bloquer les nœuds de sortie des VPN connus pour être utilisés par ces réseaux (notamment AstrillVPN).
*   **Formation des recruteurs :** Sensibiliser aux signaux faibles comme les incohérences dans les documents d'identité (métadonnées suspectes, traces de retouche IA/SynthID), les textes générés par traduction automatique ou les accès simultanés depuis des localisations géographiques incohérentes.

---
[Source](https://thehackernews.com/2026/08/researchers-built-fake-crypto-startup.html){:target="_blank"}
