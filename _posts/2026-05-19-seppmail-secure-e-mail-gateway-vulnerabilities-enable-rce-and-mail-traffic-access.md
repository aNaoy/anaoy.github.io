---
title: 'SEPPMail Secure E-Mail Gateway Vulnerabilities Enable RCE and Mail Traffic Access'
date: 2026-05-19
permalink: /posts/2026/05/19/seppmail-secure-e-mail-gateway-vulnerabilities-enable-rce-and-mail-traffic-access/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités critiques dans la passerelle de messagerie SEPPMail

Des chercheurs d'InfoGuard Labs ont identifié une série de vulnérabilités critiques affectant la passerelle de messagerie sécurisée SEPPMail. Ces failles permettent à un attaquant non authentifié d'exécuter du code à distance (RCE), d'accéder à l'ensemble du trafic de messagerie ou de s'introduire dans le réseau interne.

**Points clés :**
*   L'exploitation combinée de ces vulnérabilités peut mener à une prise de contrôle totale de l'appliance.
*   Certaines attaques peuvent être automatisées en forçant la rotation des logs (via l'envoi massif de requêtes web) pour déclencher le rechargement d'une configuration malveillante.
*   Les vulnérabilités touchent principalement les interfaces web de l'appliance.

**Vulnérabilités majeures :**
*   **CVE-2026-2743 (CVSS 10.0) :** Path traversal permettant l'écriture arbitraire de fichiers et une RCE.
*   **CVE-2026-44125 (CVSS 9.3) :** Absence de contrôle d'autorisation dans la nouvelle interface GINA.
*   **CVE-2026-44128 (CVSS 9.3) :** Injection de code via une fonction `eval()` non sécurisée.
*   **CVE-2026-44126 (CVSS 9.2) :** Désérialisation de données non fiables permettant l'exécution de code.
*   **CVE-2026-44127 (CVSS 8.8) :** Lecture arbitraire de fichiers locaux et suppression de fichiers.
*   **CVE-2026-44129 (CVSS 8.3) :** Injection d'expressions dans le moteur de template.
*   **CVE-2026-7864 (CVSS 6.9) :** Fuite d'informations sensibles sur l'environnement serveur.

**Recommandations :**
*   Mettre à jour immédiatement l'appliance SEPPMail vers la **version 15.0.4 ou supérieure**, celle-ci incluant les correctifs pour l'ensemble des vulnérabilités mentionnées.
*   Surveiller les logs système pour détecter toute activité suspecte ou tentative de manipulation de la configuration syslog.

---
[Source](https://thehackernews.com/2026/05/seppmail-secure-e-mail-gateway.html){:target="_blank"}
