---
title: 'U.S. Senator accuses Microsoft of “gross cybersecurity negligence”'
date: 2025-09-12
permalink: /posts/2025/09/12/us-senator-accuses-microsoft-of-gross-cybersecurity-negligence/
tags:
- veille-cyber
- bleepingcomp
---
**Négligence de Microsoft en matière de cybersécurité : Accusations et risques pour la santé**

Le sénateur américain Ron Wyden a alerté la Federal Trade Commission (FTC) sur une "négligence grossière en matière de cybersécurité" de la part de Microsoft. Il demande une enquête suite à des attaques par ransomware visant des organisations de santé, notamment le piratage de données de 5,6 millions de patients chez Ascension Health en mai 2024.

L'attaque contre Ascension Health aurait été rendue possible par une technique appelée "Kerberoasting", exploitant des mots de passe faibles ou faciles à deviner, potentiellement chiffrés avec l'algorithme RC4, jugé obsolète et vulnérable. Cette méthode permet aux attaquants d'escalader leurs privilèges et de se déplacer latéralement sur les réseaux compromis.

Le sénateur reproche à Microsoft un manque de réactivité face aux risques de sécurité documentés, malgré des discussions avec son équipe en juillet 2024. Il déplore la réponse de Microsoft, jugée trop technique et insuffisamment claire pour les décideurs d'entreprise. L'utilisation persistante de l'algorithme RC4, bien qu'il soit une option, contribue à ces risques.

Wyden considère ces pratiques comme une menace sérieuse pour la sécurité nationale, craignant des incidents plus graves sans intervention de la FTC. Il souligne la position dominante de Microsoft sur le marché des systèmes d'exploitation d'entreprise comme facteur aggravant.

Microsoft, de son côté, affirme décourager l'usage de RC4, qui représente moins de 0,1% de son trafic, mais soutient qu'une désactivation complète pourrait perturber les systèmes de nombreux clients. L'entreprise travaille à sa suppression progressive et continue d'informer ses clients sur les meilleures pratiques d'utilisation de cet algorithme. Elle indique avoir l'intention de le désactiver à terme et reste en dialogue avec le bureau du sénateur.

**Points Clés :**

*   Accusation de "négligence grossière en matière de cybersécurité" contre Microsoft par le sénateur Ron Wyden.
*   Impact sur des organisations de santé, avec l'exemple de la brèche chez Ascension Health.
*   Exploitation d'une technique appelée "Kerberoasting" utilisant l'algorithme de chiffrement RC4, jugé obsolète.
*   Critique du manque de réactivité et de clarté de Microsoft face aux risques de sécurité.
*   Inquiétude quant à la sécurité nationale en raison des pratiques de Microsoft et de sa position sur le marché.
*   Réponse de Microsoft affirmant travailler à la suppression de RC4 tout en prenant en compte la compatibilité avec les systèmes existants.

**Vulnérabilités :**

*   **Kerberoasting :** Technique post-compromission permettant aux attaquants de voler des identifiants de compte de service chiffrés à partir de Microsoft Active Directory.
*   **Algorithme de chiffrement RC4 :** Jugé faible, obsolète et vulnérable, permettant la récupération d'informations en clair et facilitant le déchiffrement des mots de passe. Bien qu'il soit encore une option dans Kerberos, il est déconseillé en faveur d'algorithmes plus robustes comme AES 128/256. Aucune CVE spécifique n'est mentionnée dans l'article pour cette vulnérabilité directement liée à RC4, mais il est intrinsèquement une faiblesse.

**Recommandations :**

*   **Pour Microsoft :**
    *   Prendre des mesures décisives pour atténuer les risques de sécurité bien documentés dans ses produits.
    *   Alerter clairement les clients sur les dangers de l'utilisation de RC4.
    *   Rendre les algorithmes de chiffrement plus robustes (comme AES 128/256) la configuration par défaut.
    *   Accélérer la suppression de l'algorithme RC4 de ses systèmes.
*   **Pour les clients (organisations) :**
    *   Être vigilants face aux menaces de cybersécurité et à la sécurité des produits utilisés.
    *   Mettre à jour les protocoles et algorithmes de chiffrement vers des options plus sécurisées.
    *   Être attentifs aux recommandations de sécurité émises par les fournisseurs.

---
[Source](https://www.bleepingcomputer.com/news/security/us-senator-accuses-microsoft-of-gross-cybersecurity-negligence/){:target="_blank"}
