---
title: 'CISA and NSA Issue Urgent Guidance to Secure WSUS and Microsoft Exchange Servers'
date: 2025-10-31
permalink: /posts/2025/10/31/cisa-and-nsa-issue-urgent-guidance-to-secure-wsus-and-microsoft-exchange-servers/
tags:
- veille-cyber
- hackernews
---
### Sécurisation Urgente des Serveurs Microsoft Exchange et WSUS

Les agences de cybersécurité américaines (CISA) et de sécurité nationale (NSA), en collaboration avec leurs homologues australiens et canadiens, ont émis des directives pour renforcer la sécurité des serveurs Microsoft Exchange locaux. Les instances mal configurées ou non protégées sont particulièrement ciblées par des activités malveillantes. Il est recommandé de démanteler les serveurs Exchange locaux obsolètes après leur migration vers Microsoft 365.

**Points Clés :**

*   Les serveurs Microsoft Exchange locaux sont vulnérables aux attaques.
*   Les vulnérabilités dans le service Windows Server Update Services (WSUS) sont activement exploitées.
*   Des acteurs de menace ciblent les organisations pour la collecte de données sensibles via ces vulnérabilités.

**Vulnérabilités :**

*   **CVE-2025-59287 :** Une faille de sécurité dans le composant WSUS de Windows Server permettant une exécution de code à distance.

**Recommandations :**

Pour les serveurs Microsoft Exchange :

*   Maintenir les mises à jour de sécurité et le rythme de patching.
*   Migrer les serveurs Exchange obsolètes.
*   Assurer l'activation du service d'atténuation d'urgence d'Exchange.
*   Appliquer et maintenir les bases de référence de sécurité pour Exchange, Windows et les clients de messagerie.
*   Activer les solutions antivirus, l'interface d'analyse antivirus de Windows (AMSI), la réduction de la surface d'attaque (ASR), AppLocker et App Control for Business, Endpoint Detection and Response, ainsi que les fonctionnalités anti-spam et anti-malware d'Exchange.
*   Restreindre l'accès administratif au centre d'administration d'Exchange (EAC) et à PowerShell distant en appliquant le principe du moindre privilège.
*   Renforcer l'authentification et le chiffrement en configurant TLS, HSTS, Extended Protection (EP), Kerberos et SMB au lieu de NTLM, et mettre en œuvre l'authentification multifacteur.
*   Désactiver l'accès à PowerShell distant pour les utilisateurs dans l'Exchange Management Shell (EMS).

Pour les serveurs WSUS et la vulnérabilité CVE-2025-59287 :

*   Identifier les serveurs susceptibles d'être exploités.
*   Appliquer la mise à jour de sécurité hors bande publiée par Microsoft.
*   Enquêter sur les signes d'activité des menaces sur les réseaux, notamment :
    *   Surveiller et vérifier les activités suspectes et les processus enfants lancés avec des autorisations de niveau SYSTEM, particulièrement ceux provenant de wsusservice.exe et/ou w3wp.exe.
    *   Surveiller et vérifier les processus PowerShell imbriqués utilisant des commandes PowerShell encodées en Base64.
*   S'assurer que les systèmes sont entièrement corrigés et que les serveurs WSUS sont configurés de manière sécurisée.

---
[Source](https://thehackernews.com/2025/10/cisa-and-nsa-issue-urgent-guidance-to.html){:target="_blank"}
