---
title: 'Silent Swap Crypto Clipper Uses Fake Google Notes Extension to Replace Wallet Addresses'
date: 2026-06-30
permalink: /posts/2026/06/30/silent-swap-crypto-clipper-uses-fake-google-notes-extension-to-replace-wallet-addresses/
tags:
- veille-cyber
- hackernews
---
### Silent Swap : Une nouvelle menace de vol de cryptomonnaies par clipboard hijacking

La campagne « Silent Swap » utilise de faux installateurs (type « Google Notes ») pour injecter des extensions malveillantes dans les navigateurs basés sur Chromium. Ces extensions agissent comme des « clippers » : elles surveillent le presse-papier des utilisateurs pour remplacer les adresses de portefeuilles cryptographiques copiées par celles des attaquants lors des transactions.

**Points clés :**
*   **Technique « EtherHiding » :** Le malware utilise la blockchain pour résoudre ses serveurs de commande et contrôle (C2), rendant l'infrastructure difficile à bloquer.
*   **Persistence furtive :** Le malware modifie les fichiers de préférences (`Secure Preferences`) du navigateur pour charger l'extension sans approbation de l'utilisateur.
*   **Mapping dynamique :** Au lieu d'utiliser une adresse unique, le serveur des attaquants génère une adresse de remplacement spécifique pour chaque victime, rendant la détection plus complexe.
*   **Extensions VPN frauduleuses :** Parallèlement, des extensions comme « VPN Go » (Chrome/Firefox) ont été identifiées ; elles utilisent des mises à jour légitimes suivies de versions malveillantes pour voler non seulement des adresses crypto, mais aussi des mots de passe, clés API et phrases secrètes.

**Vulnérabilités exploitées :**
*   Aucune CVE spécifique n'est mentionnée, car l'attaque repose sur la manipulation légitime des fichiers de configuration du navigateur (`Secure Preferences` et `Preferences`) et sur l'abus des permissions accordées aux extensions (accès au presse-papier, historique et URLs).

**Recommandations :**
*   **Suppression immédiate :** Désinstaller toute extension suspecte, particulièrement les outils VPN gratuits ou utilitaires de notes installés via des sources non officielles.
*   **Réinitialisation des secrets :** Considérer comme compromis tous les mots de passe, clés privées, API keys ou phrases de récupération (seed phrases) utilisés pendant que ces extensions étaient actives.
*   **Vigilance sur l'origine des logiciels :** Éviter les installateurs non signés et privilégier uniquement les sites officiels.
*   **Vérification des transactions :** Toujours contrôler visuellement l'adresse de destination lors d'un transfert de cryptomonnaies, idéalement en vérifiant les premiers et derniers caractères de l'adresse.

---
[Source](https://thehackernews.com/2026/06/silent-swap-crypto-clipper-uses-fake.html){:target="_blank"}
