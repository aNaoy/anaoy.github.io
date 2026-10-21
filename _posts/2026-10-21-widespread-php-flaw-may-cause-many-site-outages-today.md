---
title: 'Widespread PHP Flaw May Cause Many Site Outages Today'
date: 2026-10-21
permalink: /posts/2026/10/21/widespread-php-flaw-may-cause-many-site-outages-today/
tags:
- veille-cyber
- krebs
---
### Alerte critique : Vulnérabilités majeures dans le langage PHP

Une faille critique affectant le langage PHP, omniprésent sur le Web, a été révélée, entraînant des pannes sur de nombreux sites. Ces vulnérabilités, découvertes avec l'aide de modèles d'IA, permettent à un attaquant de prendre le contrôle total des serveurs via l'exécution de code à distance (RCE). 

**Points clés :**
* **Impact massif :** Environ 70 % des sites web sont potentiellement vulnérables. Toutes les versions de PHP depuis 10 ans sont concernées, incluant des plateformes comme WordPress, Drupal, Magento et Joomla.
* **Exploitation active :** Des preuves d'exploitation sont déjà détectées « dans la nature ». Les experts comparent la gravité de cet incident à la vulnérabilité Log4Shell.
* **Risques :** Exécution de code arbitraire, installation de portes dérobées (web shells), déni de service et exposition de données sensibles.

**Vulnérabilités :**
* **CVE-2026-109618**
* **CVE-2026-109619**

**Recommandations :**
* **Mise à jour immédiate :** Appliquer sans délai les correctifs de sécurité fournis par PHP. Les versions corrigées sont : **8.5.12, 8.4.27, 8.3.36 et 8.2.35**.
* **Surveillance :** Inspecter les journaux de serveurs à la recherche de comportements anormaux ou de signes d'installation de web shells.
* **Protection périmétrique :** Utiliser des règles de pare-feu applicatif (WAF) pour filtrer les tentatives d'exploitation connues en attendant la mise à jour des environnements.

---
[Source](https://krebsonsecurity.com/2026/10/widespread-php-flaw-may-cause-many-site-outages-today/){:target="_blank"}
