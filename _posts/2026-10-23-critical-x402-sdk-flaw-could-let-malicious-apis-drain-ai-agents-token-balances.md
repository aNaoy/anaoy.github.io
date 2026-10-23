---
title: 'Critical x402 SDK Flaw Could Let Malicious APIs Drain AI Agents’ Token Balances'
date: 2026-10-23
permalink: /posts/2026/10/23/critical-x402-sdk-flaw-could-let-malicious-apis-drain-ai-agents-token-balances/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans le SDK x402 : Risques pour les agents IA

Le SDK x402, utilisé par les agents IA pour automatiser les paiements d'API, présentait trois vulnérabilités critiques corrigées le 18 août 2024. Bien qu'aucune exploitation n'ait été signalée, l'absence d'avis de sécurité officiels laisse de nombreux utilisateurs exposés.

**Points clés :**
* **Absence de limite de dépenses :** Par défaut, le client acceptait les demandes de paiement sans plafond, permettant à une API malveillante de vider le portefeuille d'un agent.
* **Contournement de paiement (Solana) :** Le code TypeScript acceptait les « approbations de jetons » comme des paiements valides, permettant d'accéder à des ressources sans transfert réel de fonds.
* **Usurpation d'identité (SIWx) :** L'extension de connexion signait des messages pour des sites tiers sans vérifier que le domaine correspondait à celui de l'API contactée.

**Vulnérabilités :**
* Aucune CVE n'a été assignée par la fondation x402. La gestion des correctifs a été traitée via des mises à jour standard sans signalement de sécurité explicite dans les journaux de modifications.

**Recommandations :**
* **Mise à jour immédiate :** Passer aux versions 2.28.0 (ou supérieures) pour les paquets TypeScript, Go et Python.
* **Configuration des contrôles :** Les nouvelles versions imposent par défaut un plafond de 1 $ et restreignent les paiements aux stablecoins reconnus. Il est conseillé de ne pas désactiver ces contrôles (`spendControls: false`).
* **Validation des messages :** Pour les implémentations personnalisées, vérifier systématiquement que le message de connexion (SIWx) identifie correctement le site contacté avant toute signature.
* **Politique de dépenses :** En cas d'impossibilité de mise à jour, implémenter manuellement une politique de dépenses via `registerPolicy` pour limiter les montants, les jetons et les destinataires autorisés.

---
[Source](https://thehackernews.com/2026/10/critical-x402-sdk-flaw-could-let.html){:target="_blank"}
