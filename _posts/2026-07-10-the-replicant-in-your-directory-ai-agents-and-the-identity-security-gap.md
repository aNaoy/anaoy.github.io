---
title: 'The Replicant in Your Directory: AI Agents and the Identity Security Gap'
date: 2026-07-10
permalink: /posts/2026/07/10/the-replicant-in-your-directory-ai-agents-and-the-identity-security-gap/
tags:
- veille-cyber
- bleepingcomp
---
### La menace invisible des identités non humaines et des agents IA

L'adoption massive des agents IA et des identités machines (comptes de service, jetons OAuth, applications) fragilise les systèmes de sécurité traditionnels, conçus exclusivement pour des utilisateurs humains. Ces identités « non humaines », souvent oubliées ou non répertoriées, dépassent désormais largement en nombre les comptes utilisateurs, créant une surface d'attaque en constante expansion.

**Points clés :**
*   **Inadaptation de la gouvernance :** Les processus de sécurité basés sur le cycle de vie humain (embauche, changement de poste, départ) sont inefficaces pour des machines qui prolifèrent, interagissent et créent d'autres identités à une vitesse dépassant la capacité de gestion humaine.
*   **Le danger de la confiance :** Le risque majeur ne réside pas dans l'exploitation d'une vulnérabilité logicielle, mais dans le détournement d'identités déjà « approuvées » (ex: jetons OAuth). Une fois qu'un attaquant compromet une identité machine de confiance, il peut facilement se déplacer latéralement pour accéder à des secrets et des données sensibles.
*   **Corrélation avec les incidents :** Les organisations qui déploient rapidement des agents IA voient leur taux de compromission bondir (43 % contre 11 % pour les autres), même lorsqu'elles disposent de pratiques de gouvernance rigoureuses.

**Vulnérabilités :**
*   L'article ne mentionne pas de CVE spécifique, mais met en évidence une vulnérabilité structurelle : **le détournement de jetons d'accès (OAuth/Service accounts)**, illustré par l'incident de 2025 lié au groupe **UNC6395**, où des jetons légitimes ont permis une intrusion à grande échelle via des intégrations tierces (Salesloft/Salesforce).

**Recommandations :**
*   **Inventaire continu :** Maintenir une visibilité en temps réel sur toutes les identités non humaines, leur origine et leurs propriétaires.
*   **Gestion du cycle de vie :** Définir systématiquement un propriétaire humain responsable pour chaque identité machine et automatiser leur révocation lorsqu'elles deviennent obsolètes.
*   **Contrôle des permissions :** Appliquer le principe du moindre privilège, même pour les agents IA, afin de limiter l'impact en cas de compromission d'une identité.
*   **Audit de gouvernance :** Évaluer régulièrement la maturité des pratiques de sécurité IA pour identifier les angles morts liés à la prolifération des identités machines.

---
[Source](https://www.bleepingcomputer.com/news/security/the-replicant-in-your-directory-ai-agents-and-the-identity-security-gap/){:target="_blank"}
