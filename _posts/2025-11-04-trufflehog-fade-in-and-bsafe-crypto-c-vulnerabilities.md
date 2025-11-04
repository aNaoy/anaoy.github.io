---
title: 'TruffleHog, Fade In and BSAFE Crypto-C vulnerabilities'
date: 2025-11-04
permalink: /posts/2025/11/04/trufflehog-fade-in-and-bsafe-crypto-c-vulnerabilities/
tags:
- veille-cyber
- zerodaysfans
---
**Trois Failles de Sécurité Détectées dans Divers Logiciels**

Des failles de sécurité ont été identifiées dans les logiciels Fade In, TruffleHog et Dell BSAFE Crypto-C. Ces vulnérabilités ont été corrigées par les éditeurs respectifs.

**Points Clés :**

*   **Fade In :** Des vulnérabilités d'écriture hors limites et d'utilisation après libération de mémoire ont été découvertes dans le module d'analyse XML.
*   **TruffleHog :** Une vulnérabilité d'exécution de code arbitraire a été trouvée dans la fonctionnalité Git.
*   **Dell BSAFE Crypto-C :** Trois failles ont été signalées, incluant des dépassements et sous-dépassements d'entiers ainsi qu'un débordement de pile, affectant la gestion des enregistrements ASN.1.

**Vulnérabilités Identifiées :**

*   **Fade In :**
    *   TALOS-2025-2250 (CVE-2025-53855) : Vulnérabilité d'écriture hors limites.
    *   TALOS-2025-2252 (CVE-2025-53814) : Vulnérabilité d'utilisation après libération de mémoire.
*   **TruffleHog :**
    *   TALOS-2025-2243 (CVE-2025-41390) : Vulnérabilité d'exécution de code arbitraire.
*   **Dell BSAFE Crypto-C :**
    *   TALOS-2025-2140 (CVE-2019-3728) : Vulnérabilité de dépassement d'entier.
    *   TALOS-2025-2141 (CVE-2019-3728) : Vulnérabilité de sous-dépassement d'entier.
    *   TALOS-2025-2142 (CVE-2019-3728) : Vulnérabilité de débordement de pile.

**Recommandations :**

Les correctifs pour ces vulnérabilités sont disponibles auprès des éditeurs concernés. Il est conseillé de maintenir ces logiciels à jour pour se protéger contre les exploitations potentielles. Les règles Snort sont également disponibles pour la détection des tentatives d'exploitation.

---
[Source](https://blog.talosintelligence.com/trufflehog-fade-in-and-bsafe-crypto-c-vulnerabilities/){:target="_blank"}
