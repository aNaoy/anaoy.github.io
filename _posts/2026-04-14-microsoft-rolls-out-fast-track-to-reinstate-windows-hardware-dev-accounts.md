---
title: 'Microsoft rolls out fast-track to reinstate Windows hardware dev accounts'
date: 2026-04-14
permalink: /posts/2026/04/14/microsoft-rolls-out-fast-track-to-reinstate-windows-hardware-dev-accounts/
tags:
- veille-cyber
- bleepingcomp
---
### Accélération de la restauration des comptes développeurs Windows

Microsoft a mis en place une procédure d'urgence pour rétablir l'accès des développeurs à leurs comptes du *Windows Hardware Program*, après une vague de suspensions massives survenues sans préavis. Cette mesure faisait suite à une exigence de vérification d'identité obligatoire pour tout éditeur publiant des pilotes Windows.

**Points clés :**
*   **Impact opérationnel :** Des projets majeurs (WireGuard, VeraCrypt, MemTest86, Windscribe) ont été bloqués, empêchant la publication de mises à jour de sécurité critiques.
*   **Motif de la suspension :** Microsoft invoque le non-respect des procédures de vérification d'identité, nécessaires pour sécuriser la distribution des pilotes en mode noyau (*kernel*).
*   **Problème de communication :** De nombreux développeurs ont affirmé n'avoir reçu aucune notification préalable concernant ces nouvelles obligations de conformité.

**Vulnérabilités associées :**
*   Bien qu'aucune CVE spécifique ne soit liée à cette action, le programme vise à prévenir les attaques de type **BYOVD** (*Bring Your Own Vulnerable Driver*). L'utilisation de pilotes signés légitimement mais vulnérables permet à des attaquants d'élever leurs privilèges au niveau du noyau, une menace récurrente exploitée par des acteurs malveillants.

**Recommandations :**
*   **Procédure de rétablissement :** Les développeurs dont le compte est suspendu doivent ouvrir un ticket de support via le *Hardware Dev Center* en fournissant une justification commerciale claire.
*   **Conformité :** Une fois la procédure accélérée initiée, il est impératif de finaliser immédiatement toutes les étapes de vérification d'identité requises pour conserver l'accès au portail.
*   **Support :** En cas d'échec des outils automatisés, Microsoft invite les utilisateurs à utiliser les contacts de support alternatifs fournis dans leur documentation officielle et à s'assurer d'être connectés avec le compte approprié.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-rolls-out-fast-track-to-reinstate-windows-hardware-dev-accounts/){:target="_blank"}
