---
title: 'ChatGPT Agent - XSS on file://home/oai/redirect.html'
date: 2025-09-08
permalink: /posts/2025/09/08/chatgpt-agent-xss-on-filehomeoairedirecthtml/
tags:
- veille-cyber
- zerodaysfans
---
## Vulnérabilité XSS dans ChatGPT Agent

Le mode Agent de ChatGPT, qui utilise un navigateur dans une machine virtuelle distante, est affecté par une vulnérabilité de Cross-Site Scripting (XSS). Le fichier `file:///home/oai/redirect.html`, présent par défaut dans la VM, est vulnérable via son paramètre `target`.

**Points clés :**

*   La vulnérabilité permet de rediriger vers des URL `javascript:`, potentiellement dangereuses.
*   Le mode Agent peut être amené à ouvrir une URL `file://` en l'incluant dans une page web.

**Vulnérabilités exploitables :**

*   **XSSI (Cross-Site Script Inclusion) :** Si un fichier local sensible, dont le contenu est un script JavaScript valide, est chargé.
*   **Lecture de fichiers locaux via SpectreJS :** Des attaquants avancés peuvent utiliser SpectreJS pour lire n'importe quel fichier local en le chargeant comme sous-ressource (image, script, etc.).

**Recommandations :**

Bien que des versions corrigées existent, il est conseillé aux utilisateurs de s'assurer qu'ils utilisent la dernière version disponible du package ChatGPT Agent pour bénéficier des correctifs de sécurité.

---
[Source](https://github.com/google/security-research/security/advisories/GHSA-fhcg-rg39-8mv6){:target="_blank"}
