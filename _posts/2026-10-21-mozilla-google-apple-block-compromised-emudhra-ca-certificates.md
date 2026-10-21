---
title: 'Mozilla, Google, Apple block compromised eMudhra CA certificates'
date: 2026-10-21
permalink: /posts/2026/10/21/mozilla-google-apple-block-compromised-emudhra-ca-certificates/
tags:
- veille-cyber
- bleepingcomp
---
### Révocation massive de certificats eMudhra suite à une erreur de génération cryptographique

Huit certificats intermédiaires de l'autorité de certification eMudhra ont été révoqués après la découverte d'une faille critique dans la génération de leurs clés privées. Une erreur dans un script utilisé en avril 2025 a conduit à la création de clés P-384 extrêmement faibles, avec des valeurs numériques suffisamment basses pour être retrouvées en quelques secondes. Bien qu'aucune preuve d'exploitation malveillante n'ait été constatée, cette vulnérabilité permettait théoriquement à un attaquant de forger des certificats légitimes et d'intercepter des communications chiffrées.

**Points clés :**
*   **Cause :** Erreur de script ayant généré des clés cryptographiques prévisibles.
*   **Risque :** Usurpation d'identité numérique et interception de trafic (Man-in-the-Middle).
*   **Action immédiate :** Mozilla, Google et Apple ont bloqué ces certificats via leurs mécanismes de révocation (OneCRL, etc.).
*   **Complexité :** Les logiciels gérant leur propre magasin de certificats ou n'effectuant pas de vérification de révocation restent potentiellement vulnérables tant qu'ils ne sont pas mis à jour.

**Vulnérabilité :**
*   **CVE-2026-111943 :** Affecte spécifiquement le langage Go, mais la faille concerne l'ensemble de l'écosystème utilisant les certificats compromis d'eMudhra.

**Recommandations :**
*   **Mise à jour système :** Appliquer les correctifs pour les environnements de développement (Go, Node.js, Python, Rust, etc.) et les bibliothèques de certificats (ca-certificates sous Linux, etc.).
*   **Vérification :** Consulter le site [emudhra.we-have-a-problem.com](https://emudhra.we-have-a-problem.com/) pour identifier les logiciels affectés et vérifier l'état de vulnérabilité de vos systèmes.
*   **Attention aux outils isolés :** Être vigilant avec les outils comme `curl` sous macOS, qui peuvent ne pas vérifier nativement la révocation des certificats, nécessitant des interventions manuelles.

---
[Source](https://www.bleepingcomputer.com/news/security/mozilla-google-apple-block-compromised-emudhra-ca-certificates/){:target="_blank"}
