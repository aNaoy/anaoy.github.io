---
title: 'OpenAI is adding invisible watermarks to ChatGPT and Codex text in the EU'
date: 2026-10-06
permalink: /posts/2026/10/06/openai-is-adding-invisible-watermarks-to-chatgpt-and-codex-text-in-the-eu/
tags:
- veille-cyber
- bleepingcomp
---
### Implémentation du marquage invisible par OpenAI dans l'UE

OpenAI déploie progressivement la technologie « textGrain » au sein de l'Union européenne, visant à insérer des filigranes statistiques invisibles dans les textes générés par ChatGPT et Codex. Cette initiative, qui demeure optionnelle au niveau mondial pour les développeurs via API, cherche à renforcer la traçabilité des contenus générés par l'IA.

**Points clés :**
*   **Technologie :** Le système modifie subtilement le choix des mots pour créer une empreinte statistique détectable, sans altérer la qualité rédactionnelle.
*   **Accessibilité :** Le déploiement est prioritaire dans l'UE ; le détecteur de filigranes reste restreint à des chercheurs et organisations approuvés.
*   **Limites techniques :** La fiabilité de la détection diminue drastiquement avec l'édition humaine (remplacement de synonymes), la traduction, ou lorsque le texte est trop court.

**Vulnérabilités et limites :**
*   **Fragilité face à l'édition :** Une modification de seulement 25 % du texte fait chuter le taux de détection à 17 %.
*   **Défaut de preuve :** L'absence de filigrane détecté ne garantit nullement une paternité humaine.
*   **Incertitude contextuelle :** Le marquage ne permet pas d'identifier l'utilisateur, le compte associé ou le niveau d'intervention humaine dans le résultat final.
*   *Note : Aucune CVE n'est applicable, car il s'agit d'une limite conceptuelle et non d'une faille logicielle exploitable.*

**Recommandations :**
*   **Ne pas se fier exclusivement aux outils de détection :** Compte tenu de la volatilité du marquage face aux modifications simples, les organisations ne doivent pas utiliser ces outils comme une preuve formelle d'authenticité ou de fraude.
*   **Privilégier la vérification humaine :** Maintenir des processus de validation éditoriale indépendants pour les contenus critiques.
*   **Veille technologique :** Les développeurs utilisant l'API doivent évaluer si l'activation de `textGrain` apporte une valeur ajoutée réelle par rapport aux besoins spécifiques de conformité ou de sécurité de leurs applications.

---
[Source](https://www.bleepingcomputer.com/news/artificial-intelligence/openai-is-adding-invisible-watermarks-to-chatgpt-and-codex-text-in-the-eu/){:target="_blank"}
