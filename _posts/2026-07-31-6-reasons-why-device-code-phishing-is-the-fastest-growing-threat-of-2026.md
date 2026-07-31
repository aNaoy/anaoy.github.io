---
title: '6 Reasons Why Device Code Phishing is the Fastest-Growing Threat of 2026'
date: 2026-07-31
permalink: /posts/2026/07/31/6-reasons-why-device-code-phishing-is-the-fastest-growing-threat-of-2026/
tags:
- veille-cyber
- hackernews
---
### L'essor fulgurant du phishing par code de périphérique (Device Code Phishing)

Le phishing par "Device Code" est devenu une menace industrielle majeure en 2026. En exploitant le flux d'autorisation OAuth 2.0 (initialement prévu pour les appareils sans clavier comme les smart TV ou les imprimantes), les attaquants parviennent à voler des jetons d'accès en contournant toutes les protections classiques.

**Points clés :**
*   **Contournement total de l'authentification :** L'attaque cible la couche d'autorisation et non l'authentification elle-même. Par conséquent, les clés de sécurité (Passkeys), la MFA traditionnelle et même les méthodes de MFA résistantes au phishing sont inefficaces.
*   **Industrialisation via le PhaaS :** Des kits de "Phishing-as-a-Service" (PaaS) comme *EvilTokens*, *Tycoon2FA* ou *Kali365* intègrent désormais cette technique, facilitant son adoption à grande échelle.
*   **Facilité de création :** L'utilisation de l'IA générative permet aux attaquants de concevoir de nouveaux kits rapidement, rendant la détection basée sur les signatures (IOC) obsolète.
*   **Au-delà de Microsoft :** Bien que 99 % des attaques visent actuellement Microsoft, le protocole OAuth 2.0 étant un standard, les services comme AWS, GitHub ou Salesforce sont des cibles logiques et vulnérables.
*   **Déplacement de la menace :** Les attaquants se détournent de la couche d'authentification (trop protégée) pour cibler les mécanismes d'autorisation et les flux de consentement (ex: *ConsentFix*).

**Vulnérabilités :**
*   Abus du flux **OAuth 2.0 Device Authorization Grant**.
*   Absence de protection spécifique sur les mécanismes de consentement et d'autorisation après authentification réussie.
*   *Note : Aucune CVE spécifique n'est mentionnée, car il s'agit d'un abus de conception légitime du protocole OAuth et non d'une faille logicielle isolée.*

**Recommandations :**
*   **Politiques d'accès conditionnel :** Restreindre les flux d'autorisation par code de périphérique dans les environnements Microsoft lorsque cela est possible sans perturber les outils métier.
*   **Surveillance au niveau du navigateur :** La protection doit se situer au niveau du navigateur (point de visibilité unique du flux d'approbation et du leurre), car les proxies réseau et passerelles email ne peuvent pas bloquer l'accès à une URL légitime utilisée lors de l'attaque.
*   **Changement de paradigme :** Passer d'une détection basée sur les indicateurs de compromission (IOC) vers une détection comportementale axée sur les signatures des kits de phishing et le processus d'approbation lui-même.

---
[Source](https://thehackernews.com/2026/07/6-reasons-why-device-code-phishing-is.html){:target="_blank"}
