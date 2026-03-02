---
title: 'Google Develops Merkle Tree Certificates to Enable Quantum-Resistant HTTPS in Chrome'
date: 2026-03-02
permalink: /posts/2026/03/02/google-develops-merkle-tree-certificates-to-enable-quantum-resistant-https-in-chrome/
tags:
- veille-cyber
- hackernews
---
**Sécurisation du Web face à l'Ère Quantique**

Google travaille à l'intégration de certificats basés sur les arbres de Merkle (Merkle Tree Certificates - MTC) dans le navigateur Chrome afin de garantir la sécurité des connexions HTTPS face à la menace future des ordinateurs quantiques. Cette approche vise à rendre les certificats plus efficaces et évolutifs que les certificats X.509 traditionnels dans un contexte post-quantique.

**Points Clés :**

*   La menace des ordinateurs quantiques pourrait compromettre les méthodes de chiffrement actuelles utilisées pour sécuriser les communications sur Internet.
*   Les certificats X.509 classiques, qui contiennent des informations volumineuses, pourraient devenir moins efficaces avec l'adoption de cryptographie post-quantique.
*   Les MTC permettent à une autorité de certification de signer un "arbre de tête" unique, représentant potentiellement des millions de certificats.
*   Le certificat envoyé au navigateur devient une preuve légère d'inclusion dans cet arbre, réduisant ainsi la quantité de données échangées lors de la négociation TLS (Transport Layer Security).
*   Cette méthode découple la force du chiffrement de la taille des données transmises, maintenant ainsi des performances élevées même avec des algorithmes post-quantiques plus robustes.

**Vulnérabilités (non spécifiées dans l'article) :**

L'article ne mentionne pas de vulnérabilités spécifiques (CVE) car il traite d'une nouvelle technologie préventive plutôt que d'une faille existante. La menace principale évoquée est la puissance future des ordinateurs quantiques qui rendra obsolètes les algorithmes de chiffrement actuels, y compris ceux utilisés dans les certificats X.509.

**Recommandations :**

*   **Évolution des Certificats :** Adoption des Merkle Tree Certificates (MTC) pour une infrastructure à clé publique (PKI) de nouvelle génération.
*   **Optimisation des Données :** Réduction au minimum des clés publiques et des signatures lors de la négociation TLS.
*   **Déploiement Progressif :** Le déploiement des MTC dans Chrome se fera en trois phases, avec une étude de faisabilité en cours, une phase d'invitation pour les opérateurs de logs de transparence des certificats en 2027, et la finalisation des exigences pour l'intégration de nouvelles autorités de certification en 2027.
*   **Robustesse de l'Écosystème :** Préparation de l'écosystème Web à la résilience post-quantique pour assurer la sécurité des utilisateurs.

---
[Source](https://thehackernews.com/2026/03/google-develops-merkle-tree.html){:target="_blank"}
