---
title: 'curl Patches HTTP/2 Upload Flaw After PoC Demonstrates Client-Side Code Execution'
date: 2026-10-14
permalink: /posts/2026/10/14/curl-patches-http2-upload-flaw-after-poc-demonstrates-client-side-code-execution/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique de type Use-After-Free dans curl

Une faille de sécurité majeure, identifiée comme **CVE-2026-92392**, a été découverte dans la gestion des téléchargements HTTP/2 par la bibliothèque `libcurl` et l'outil `curl`. Cette vulnérabilité, classée « Haute » par les développeurs, permet à un serveur malveillant de corrompre la mémoire d'un client et, dans des conditions spécifiques, d'exécuter du code arbitraire (RCE).

**Points clés :**
*   **Mécanisme d'attaque :** La faille repose sur un *use-after-free*. Lors d'un téléchargement HTTP/2, un serveur peut forcer le client à traiter des données résiduelles comme une nouvelle requête après la réinitialisation du flux. Le pointeur vers le gestionnaire de transfert (« easy handle ») reste actif après sa libération, permettant une corruption mémoire lorsque le serveur envoie des données supplémentaires.
*   **Complexité :** Bien que l'exécution de code soit théoriquement possible, elle nécessite une connaissance précise de l'architecture, de la mise en page de la mémoire et des mécanismes de défense (comme ASLR) de la cible. Le résultat le plus probable est un plantage du programme.
*   **Origine :** La vulnérabilité a été identifiée par Luna Tong (Anthropic) via un outil d'analyse automatisé (OSS Scanner).

**Vulnérabilité :**
*   **CVE-2026-92392 :** Use-after-free affectant curl et libcurl de la version 8.12.0 à 8.22.0.

**Recommandations :**
*   **Mise à jour immédiate :** Installer la version **8.23.0**, qui corrige cette faille ainsi que 23 autres vulnérabilités mineures.
*   **Correctifs pour versions antérieures :** Appliquer les correctifs spécifiques pour les branches maintenues (8.14.3, 8.16.2, 8.20.2).
*   **Contournement temporaire :** Si la mise à jour est impossible, désactiver l'utilisation de HTTP/2 en forçant le protocole HTTP/1.1 via l'option `--http1.1` (ligne de commande) ou `CURL_HTTP_VERSION_1_1` (via `libcurl`).
*   **Compilation :** Il est possible de recompiler `libcurl` sans la prise en charge de HTTP/2 pour éliminer la surface d'attaque.

---
[Source](https://thehackernews.com/2026/10/curl-patches-http2-upload-flaw-after.html){:target="_blank"}
