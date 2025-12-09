---
title: 'Ivanti warns of critical Endpoint Manager code execution flaw'
date: 2025-12-09
permalink: /posts/2025/12/09/ivanti-warns-of-critical-endpoint-manager-code-execution-flaw/
tags:
- veille-cyber
- bleepingcomp
---
**Ivanti EPM : Vulnérabilité Critique de Code Exécution et Autres Failles**

Une faille de sécurité critique, identifiée comme **CVE-2025-10573**, a été découverte dans le logiciel Endpoint Manager (EPM) d'Ivanti. Cette vulnérabilité de type Cross-Site Scripting (XSS) stocké, bien que nécessitant une interaction utilisateur, permet à des attaquants non authentifiés d'injecter du code JavaScript malveillant. L'exploitation vise à empoisonner le tableau de bord web de l'administrateur EPM, menant potentiellement à l'exécution de code côté client et à la prise de contrôle de la session de l'administrateur.

Ivanti a publié une mise à jour, EPM 2024 SU4 SR1, pour corriger cette faille. Bien que la solution EPM ne soit pas conçue pour être exposée en ligne, des centaines d'instances sont actuellement accessibles via Internet, principalement aux États-Unis, en Allemagne et au Japon.

Parallèlement, trois autres vulnérabilités de haute sévérité ont été corrigées :
*   **CVE-2025-13659** et **CVE-2025-13662** : Ces failles, également de type exécution de code arbitraire à distance, requièrent que l'attaquant interagisse avec un serveur cœur non fiable ou importe des fichiers de configuration non fiables.

Ivanti n'a pas connaissance d'exploitations de ces vulnérabilités avant leur divulgation publique. Cependant, l'historique des failles de sécurité découvertes dans les produits Ivanti EPM montre qu'elles sont souvent ciblées par des acteurs malveillants. Des vulnérabilités similaires dans EPM ont été précédemment identifiées comme activement exploitées.

**Points Clés :**
*   Découverte d'une vulnérabilité critique (CVE-2025-10573) dans Ivanti Endpoint Manager (EPM).
*   La faille permet l'exécution de code JavaScript arbitraire via une attaque XSS stocké.
*   Trois autres vulnérabilités de haute sévérité (CVE-2025-13659, CVE-2025-13662) ont été corrigées.
*   Des centaines d'instances EPM exposées sur Internet sont potentiellement à risque.
*   Ivanti a publié des correctifs pour ces failles.

**Vulnérabilités :**
*   **CVE-2025-10573** : Exécution de code arbitraire via XSS stocké (nécessite interaction utilisateur).
*   **CVE-2025-13659** : Exécution de code arbitraire (nécessite interaction utilisateur).
*   **CVE-2025-13662** : Exécution de code arbitraire (nécessite interaction utilisateur).

**Recommandations :**
*   Appliquer immédiatement la mise à jour **EPM 2024 SU4 SR1** pour corriger CVE-2025-10573.
*   Appliquer les mises à jour de sécurité publiées pour corriger CVE-2025-13659 et CVE-2025-13662.
*   Éviter d'exposer les instances Ivanti EPM directement sur Internet.
*   Sensibiliser les administrateurs aux risques liés à l'interaction avec des environnements non fiables.

---
[Source](https://www.bleepingcomputer.com/news/security/ivanti-warns-of-critical-endpoint-manager-code-execution-flaw/){:target="_blank"}
