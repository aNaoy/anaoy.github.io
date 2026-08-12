---
title: 'Signal adds new security feature to thwart man-in-the-middle attacks'
date: 2026-08-12
permalink: /posts/2026/08/12/signal-adds-new-security-feature-to-thwart-man-in-the-middle-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Signal renforce la sécurité des échanges par la vérification automatique des clés

Signal déploie une nouvelle fonctionnalité de « transparence des clés » visant à prévenir les attaques de type « homme du milieu » (MitM). Ce système automatise la vérification de l'intégrité des clés de chiffrement en s'appuyant sur des auditeurs tiers indépendants (Cloudflare et Trail of Bits), garantissant que la clé publique associée à un utilisateur n'a pas été modifiée à son insu par une entité malveillante.

**Points clés :**
*   **Transparence des clés :** Le système assure une cohérence mondiale des clés de chiffrement sans nécessiter de rencontre physique ou de canal de communication secondaire, contrairement à la vérification manuelle des numéros de sécurité.
*   **Indépendance :** La vérification repose sur une approche distribuée impliquant l'utilisateur, ses contacts et des auditeurs tiers.
*   **Interface utilisateur :** Une validation réussie affiche un indicateur visuel (coche verte et message « Chiffrement vérifié »).
*   **Flexibilité :** Les utilisateurs peuvent désactiver cette option dans les paramètres de confidentialité pour conserver uniquement la méthode de vérification manuelle.

**Vulnérabilités adressées :**
*   **Attaques de type Man-in-the-Middle (MitM) :** L'usurpation d'identité via l'échange frauduleux de clés de chiffrement, notamment en cas de compromission des serveurs de Signal par des acteurs malveillants. 
*   *Note : Aucune CVE spécifique n'est associée, cette mise à jour étant une amélioration proactive de l'architecture de sécurité plutôt qu'un correctif logiciel.*

**Recommandations :**
*   **Activation :** Activer la fonctionnalité via le menu *Paramètres > Confidentialité > Avancé > Vérification automatique des clés*.
*   **Vigilance :** Bien que ce système protège contre l'interception, il est recommandé de rester vigilant face aux campagnes de phishing et d'ingénierie sociale (notamment les fausses alertes « Support Signal ») qui ciblent les comptes via l'abus de la fonction « Appareils associés ».

---
[Source](https://www.bleepingcomputer.com/news/security/signal-adds-new-security-feature-to-thwart-man-in-the-middle-attacks/){:target="_blank"}
