---
title: 'Using Device Linking to Eavesdrop on WhatsApp and Signal'
date: 2026-09-29
permalink: /posts/2026/09/29/using-device-linking-to-eavesdrop-on-whatsapp-and-signal/
tags:
- veille-cyber
- schneier
---
### Surveillance par couplage d'appareils sur WhatsApp et Signal

La fonctionnalité permettant de lier un compte de messagerie (WhatsApp, Signal) à un ordinateur de bureau est détournée par les autorités pour contourner le chiffrement de bout en bout. En accédant au compte via une session liée, la police peut consulter les messages en temps réel sans avoir à casser le protocole de sécurité.

**Points clés :**
*   Le chiffrement des messages n'est pas brisé ; c'est le compte lui-même qui est dupliqué sur une machine contrôlée par les autorités.
*   L'opération nécessite une compromission initiale de l'appareil mobile ou du processus d'authentification.
*   Cette méthode permet une surveillance transparente et persistante des communications.

**Vecteurs d'attaque :**
*   **Accès physique :** Manipulation directe du téléphone cible pour scanner le code QR de couplage.
*   **Phishing :** Interception des codes de vérification via des campagnes de hameçonnage ciblées.
*   **Interception SMS :** Détournement des codes d'authentification via une surveillance des télécoms.
*(Note : Aucun identifiant CVE n'est associé à cette méthode, car il s'agit d'un détournement de fonctionnalité légitime et non d'une faille logicielle.)*

**Recommandations :**
*   **Audit de sécurité :** Vérifier régulièrement la liste des appareils connectés dans les paramètres de confidentialité de WhatsApp et Signal.
*   **Suppression proactive :** Révoquer immédiatement tout accès sur les appareils ou sessions inconnus.
*   **Sécurisation physique :** Verrouiller l'accès au téléphone par un code robuste ou une authentification biométrique pour empêcher le scan non autorisé de codes QR.

---
[Source](https://www.schneier.com/blog/archives/2026/09/using-device-linking-to-eavesdrop-on-whatsapp-and-signal.html){:target="_blank"}
