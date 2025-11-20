---
title: 'GlobalProtect VPN portals probed with 2.3 million scan sessions'
date: 2025-11-20
permalink: /posts/2025/11/20/globalprotect-vpn-portals-probed-with-23-million-scan-sessions/
tags:
- veille-cyber
- bleepingcomp
---
**Recrudescence des sondages sur les portails VPN GlobalProtect**

Une campagne coordonnée de sondages malveillants visant les portails de connexion VPN GlobalProtect de Palo Alto Networks a connu une augmentation spectaculaire. En seulement 24 heures, l'activité a été multipliée par 40, atteignant un pic inédit sur 90 jours. Sur une période de cinq jours, 2,3 millions de sessions ont été détectées ciblant le point d'accès `*/global-protect/login.esp`, qui correspond à la page d'authentification des utilisateurs VPN.

Les tentatives de connexion sont principalement dirigées vers les États-Unis, le Mexique et le Pakistan. Les analyses montrent un lien entre cette activité et des campagnes antérieures, grâce à des empreintes TCP/JA4t récurrentes et à la réutilisation des mêmes numéros de système autonome (ASN). Les principaux ASN identifiés sont AS200373 (3xK Tech GmbH), avec une prédominance d'adresses IP géolocalisées en Allemagne et au Canada, et AS208885 (Noyobzoda Faridduni Saidilhom).

Cette intensification des sondages est particulièrement préoccupante car elle précède fréquemment la divulgation de nouvelles vulnérabilités de sécurité. Les données indiquent que dans 80% des cas, ces pics d'activité malveillante sont suivis par la publication de failles, une corrélation encore plus forte pour les produits Palo Alto Networks. L'article mentionne également des exploitations actives de vulnérabilités telles que CVE-2025-0108, combinée avec CVE-2025-0111 et CVE-2024-9474 en février, ainsi qu'une violation de données révélée en septembre.

**Points Clés :**

*   Augmentation de 40x en 24h de l'activité de sondage malveillant sur les portails VPN GlobalProtect.
*   2,3 millions de sessions enregistrées entre le 14 et le 19 novembre ciblant le point d'accès `/global-protect/login.esp`.
*   Concentration des attaques sur les États-Unis, le Mexique et le Pakistan.
*   Lien établi avec des campagnes antérieures via des indicateurs techniques et temporels.
*   Les sondages malveillants précèdent souvent la divulgation de nouvelles vulnérabilités de sécurité.

**Vulnérabilités Mentionnées :**

*   CVE-2025-0108
*   CVE-2025-0111
*   CVE-2024-9474

**Recommandations Implicites :**

*   Surveiller activement et bloquer les tentatives de sondage malveillant sur les portails VPN GlobalProtect, car elles peuvent indiquer une exploitation imminente de vulnérabilités.
*   Maintenir les systèmes à jour et appliquer les correctifs de sécurité dès leur publication pour atténuer les risques associés aux failles connues ou nouvellement découvertes.

---
[Source](https://www.bleepingcomputer.com/news/security/globalprotect-vpn-portals-probed-with-23-million-scan-sessions/){:target="_blank"}
