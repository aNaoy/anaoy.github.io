---
title: 'New DDRop Attack Breaks Intel TDX and AMD SEV-SNP Confidential Computing'
date: 2026-09-14
permalink: /posts/2026/09/14/new-ddrop-attack-breaks-intel-tdx-and-amd-sev-snp-confidential-computing/
tags:
- veille-cyber
- hackernews
---
### DDRop : Une faille matérielle critique dans le Cloud Computing confidentiel

L'attaque **DDRop** permet de compromettre l'intégrité de la mémoire chiffrée sur les serveurs utilisant les technologies Intel TDX, Intel Scalable SGX et AMD SEV-SNP. En exploitant l'absence de vérification de « fraîcheur » (*freshness*) des données en mémoire, l'attaque permet à un utilisateur malveillant de forcer le processeur à lire d'anciennes données chiffrées, le faisant croire à une mise à jour réussie.

#### Points clés
*   **Mécanisme :** Un interposeur matériel bon marché (environ 160 $) est inséré physiquement entre le processeur et le module mémoire DDR5. Il intercepte le bus mémoire et supprime sélectivement certaines écritures en créant de fausses erreurs signalées au module, tout en masquant ces erreurs au processeur.
*   **Impact :** L'attaque permet de contourner les protections de confidentialité, de lire la mémoire protégée, de forger des attestations de sécurité pour usurper des machines virtuelles de confiance, ou d'activer des modes de débogage pour exfiltrer des données.
*   **Portée :** Concerne les serveurs cloud utilisant Intel TDX, Intel SGX et AMD SEV-SNP. Les GPU NVIDIA sont immunisés car leur mémoire est intégrée au package du processeur.
*   **Modèle de menace :** Nécessite un accès physique temporaire à la machine (ex: employé malveillant, compromission de la chaîne d'approvisionnement).

#### Vulnérabilités
*   **CVE :** Aucune. Intel et AMD considèrent les attaques physiques nécessitant un interposeur comme hors du périmètre de leur modèle de menace standard.

#### Recommandations
*   **Correctifs :** Aucun patch logiciel n'est possible, car la faille réside dans la conception matérielle (absence de vérification de fraîcheur).
*   **Atténuation :**
    *   Activer les modes d'intégrité cryptographique les plus robustes (ex: *Cryptographic Integrity* sur Intel TDX), bien que cela ne bloque pas tous les vecteurs de l'attaque.
    *   Renforcer la sécurité physique des centres de données et surveiller l'accès aux serveurs pour détecter toute altération matérielle.
    *   Réduire les fonctionnalités de gestion mémoire vulnérables au niveau logiciel pour limiter la surface d'attaque.

---
[Source](https://thehackernews.com/2026/09/new-ddrop-attack-breaks-intel-tdx-and.html){:target="_blank"}
