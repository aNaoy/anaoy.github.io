---
title: 'WWBN, MedDream, Eclipse vulnerabilities'
date: 2025-08-07
permalink: /posts/2025/08/07/wwbn-meddream-eclipse-vulnerabilities/
tags:
- veille-cyber
- zerodaysfans
---
### Alertes de Sécurité : WWBN, MedDream, et Eclipse ThreadX

Des chercheurs en cybersécurité ont identifié plusieurs vulnérabilités dans les logiciels WWBN AVideo, MedDream PACS Premium et un module d'Eclipse ThreadX. Ces failles ont été corrigées par les éditeurs respectifs, conformément aux politiques de divulgation de Cisco.

**Points Clés et Vulnérabilités :**

*   **WWBN AVideo (versions 14.4 et dev master commit 8a8954ff)** :
    *   **Cinq vulnérabilités XSS (Cross-Site Scripting)** : Permettent l'exécution de JavaScript arbitraire via des requêtes HTTP spécialement conçues, nécessitant que l'utilisateur visite une page web malveillante.
        *   CVE-2025-46410
        *   CVE-2025-53084
        *   CVE-2025-50128
        *   CVE-2025-36548
        *   CVE-2025-41420
    *   **Vulnérabilité de condition de concurrence (TALOS-2025-2212 / CVE-2025-25214)** : Affectant la fonctionnalité de décompression dans `aVideoEncoder.json.php`, elle peut mener à une exécution de code arbitraire via une série de requêtes HTTP malveillantes.
    *   **Vulnérabilité d'interception incomplète (TALOS-2025-2213 / CVE-2025-48732)** : Présente dans le fichier `.htaccess` d'exemple, permettant une exécution de code arbitraire via une requête HTTP vers un fichier `.phar`.

*   **MedDream PACS Premium (versions 7.3.3.840 et 7.3.5.860)** :
    *   **Mauvaises permissions par défaut (TALOS-2025-2154 / CVE-2025-26469)** : Dans `CServerSettings::SetRegistryValues`, des identifiants stockés dans le registre peuvent être déchiffrés par une application malveillante.
    *   **Escalade de privilèges (TALOS-2025-2156 / CVE-2025-27724)** : Dans `login.php`, un fichier `.php` spécialement conçu peut permettre à un attaquant d'obtenir des capacités élevées.
    *   **XSS Réfléchi (TALOS-2025-2176 / CVE-2025-32731)** : Dans `radiationDoseReport.php`, un URL malveillant peut entraîner l'exécution de code JavaScript arbitraire.
    *   **Usurpation de Requête Serveur (SSRF) (TALOS-2025-2177 / CVE-2025-24485)** : Dans `cecho.php`, une requête HTTP non authentifiée peut mener à une faille SSRF.

*   **Eclipse ThreadX FileX (git commit 1b85eb2)** :
    *   **Dépassement de tampon (TALOS-2024-2088)** : Dans le pilote de disque RAM de FileX, une série de paquets réseau crafted peut permettre l'exécution de code.

**Recommandations :**

Il est conseillé aux utilisateurs de ces logiciels de s'assurer qu'ils disposent des dernières mises à jour fournies par les éditeurs pour corriger ces failles de sécurité. Des règles de détection pour les systèmes comme Snort sont disponibles sur Snort.org, et les rapports de vulnérabilité détaillés se trouvent sur Talos Intelligence.

---
[Source](https://blog.talosintelligence.com/wwbn-meddream-eclipse-vulnerabilities/){:target="_blank"}
