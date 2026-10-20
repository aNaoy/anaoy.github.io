---
title: 'Eight eMudhra CA Keys Compromised, Triggering Emergency Fixes Across Browsers and Software'
date: 2026-10-20
permalink: /posts/2026/10/20/eight-emudhra-ca-keys-compromised-triggering-emergency-fixes-across-browsers-and-software/
tags:
- veille-cyber
- hackernews
---
### Compromission des clés privées de l'autorité de certification eMudhra

Huit clés privées appartenant à des autorités de certification (CA) intermédiaires de l'entreprise indienne eMudhra ont été compromises, permettant théoriquement l'émission frauduleuse de certificats TLS/SSL valides. Cette faille majeure a nécessité des mesures d'urgence de la part des principaux navigateurs et éditeurs de logiciels pour protéger l'intégrité des connexions sécurisées.

**Points clés :**
* **Portée :** La compromission concerne huit certificats (TLS, signature de code, DV/OV/EV) de la marque *emSign*.
* **Réaction rapide :** Mozilla et Google Chrome ont bloqué ces certificats via des listes de révocation (OneCRL et CRLSet) quelques heures après le signalement le 17 octobre.
* **Impact :** Aucun certificat TLS n'ayant été consigné dans les journaux de transparence (Certificate Transparency) avant le blocage, le risque d'exploitation malveillante en ligne semble limité.
* **Conséquences pour eMudhra :** La confiance envers l'autorité *emSign ECC Root CA - G3* est révoquée ; son retrait des magasins racines est en cours par les principaux éditeurs.

**Vulnérabilités identifiées :**
* **CVE-2026-111943 :** Vulnérabilité dans le langage Go permettant l'acceptation de chaînes de certificats compromises.
* **CVE-2026-113470 :** Problème de sécurité dans Firefox nécessitant une mise à jour pour inclure les blocages de révocation hors ligne.

**Recommandations :**
* **Mise à jour immédiate :** Appliquer les correctifs publiés par les éditeurs pour les bibliothèques et logiciels utilisant des magasins de certificats (Go 1.27.3/1.26.10, Firefox 158.0.1, NSS 3.131.1, Python `certifi` 2026.10.19, etc.).
* **Vérification des infrastructures :** Pour les opérateurs de systèmes, s'assurer que les logiciels vérifient activement les listes de révocation. Lorsque ce n'est pas possible, procéder manuellement au retrait de confiance des racines *emSign* concernées dans les magasins de certificats locaux.
* **Surveillance :** Rester en attente des communications officielles d'eMudhra sur la cause racine de l'incident, les circonstances de la fuite des clés restant à ce jour inconnues.

---
[Source](https://thehackernews.com/2026/10/eight-emudhra-ca-keys-compromised.html){:target="_blank"}
