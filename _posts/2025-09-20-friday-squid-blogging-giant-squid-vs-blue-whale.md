---
title: 'Friday Squid Blogging: Giant Squid vs. Blue Whale'
date: 2025-09-20
permalink: /posts/2025/09/20/friday-squid-blogging-giant-squid-vs-blue-whale/
tags:
- veille-cyber
- schneier
---
### Sécurité des codes QR : une vulnérabilité intrinsèque

Les codes QR, conçus pour la lecture par machine et non par l'humain, présentent des faiblesses de sécurité inhérentes qui les rendent intrinsèquement moins sûrs que les URLs classiques. Contrairement aux URLs lisibles par l'homme, les codes QR ne possèdent pas de sécurité intégrée dans leur conception initiale. Cette absence de sécurité, combinée à leur nature non lisible par l'humain, ouvre la porte à des abus et à une surveillance accrue des utilisateurs.

**Points clés et vulnérabilités :**

*   **Absence de sécurité intrinsèque :** La conception même des codes QR ne prend pas en compte la sécurité, ce qui les rend vulnérables.
*   **Lisibilité par machine uniquement :** Le fait qu'ils ne soient pas directement lisibles par l'homme empêche une vérification humaine immédiate du contenu, ouvrant la voie à des manipulations.
*   **Canaux clandestins et surcharge d'informations :** Les codes QR peuvent contenir plus d'informations que ce qui est visible, permettant de dissimuler des données malveillantes ou des informations supplémentaires via des canaux clandestins. Chaque carré peut potentiellement représenter plusieurs bits de données, bien au-delà de la simple information affichée.
*   **Potentiel de "backdoor" :** Les lecteurs d'applications pour smartphones peuvent être conçus pour interagir avec ces canaux clandestins, créant des portes dérobées pour des attaquants, indépendamment de la sécurité du système d'exploitation.
*   **Risque de manipulation accrue :** L'utilisation croissante des codes QR, souvent motivée par la commodité, ne s'accompagne pas d'une sensibilisation égale aux risques, entraînant une augmentation disproportionnée des abus par rapport à la croissance de leur utilisation.

**Recommandations :**

*   **Implication humaine directe :** La seule manière de sécuriser l'utilisation des codes QR est de s'assurer que l'humain est entièrement impliqué dans la boucle d'authentification, et non pas remplacé par des intermédiaires numériques potentiellement compromis.
*   **Utilisation peu pratique mais sécurisée :** Privilégier une utilisation où l'humain doit manuellement entrer les informations via une séparation physique (air gapping) entre les appareils de communication et les points de sécurité. Cela implique souvent d'utiliser plusieurs appareils distincts et de saisir manuellement les données.
*   **Vigilance quant à l'affichage :** Les lecteurs de codes QR sur les smartphones doivent afficher clairement le contenu du code avant toute action (copier, envoyer, ouvrir une application) pour permettre à l'utilisateur de vérifier.
*   **Éviter la confiance aveugle :** Ne pas faire confiance implicitement aux applications ou aux systèmes qui lisent automatiquement les codes QR sans vérification préalable de l'utilisateur.

Il n'y a pas de vulnérabilités identifiées avec des identifiants CVE spécifiques dans le texte fourni.

---
[Source](https://www.schneier.com/blog/archives/2025/09/friday-squid-blogging-giant-squid-vs-blue-whale.html){:target="_blank"}
