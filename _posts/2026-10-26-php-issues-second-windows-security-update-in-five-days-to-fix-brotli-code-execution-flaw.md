---
title: 'PHP Issues Second Windows Security Update in Five Days to Fix Brotli Code Execution Flaw'
date: 2026-10-26
permalink: /posts/2026/10/26/php-issues-second-windows-security-update-in-five-days-to-fix-brotli-code-execution-flaw/
tags:
- veille-cyber
- hackernews
---
### Mise à jour de sécurité PHP : Correction d'une faille critique dans la bibliothèque Brotli

PHP a publié de nouvelles versions de ses paquets Windows (8.2.35-1, 8.3.36-1, 8.4.27-1 et 8.5.12-1) afin de corriger une vulnérabilité critique affectant la bibliothèque de compression Brotli intégrée.

**Points clés :**
*   **Origine de la faille :** La vulnérabilité réside dans la bibliothèque Brotli (mise à jour vers la version 1.2.1).
*   **Vecteur d'attaque :** La faille est exploitable via l'extension cURL de PHP lorsque la décompression automatique des réponses HTTP est activée (via `CURLOPT_ENCODING`).
*   **Impact :** Un attaquant peut provoquer une corruption mémoire et potentiellement exécuter du code à distance (RCE) en envoyant une réponse compressée malveillante à une application PHP.
*   **Risque :** Classée critique (score de 9.2 sur l'échelle CVSS 4.0 par Google). Aucune exploitation active n'a été recensée à ce jour.

**Vulnérabilité :**
*   **CVE-2026-111497 :** Faille de corruption mémoire dans le décodeur Brotli.

**Recommandations :**
*   **Mise à jour :** Téléchargez et installez les nouvelles versions des paquets PHP pour Windows disponibles sur le site officiel. Comme le numéro de version PHP reste inchangé, vérifiez le suffixe « -1 » et le hash SHA-256 des fichiers.
*   **Atténuation temporaire :** Si une mise à jour immédiate est impossible, désactivez la décompression automatique dans vos clients HTTP. Pour la bibliothèque Guzzle, définissez l'option `decode_content` à `false`. Évitez de définir `CURLOPT_ENCODING` dans vos appels cURL.

---
[Source](https://thehackernews.com/2026/10/php-issues-second-windows-security.html){:target="_blank"}
