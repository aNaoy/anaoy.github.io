---
title: 'Microsoft January 2026 Patch Tuesday fixes 3 zero-days, 114 flaws'
date: 2026-01-13
permalink: /posts/2026/01/13/microsoft-january-2026-patch-tuesday-fixes-3-zero-days-114-flaws/
tags:
- veille-cyber
- bleepingcomp
---
## Patch Tuesday de Janvier 2026 : Mises à jour de Sécurité et Vulnérabilités

Microsoft a publié ses mises à jour de sécurité de janvier 2026, corrigeant un total de 114 failles. Parmi celles-ci figurent trois vulnérabilités zero-day, dont une qui était activement exploitée. Huit vulnérabilités ont été classées comme critiques.

### Points Clés

*   **114 vulnérabilités corrigées :** Ce chiffre inclut les failles dans les systèmes Windows, ainsi que dans certains composants comme Microsoft Office et Azure. Les mises à jour pour Microsoft Edge et Mariner, publiées plus tôt dans le mois, ne sont pas incluses dans ce décompte.
*   **Trois zero-days :** Trois vulnérabilités étaient connues du grand public ou exploitées avant qu'un correctif ne soit disponible.
    *   Une vulnérabilité d' **exposition d'informations sensibles dans le Gestionnaire de fenêtres** (Desktop Window Manager) est activement exploitée. Elle permettrait à un attaquant local de lire des adresses mémoire associées à un port ALPC distant.
    *   Deux autres zero-days font partie de cette mise à jour.
*   **Expiration des certificats de démarrage sécurisé :** Microsoft met en garde contre l'expiration prochaine des certificats de démarrage sécurisé émis en 2011. Les systèmes non mis à jour risquent de voir leur protection contournée par des acteurs malveillants. Les mises à jour visent à renouveler ces certificats.
*   **Suppression de pilotes vulnérables :** Des pilotes de modem tiers (Agere) précédemment identifiés comme vulnérables et exploités pour obtenir des privilèges administratifs ont été supprimés des systèmes Windows.

### Vulnérabilités notables (avec CVE si disponibles)

Voici une sélection des vulnérabilités corrigées, en mettant l'accent sur les plus critiques et celles mentionnées spécifiquement :

*   **Gestionnaire de fenêtres (Desktop Window Manager) :**
    *   Exposition d'informations sensibles (Activement exploitée) : **CVE-2026-20805**
    *   Élévation de privilèges : **CVE-2026-20871**
*   **Pilotes de modem Agere pour Windows :**
    *   Élévation de privilèges : **CVE-2023-31096** (Ce CVE semble être une ancienne référence, mais la description mentionne la suppression de ces pilotes)
*   **Composants Microsoft Office :**
    *   Exécution de code à distance (Critical) : **CVE-2026-20952**, **CVE-2026-20953**, **CVE-2026-20957**, **CVE-2026-20955**, **CVE-2026-20944**
    *   Contournement de fonctionnalité de sécurité : **CVE-2026-20949** (Microsoft Excel)
*   **Composant graphique Microsoft :**
    *   Élévation de privilèges (Critical) : **CVE-2026-20822**
*   **Service de sous-système d'autorité de sécurité locale (LSASS) :**
    *   Exécution de code à distance (Critical) : **CVE-2026-20854**
*   **Démarrage sécurisé :**
    *   Contournement de fonctionnalité de sécurité dû à l'expiration du certificat : **CVE-2026-21265**
*   **Azure Connected Machine Agent :**
    *   Élévation de privilèges : **CVE-2026-21224**

La liste complète des vulnérabilités et de leurs descriptions est disponible via le lien fourni dans l'article original.

### Recommandations

*   **Appliquer les mises à jour :** La priorité absolue est d'installer rapidement les mises à jour de sécurité publiées par Microsoft pour corriger ces 114 vulnérabilités, en particulier les trois zero-days.
*   **Surveiller les certificats de démarrage sécurisé :** Vérifier l'état des certificats de démarrage sécurisé et s'assurer que les systèmes sont à jour pour maintenir leur intégrité.
*   **Mettre à jour Microsoft Edge et Mariner :** Bien que non inclus dans le décompte principal, s'assurer que ces composants sont également à jour.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-january-2026-patch-tuesday-fixes-3-zero-days-114-flaws/){:target="_blank"}
