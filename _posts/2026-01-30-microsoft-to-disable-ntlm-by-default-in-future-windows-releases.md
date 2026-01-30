---
title: 'Microsoft to disable NTLM by default in future Windows releases'
date: 2026-01-30
permalink: /posts/2026/01/30/microsoft-to-disable-ntlm-by-default-in-future-windows-releases/
tags:
- veille-cyber
- bleepingcomp
---
**Abandon de NTLM pour une Sécurité Renforcée**

Microsoft désactivera par défaut le protocole d'authentification NTLM, vieux de 30 ans, dans les futures versions de Windows, en raison de ses vulnérabilités connues qui exposent les organisations aux cyberattaques. NTLM, bien que remplacé par Kerberos comme protocole d'authentification par défaut pour les appareils connectés à un domaine depuis Windows 2000, est toujours utilisé comme méthode de repli lorsque Kerberos n'est pas disponible.

Les faiblesses intrinsèques de NTLM ont été exploitées par diverses attaques, notamment les attaques par retransmission NTLM (NTLM relay attacks), permettant l'escalade de privilèges et le contrôle total du domaine Windows. Des vulnérabilités comme PetitPotam, ShadowCoerce, DFSCoerce et RemotePotato0 ont permis de contourner les mesures d'atténuation existantes. De plus, NTLM est une cible pour les attaques "pass-the-hash", où les pirates volent des hachages de mots de passe pour s'authentifier en tant qu'utilisateur compromis et se propager sur le réseau.

Dans le cadre d'une transition vers des méthodes d'authentification plus modernes et résistantes au phishing, Microsoft a annoncé un plan en trois phases pour abandonner NTLM par défaut.

**Points Clés:**

*   NTLM, protocole d'authentification ancien, présente des vulnérabilités significatives.
*   Kerberos est le protocole moderne et plus sécurisé, préféré par Microsoft.
*   L'abandon de NTLM vise à renforcer la sécurité des environnements Windows.

**Vulnérabilités (non exhaustive, sans CVE spécifiques mentionnées dans l'article):**

*   Attaques par retransmission NTLM (NTLM relay attacks) : Permettent l'escalade de privilèges et la prise de contrôle du domaine.
*   Exploitation de vulnérabilités telles que PetitPotam, ShadowCoerce, DFSCoerce, RemotePotato0.
*   Attaques "pass-the-hash" : Vol de hachages de mots de passe pour s'authentifier et se propager sur le réseau.

**Recommandations et Plan de Transition:**

*   **Phase 1 (actuelle, Windows 11 24H2 et Windows Server 2025) :** Mise à disposition d'outils d'audit améliorés pour identifier l'utilisation actuelle de NTLM.
*   **Phase 2 (second semestre 2026) :** Introduction de nouvelles fonctionnalités (IAKerb, Local Key Distribution Center) pour adresser les scénarios courants de repli vers NTLM.
*   **Phase 3 (futures versions) :** Désactivation par défaut de l'authentification NTLM sur le réseau. NTLM restera présent mais devra être explicitement réactivé via des contrôles de stratégie si nécessaire.
*   **Général :** Les administrateurs sont encouragés à migrer vers Kerberos ou l'authentification Negotiation et à configurer les serveurs pour bloquer les attaques par retransmission NTLM. Microsoft recommande aux développeurs d'arrêter d'utiliser NTLM dans leurs applications depuis 2010.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-to-disable-ntlm-by-default-in-future-windows-releases/){:target="_blank"}
