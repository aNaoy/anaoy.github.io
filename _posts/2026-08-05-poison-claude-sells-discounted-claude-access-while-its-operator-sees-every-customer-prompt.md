---
title: 'Poison Claude Sells Discounted Claude Access While Its Operator Sees Every Customer Prompt'
date: 2026-08-05
permalink: /posts/2026/08/05/poison-claude-sells-discounted-claude-access-while-its-operator-sees-every-customer-prompt/
tags:
- veille-cyber
- hackernews
---
### Risques de sécurité liés aux services de proxy pour modèles d'IA

Des chercheurs en cybersécurité ont identifié plusieurs plateformes illégales, telles que « Poison Claude », proposant un accès à prix réduit aux modèles de langage (LLM) d'Anthropic (Claude). Ces services exploitent les crédits promotionnels offerts par les plateformes cloud (comme AWS Bedrock) pour revendre des jetons d'accès à des tarifs largement inférieurs aux prix officiels.

**Points clés :**
*   **Mécanisme de proxy :** Ces services agissent comme des intermédiaires (Man-in-the-Middle). Les utilisateurs configurent leurs outils pour passer par une API tierce, qui relaie ensuite les requêtes vers le fournisseur légitime (Anthropic).
*   **Vol de données :** En utilisant ces proxys, les utilisateurs exposent la totalité de leurs invites (prompts) aux opérateurs du service, qui ont une visibilité complète sur les données transmises.
*   **Économie souterraine :** Ce marché gris répond à une forte demande, notamment dans les régions où ces modèles sont restreints ou bannis, facilitant également l'usage massif de bots et la création d'identités synthétiques via des essais gratuits détournés.

**Vulnérabilités :**
*   **Configuration exposée :** Des erreurs de configuration (ex: endpoints API mal protégés) permettent de divulguer des statistiques internes, comme le nombre d'utilisateurs actifs, confirmant l'ampleur de ces réseaux. (Aucune CVE spécifique n'est associée à ces pratiques, car il s'agit d'abus de service et de configurations défaillantes plutôt que d'une faille logicielle répertoriée).

**Recommandations :**
*   **Éviter les services tiers non officiels :** Ne jamais utiliser de clés API ou de services de proxy fournis par des sources douteuses, sous peine de compromettre la confidentialité des données traitées par l'IA.
*   **Utilisation des canaux officiels :** Passer exclusivement par les interfaces et API fournies directement par les éditeurs (Anthropic, OpenAI, etc.) pour garantir la sécurité des échanges et le respect des conditions d'utilisation.
*   **Surveillance des configurations :** Pour les développeurs, sécuriser rigoureusement les endpoints API pour éviter toute exposition d'informations sur l'usage des services.
*   **Sensibilisation :** Mettre en garde les utilisateurs contre la promesse d'économies, qui cache souvent un risque majeur de fuite de données sensibles ou de propriété intellectuelle.

---
[Source](https://thehackernews.com/2026/08/poison-claude-sells-discounted-claude.html){:target="_blank"}
