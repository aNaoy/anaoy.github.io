---
title: 'Vulnérabilité dans Oracle Java SE (18 novembre 2026)'
date: 2026-11-18
permalink: /posts/2026/11/18/vulnerabilite-dans-oracle-java-se-18-novembre-2026/
tags:
- veille-cyber
- certfr
---
### Vulnérabilité critique "java4shell" dans Oracle Java SE

La vulnérabilité **CVE-2026-114938** affecte le décodeur Base64 d'OpenJDK sur les processeurs x86-64 supportant les instructions AVX-512 VBMI. Cette faille expose de nombreux produits d'entreprise (Jira, Jenkins, Elasticsearch, etc.) à des risques d'exécution de code arbitraire et de déni de service à distance.

**Points clés :**
*   **Vulnérabilité :** CVE-2026-114938 ("java4shell").
*   **Cause :** Défaut dans le décodeur Base64 lié à l'optimisation matérielle AVX-512 VBMI.
*   **Impact :** Exécution de code à distance et déni de service (DoS).
*   **Cibles :** Versions spécifiques d'Oracle Java SE, Oracle GraalVM Enterprise Edition et Oracle GraalVM for JDK.
*   **Exploitation :** Nécessite l'envoi de données Base64 malveillantes spécifiques vers les composants affectés.

**Recommandations :**
*   **Correction :** Appliquer les correctifs de sécurité fournis dans les bulletins officiels d'Oracle et d'OpenJDK.
*   **Vérification :** Identifier si les serveurs utilisent des processeurs vulnérables via la commande Linux : `grep -m1 '^flags' /proc/cpuinfo | tr ' ' '
' | grep -E '^(avx512f|avx512bw|avx512vbmi|bmi2)$'`.
*   **Contournement provisoire :** En cas d'impossibilité d'appliquer les correctifs immédiatement, lancer OpenJDK avec les options JVM suivantes : `-XX:-UseBASE64Intrinsics` et `-XX:UseAVX=2`.

---
[Source](https://www.cert.cyber.gouv.fr/alerte/CERTFR-2026-ALE-016/){:target="_blank"}
