---
title: 'Friday Squid Blogging: Jumbo Flying Squid in the South Pacific'
date: 2026-03-21
permalink: /posts/2026/03/21/friday-squid-blogging-jumbo-flying-squid-in-the-south-pacific/
tags:
- veille-cyber
- schneier
---
### Vulnérabilité critique dans le logiciel fiscal H&R Block

Une faille de sécurité majeure a été identifiée dans la version 2025 du logiciel H&R Block Business. L'application installe une autorité de certification (CA) racine ("WK ATX ServerHost 2024") dans le magasin de certificats de confiance de la machine locale, tout en incluant la clé privée correspondante dans un fichier DLL.

**Points clés :**
* **Persistance :** Le certificat malveillant n'est pas supprimé lors de la désinstallation du logiciel.
* **Exploitation :** L'accès à la clé privée permet à un attaquant d'intercepter et de manipuler le trafic TLS chiffré (attaque de type Man-in-the-Middle) en utilisant des outils comme `mitmproxy` combinés à une usurpation DNS.
* **Absence de correctif :** Le fournisseur n'a pas encore répondu ou corrigé cette vulnérabilité.

**Recommandations :**
* **Isolation stricte :** Pour les opérations sensibles, utiliser une configuration informatique cloisonnée ("air-gapped"), séparant physiquement la machine effectuant les transactions privées de celle connectée à Internet.
* **Audit local :** Vérifier manuellement le magasin de certificats racine de Windows pour identifier et supprimer tout certificat suspect portant le nom "WK ATX ServerHost 2024".
* **Vigilance :** Éviter l'utilisation de logiciels tiers non essentiels sur les systèmes manipulant des données financières ou fiscales critiques tant qu'une mise à jour officielle n'a pas été déployée.

---
[Source](https://www.schneier.com/blog/archives/2026/03/friday-squid-blogging-jumbo-flying-squid-in-the-south-pacific.html){:target="_blank"}
