---
title: 'RubyGems, PyPI Hit by Malicious Packages Stealing Credentials, Crypto, Forcing Security Changes'
date: 2025-08-08
permalink: /posts/2025/08/08/rubygems-pypi-hit-by-malicious-packages-stealing-credentials-crypto-forcing-security-changes/
tags:
- veille-cyber
- hackernews
---
### Vampirisme de données et de cryptomonnaies dans les dépôts de paquets

Deux campagnes distinctes ont été révélées, visant respectivement les écosystèmes RubyGems et PyPI, avec pour objectif principal le vol d'informations sensibles.

**Campagne RubyGems :**

*   **Cible :** Plus de 60 paquets malveillants ont été découverts dans RubyGems, se faisant passer pour des outils d'automatisation pour les réseaux sociaux, le blogging et la messagerie (Instagram, Twitter/X, TikTok, WordPress, Telegram, Kakao, Naver).
*   **Méthode :** Ces paquets, actifs depuis au moins mars 2023, dérobent des identifiants (noms d'utilisateur et mots de passe) via une interface graphique utilisateur lorsqu'ils sont utilisés pour des tâches comme la publication en masse ou l'engagement. Certains paquets ciblaient spécifiquement les plateformes de discussion financière pour manipuler la perception publique.
*   **Infrastructure :** Les données exfiltrées sont envoyées à des serveurs tels que `programzon[.]com`, `appspace[.]kr`, et `marketingduo[.]co[.]kr`.
*   **Victimes probables :** Des professionnels du marketing ("grey-hats") utilisant ces outils pour des campagnes de spam, de SEO et d'engagement artificiel. L'opération semble mature, évoluant avec plusieurs alias et vagues d'infrastructure, et cible principalement les utilisateurs sud-coréens.
*   **Points clés :**
    *   Plus de 275 000 téléchargements cumulés pour les paquets compromis.
    *   Ciblage de données d'authentification et potentiellement d'informations financières.
    *   Utilisation d'interfaces utilisateur en coréen et d'exfiltration vers des domaines `.kr`.

**Campagne PyPI :**

*   **Cible :** Plusieurs paquets "typosquatting" ont été détectés sur le Python Package Index (PyPI), imitant les noms de bibliothèques légitimes comme `bittensor` et `bittensor-cli`.
*   **Méthode :** Ces paquets sont conçus pour voler des cryptomonnaies des portefeuilles Bittensor en détournant les fonctions légitimes de "staking" (délégation de puissance de calcul). Le code malveillant est dissimulé dans des fonctionnalités d'apparence légitime.
*   **Points clés :**
    *   Exemples de noms de paquets malveillants : `bitensor` (versions 9.9.4 et 9.9.5), `bittenso-cli`, `qbittensor`, `bittenso`.
    *   Ciblage spécifique des opérations de staking pour des raisons stratégiques.

**Mesures de sécurité PyPI :**

En réponse à ces menaces, PyPI a implémenté de nouvelles restrictions :

*   **Rejet des paquets "wheels" malveillants :** Les paquets exploitant des vulnérabilités de confusion des analyseurs ZIP pour introduire des charges utiles malveillantes seront rejetés. Cela fait suite à la découverte que certains outils d'installation ont un comportement d'extraction différent de celui de la bibliothèque standard `zipfile`.
*   **Avertissements pour les métadonnées incohérentes :** PyPI avertira les utilisateurs qui publient des paquets dont le contenu ZIP ne correspond pas au fichier métadonnées `RECORD` inclus.
*   **Rejet futur basé sur les métadonnées :** À partir du 1er février 2026, PyPI commencera à rejeter les nouveaux paquets "wheels" dont le contenu ZIP ne correspondra pas aux métadonnées `RECORD`.

**Recommandations :**

*   **Vigilance accrue lors de l'installation de paquets :** Examiner attentivement le nom des paquets avant l'installation, en particulier pour les bibliothèques liées à la finance, aux réseaux sociaux ou à l'automatisation.
*   **Vérification de la légitimité des paquets :** S'assurer que les paquets proviennent de sources fiables et que leurs descriptions correspondent à leur fonctionnalité réelle.
*   **Mise à jour régulière des outils de développement :** Maintenir à jour les environnements de développement et les gestionnaires de paquets pour bénéficier des dernières correctifs de sécurité.
*   **Prudence avec les fonctions d'automatisation :** Être particulièrement prudent avec les outils promettant une automatisation avancée, car ils peuvent être utilisés pour dissimuler des fonctionnalités malveillantes.
*   **Sécurisation des portefeuilles de cryptomonnaies :** Utiliser des méthodes d'authentification fortes et être vigilant quant aux opérations de staking ou de délégation impliquant des actifs numériques.

---
[Source](https://thehackernews.com/2025/08/rubygems-pypi-hit-by-malicious-packages.html){:target="_blank"}
