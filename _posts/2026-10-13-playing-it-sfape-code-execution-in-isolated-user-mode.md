---
title: 'Playing It SFAPE: Code Execution in Isolated User Mode'
date: 2026-10-13
permalink: /posts/2026/10/13/playing-it-sfape-code-execution-in-isolated-user-mode/
tags:
- veille-cyber
- zerodaysfans
---
### Exécution de code dans le mode utilisateur isolé (IUM) de Windows

L'article analyse des vulnérabilités au sein de **SFAPE.dll**, un composant « enclave » de Windows utilisé par *Microsoft Defender SmartScreen* pour protéger les identifiants utilisateur. Ces enclaves fonctionnent via la sécurité basée sur la virtualisation (VBS), isolant l'exécution dans un niveau de confiance distinct (VTL1) inaccessible directement depuis le noyau Windows standard (VTL0).

#### Points clés
*   **Isolation VBS :** Les enclaves VBS permettent d'isoler des données sensibles (ex: hachages de mots de passe) dans une mémoire privée. Bien que l'hôte (VTL0) ne puisse pas lire cette mémoire, il communique avec l'enclave via des appels exportés (`CallEnclave`).
*   **Surface d'attaque :** La sécurité repose sur la validation rigoureuse des entrées fournies par l'hôte. Des erreurs dans cette logique permettent de corrompre la mémoire VTL1, d'outrepasser les validateurs d'adresses et d'exécuter du code arbitraire au sein de l'enclave.
*   **Chaînage d'exploitation :** L'exploitation démontrée part d'une écriture fixe de 4 octets (`STATUS_ALREADY_INITIALIZED`) pour corrompre la configuration de l'enclave, ce qui permet de détourner les fonctions de vérification de portée mémoire, de manipuler des objets via des conditions de concurrence (TOCTOU) et, finalement, d'utiliser `NtContinue` pour exécuter du code arbitraire en réutilisant des portions de `vertdll`.

#### Vulnérabilités
*   **CVE-2026-83498 :** Vulnérabilité critique dans `SFAPE.dll` liée à une vérification insuffisante lors de l'initialisation répétée de l'enclave, permettant une écriture en mémoire hors limites.
*   **CVE-2023-36880 & CVE-2024-21423 :** Vulnérabilités antérieures dans l'enclave `prefs_enclave_x64.dll` (Microsoft Edge), servant de base aux recherches sur l'exploitation des enclaves.

#### Recommandations
*   **Mise à jour système :** Appliquer les correctifs de sécurité de septembre 2026 (KB5124008 et ultérieurs) qui corrigent `SFAPE.dll`.
*   **Gestion des politiques d'intégrité :** Bien que Microsoft ait mis à jour la politique d'intégrité de code (VBS Code Integrity) pour bloquer les anciennes versions de `SFAPE.dll`, une vigilance particulière est requise vis-à-vis des composants obsolètes ou vulnérables (`Bring Your Own Vulnerable Enclave`) qui ne sont pas systématiquement bloqués sur tous les systèmes.
*   **Durcissement :** S'assurer que la protection LSA (*LSA Protection*) est active afin de limiter l'accès aux processus sensibles chargés de manipuler les enclaves.

---
[Source](https://blog.doyensec.com/2026/10/13/Sfape.html){:target="_blank"}
