---
title: 'Microsoft: Some Windows PCs fail to install latest monthly updates'
date: 2026-06-10
permalink: /posts/2026/06/10/microsoft-some-windows-pcs-fail-to-install-latest-monthly-updates/
tags:
- veille-cyber
- bleepingcomp
---
### Dysfonctionnement des mises à jour Windows : Erreurs d'installation sur les versions 24H2 et 25H2

Certains appareils ayant migré vers Windows 11 (versions 24H2 ou 25H2) rencontrent des échecs lors de l'installation des mises à jour cumulatives mensuelles. Ce problème touche une petite partie des systèmes mis à niveau depuis Windows 10 (21H2/22H2) ou Windows 11 (23H2).

**Points clés :**
*   **Symptômes :** Blocage des mises à jour Windows et apparition des codes d'erreur **0x80073712** ou **0x800f0993**.
*   **Causes :** Corruption du magasin de composants système ou échec de réhydratation lors de la mise à niveau.
*   **Vulnérabilités :** Aucune CVE associée ; il s'agit d'un problème de fiabilité du processus de mise à jour système et non d'une faille de sécurité exploitable.

**Recommandations :**
1.  **Redémarrage simple :** Pour les appareils grand public (Home) et non gérés, un simple redémarrage peut suffire à appliquer un correctif déployé automatiquement par Microsoft.
2.  **Suppression du package corrompu :** Pour les systèmes déjà impactés, exécutez la commande suivante dans une invite de commande (CMD) en mode administrateur :
    `dism /online /remove-package /packagename:Package_for_RollupFix~31bf3856ad364e35~amd64~~26100.1742.1.10`
3.  **Mise à niveau sur place (In-place upgrade) :** Si les solutions précédentes échouent, effectuez une mise à niveau complète de Windows 11 pour réparer les fichiers système endommagés.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-some-upgraded-windows-pcs-fail-to-install-monthly-updates/){:target="_blank"}
