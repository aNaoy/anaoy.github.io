---
title: 'Microsoft Patch Tuesday July 2026 - The AI Acopolypse is Here , (Tue, Jul 14th)'
date: 2026-07-15
permalink: /posts/2026/07/15/microsoft-patch-tuesday-july-2026-the-ai-acopolypse-is-here-tue-jul-14th/
tags:
- veille-cyber
- sans-isc
---
### Analyse du Patch Tuesday de Juillet 2026 : Une mise à jour massive

Le Patch Tuesday de juillet 2026 se distingue par une ampleur exceptionnelle avec 622 vulnérabilités corrigées, auxquelles s'ajoutent 427 failles spécifiques au navigateur Microsoft Edge (Chromium). Parmi ces correctifs, 62 sont classées comme « critiques ».

**Points clés et vulnérabilités notables**

*   **Exploitation active :** Deux vulnérabilités font déjà l'objet d'exploitations réelles :
    *   **CVE-2026-56155 :** Élévation de privilèges dans Active Directory Federation Services.
    *   **CVE-2026-56164 :** Élévation de privilèges dans Microsoft SharePoint Server (gravité modérée).
*   **Vulnérabilités divulguées sans exploitation connue :**
    *   **CVE-2026-50661 :** Contournement de fonctionnalité de sécurité dans Windows BitLocker.
*   **Vulnérabilités critiques à surveiller :**
    *   **Exécution de code à distance (RCE) :** Plusieurs vulnérabilités critiques affectent le client et le serveur **DHCP**, ainsi que le pilote de transport multicast fiable (**RMCAST**), exposant les systèmes aux attaques de type « réseau adjacent ».
    *   **Composants Cloud :** Des failles critiques affectent Azure OpenAI (CVE-2026-45499) et Microsoft Entra Provisioning Service (CVE-2026-57100), bien que ces services cloud ne nécessitent généralement pas d'intervention directe de la part des clients.
    *   **Applications bureautiques :** De nombreuses failles RCE corrigées dans Excel, PowerPoint, Word et OneNote.

**Recommandations**

1.  **Priorisation des correctifs :** Bien que le volume de correctifs soit important, le temps de déploiement ne devrait pas augmenter drastiquement. Appliquez les mises à jour standard par produit (Office, Windows, Serveurs) dès que possible.
2.  **Gestion des services exposés :** Les failles RCE touchant les services réseau (DHCP, DNS, SMB, RMCAST) doivent être prioritaires sur les systèmes exposés ou dans des environnements Wi-Fi publics.
3.  **Surveillance des vecteurs d'attaque :** Étant donné l'exploitation active d'Active Directory et SharePoint, une attention particulière doit être portée à la mise à jour immédiate des serveurs d'infrastructure critique.
4.  **Processus de patching :** Ne pas se laisser submerger par le nombre de CVE ; la stratégie de gestion des correctifs doit rester centrée sur le parc applicatif et les rôles serveurs déjà en place dans l'infrastructure.

---
[Source](https://isc.sans.edu/diary/rss/33154){:target="_blank"}
