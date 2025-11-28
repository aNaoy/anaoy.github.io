---
title: 'Legacy Python Bootstrap Scripts Create Domain-Takeover Risk in Multiple PyPI Packages'
date: 2025-11-28
permalink: /posts/2025/11/28/legacy-python-bootstrap-scripts-create-domain-takeover-risk-in-multiple-pypi-packages/
tags:
- veille-cyber
- hackernews
---
**Vulnérabilités dans les scripts de démarrage Python : Risque de prise de contrôle de domaine**

Des scripts de démarrage obsolètes utilisés dans certains paquets PyPI, liés à l'outil de gestion de projet zc.buildout, présentent un risque significatif de sécurité. Ces scripts tentent de télécharger le paquet "Distribute" depuis le domaine `python-distribute[.]org`. Ce domaine, inactif depuis 2014 et désormais disponible à la vente, pourrait être acquis par un attaquant.

**Points clés :**

*   **Vecteur d'attaque :** La vulnérabilité réside dans l'utilisation de scripts de démarrage hérités qui référencent un domaine obsolète et potentiellement compromettable.
*   **Mécanisme d'exploitation :** Un attaquant pourrait acquérir le domaine `python-distribute[.]org` et y héberger du code malveillant. Lorsque le script de démarrage est exécuté, il téléchargerait et exécuterait ce code, ouvrant la voie à une compromission de la chaîne d'approvisionnement logicielle.
*   **Paquets affectés :** Des paquets tels que tornado, pypiserver, slapos.core, roman, xlutils et testfixtures incluent potentiellement ces scripts vulnérables. Slapos.core et une version de développement de Tornado sont explicitement mentionnés comme contenant toujours ce code.
*   **Nature de la vulnérabilité :** Il s'agit d'un risque de prise de contrôle de domaine (domain takeover), où le contrôle d'un domaine inactif peut être utilisé pour distribuer des charges utiles malveillantes.
*   **Contexte :** Le paquet "Distribute" était un fork temporaire de Setuptools et est devenu obsolète en 2013. L'utilisation continue des anciens scripts de démarrage qui tentent de l'installer crée une surface d'attaque inutile.
*   **Python 2 et absence d'exécution automatique :** Le script de démarrage étant écrit en Python 2, il ne s'exécute pas avec Python 3 sans modification, et il n'est pas lancé automatiquement lors de l'installation du paquet. Cependant, sa simple présence constitue une faille si les développeurs sont amenés à exécuter le script, intentionnellement ou non.
*   **Parallèle avec npm :** Un exemple antérieur de ce type d'attaque a été observé dans l'écosystème npm avec le paquet fsevents (CVE-2023-45311).

**Vulnérabilités :**

*   Aucune CVE spécifique n'est mentionnée pour la vulnérabilité des scripts de démarrage zc.buildout eux-mêmes. Cependant, la méthode d'attaque par prise de contrôle de domaine est une menace reconnue, illustrée par le cas CVE-2023-45311.

**Recommandations :**

*   **Mettre à jour les dépendances :** Les développeurs utilisant des versions obsolètes de paquets susceptibles de contenir ces scripts devraient les mettre à jour vers des versions nettoyées.
*   **Supprimer les scripts de démarrage obsolètes :** Les mainteneurs de paquets devraient activement examiner et supprimer les scripts de démarrage `bootstrap.py` qui dépendent de domaines inactifs ou obsolètes.
*   **Vérifier la sécurité de la chaîne d'approvisionnement :** Les organisations doivent renforcer leurs pratiques de sécurité pour la chaîne d'approvisionnement logicielle afin de détecter et de prévenir l'intégration de composants vulnérables.
*   **Éviter l'exécution de scripts de démarrage non fiables :** Les développeurs doivent être prudents quant à l'exécution de scripts de démarrage provenant de sources potentiellement non fiables ou obsolètes.

---
[Source](https://thehackernews.com/2025/11/legacy-python-bootstrap-scripts-create.html){:target="_blank"}
