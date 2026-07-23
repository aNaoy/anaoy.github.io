---
title: 'Microsoft working to fix Exchange Online mailbox quarantine issue'
date: 2026-07-23
permalink: /posts/2026/07/23/microsoft-working-to-fix-exchange-online-mailbox-quarantine-issue/
tags:
- veille-cyber
- bleepingcomp
---
### Dysfonctionnement majeur : Mise en quarantaine erronée des boîtes Exchange Online

Microsoft fait face à un incident technique persistant (référencé **EX1436407**) provoquant la mise en quarantaine injustifiée de boîtes aux lettres Exchange Online, empêchant ainsi l'envoi et la réception de courriels ainsi que l'accès aux calendriers.

**Points clés :**
* **Origine du problème :** Une modification récente de l'infrastructure a engendré une consommation excessive de mémoire vive (condition *out-of-memory*) liée à des données d'indexation inattendues.
* **Récurrence :** Il s'agit d'une résurgence d'un incident précédent (référencé **EX1434354**), nécessitant des mesures correctives supplémentaires.
* **État actuel :** Microsoft procède au nettoyage des données d'indexation excédentaires. Environ 72 % du processus était complété mercredi soir, avec une restauration progressive de l'accès aux boîtes aux lettres.

**Vulnérabilités :**
* Aucun numéro CVE n'est associé à cet incident, car il s'agit d'une défaillance logicielle et infrastructurelle interne et non d'une faille de sécurité exploitée par des tiers.

**Recommandations :**
* **Pour les administrateurs :** Il n'existe pas d'action corrective côté client. Il est conseillé de surveiller le centre d'administration Microsoft (Microsoft 365 Admin Center) pour les mises à jour en temps réel sur l'incident **EX1436407**.
* **Communication interne :** Informer les utilisateurs impactés que le problème est identifié et en cours de résolution par Microsoft afin d'éviter des tickets de support inutiles auprès des équipes informatiques locales.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-working-to-fix-exchange-online-mailbox-quarantine-issue/){:target="_blank"}
