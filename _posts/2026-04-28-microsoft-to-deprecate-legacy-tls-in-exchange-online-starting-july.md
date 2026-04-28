---
title: 'Microsoft to deprecate legacy TLS in Exchange Online starting July'
date: 2026-04-28
permalink: /posts/2026/04/28/microsoft-to-deprecate-legacy-tls-in-exchange-online-starting-july/
tags:
- veille-cyber
- bleepingcomp
---
### Fin du support des protocoles TLS 1.0 et 1.1 pour Exchange Online

Microsoft a annoncé l'arrêt définitif de la prise en charge des versions obsolètes du protocole TLS (1.0 et 1.1) pour les connexions POP3 et IMAP4 dans Exchange Online, effectif à partir de juillet 2026. Cette mesure vise à renforcer la sécurité des communications en éliminant des protocoles cryptographiques vulnérables aux attaques par interception et falsification.

**Points clés :**
*   **Échéance :** Juillet 2026.
*   **Impact limité :** La majorité des clients de messagerie modernes utilisent déjà TLS 1.2 ou supérieur. Seuls les utilisateurs ayant explicitement activé les terminaux « legacy » seront impactés.
*   **Conséquence technique :** Toute tentative de connexion utilisant TLS 1.0 ou 1.1 échouera, provoquant l'interruption du service pour les applications ou appareils ne supportant pas les versions récentes.

**Vulnérabilités :**
Les versions TLS 1.0 et 1.1 sont jugées obsolètes et non sécurisées par l'industrie depuis plusieurs années. Bien qu'aucune CVE spécifique ne soit liée à cette annonce, ces protocoles sont intrinsèquement vulnérables à des attaques de type *network sniffing* (interception de données réseau) et ne répondent plus aux standards de sécurité actuels recommandés par les autorités (ex: NSA).

**Recommandations :**
*   **Audit de configuration :** Vérifier les paramètres des clients POP/IMAP pour s'assurer qu'ils sont configurés pour utiliser TLS 1.2 au minimum.
*   **Mise à jour des systèmes :** Mettre à jour les applications personnalisées, les systèmes embarqués et les périphériques utilisant des protocoles de messagerie vers des versions compatibles avec TLS 1.2+.
*   **Consultation des éditeurs :** En cas de doute sur la compatibilité, contacter les fournisseurs de solutions pour obtenir des conseils de mise à niveau.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-to-deprecate-legacy-tls-in-exchange-online-starting-july/){:target="_blank"}
