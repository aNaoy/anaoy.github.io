---
title: 'How attackers adapt to built-in macOS protection'
date: 2025-08-29
permalink: /posts/2025/08/29/how-attackers-adapt-to-built-in-macos-protection/
tags:
- veille-cyber
- securelist
---
**Adaptation des attaquants aux protections intégrées de macOS**

Les cybercriminels ciblent de plus en plus macOS en raison de sa popularité croissante. Bien que le système d'exploitation intègre de solides mécanismes de sécurité, les attaquants développent des techniques pour les contourner.

**Points Clés et Vulnérabilités**

*   **Keychain :** Gestionnaire de mots de passe et de secrets.
    *   **Vulnérabilité :** Des outils comme Chainbreaker peuvent extraire des données des fichiers Keychain si l'attaquant a un accès physique et le mot de passe maître. Les outils natifs comme `security` peuvent être détournés par des attaquants ayant déjà compromis le système.
*   **SIP (System Integrity Protection) :** Protège les fichiers et processus système critiques contre les modifications.
    *   **Vulnérabilité :** Le SIP peut être désactivé en mode de récupération avec la commande `csrutil disable`. L'accès physique ou les droits administrateur compromis permettent cette désactivation.
*   **TCC (Transparency, Consent, and Control) :** Contrôle d'accès aux données sensibles par l'utilisateur.
    *   **Vulnérabilité :** Le "TCC Clickjacking" superpose une fausse fenêtre de demande de permission pour tromper l'utilisateur et obtenir des accès non désirés (comme l'accès complet au disque). La modification des bases de données `TCC.db` nécessite la désactivation du SIP ou l'accès à un processus de confiance.
*   **File Quarantine :** Marque les fichiers téléchargés pour avertir l'utilisateur avant leur exécution.
    *   **Vulnérabilité :** Des outils comme `curl` ou `wget` ne marquent pas les fichiers avec l'attribut de quarantaine. L'attribut peut être supprimé manuellement avec `xattr -d com.apple.quarantine`.
*   **Gatekeeper :** Assure que seules les applications de confiance et signées sont exécutées.
    *   **Vulnérabilité :** Les attaquants peuvent contourner l'avertissement de sécurité en demandant aux utilisateurs d'exécuter les applications via le menu contextuel ("Ouvrir" via clic droit) plutôt qu'en double-cliquant. Le SIP peut être désactivé avec `spctl --master disable` ou `--global-disable`.

**Recommandations**

*   **Pour Keychain :** Surveiller l'utilisation des commandes `security dump-keychain` et `security list-keychains` via les journaux d'événements du système (par exemple, avec ESF).
*   **Pour SIP :** Surveiller les changements d'état du SIP à l'aide de la commande `csrutil status`.
*   **Pour TCC :** Surveiller les modifications apportées aux bases de données `TCC.db`.
*   **Pour File Quarantine :** Surveiller l'exécution de la commande `xattr -d com.apple.quarantine`. Analyser l'origine des fichiers suspects n'ayant pas l'attribut de quarantaine.
*   **Pour Gatekeeper :** Surveiller l'exécution de la commande `spctl` avec les paramètres `–master disable` ou `–global-disable`.

Pour une protection complète, il est recommandé d'utiliser des solutions de sécurité tierces avancées, telles que Kaspersky Endpoint Detection and Response (EDR), qui peuvent détecter et bloquer les menaces décrites. L'utilisation de règles Sigma peut également aider à se prémunir contre le contournement des mesures de sécurité standard.

---
[Source](https://securelist.com/macos-security-and-typical-attacks/117367/){:target="_blank"}
