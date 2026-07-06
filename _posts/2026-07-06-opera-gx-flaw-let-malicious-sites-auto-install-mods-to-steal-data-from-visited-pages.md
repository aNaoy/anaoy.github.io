---
title: 'Opera GX Flaw Let Malicious Sites Auto-Install Mods to Steal Data From Visited Pages'
date: 2026-07-06
permalink: /posts/2026/07/06/opera-gx-flaw-let-malicious-sites-auto-install-mods-to-steal-data-from-visited-pages/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité critique dans Opera GX : Exfiltration de données via injection CSS universelle

Une faille de sécurité majeure dans Opera GX permettait à des sites web malveillants d'installer silencieusement des "Mods" (personnalisations esthétiques) sans aucune interaction de l'utilisateur. Cette vulnérabilité, bien qu'esthétique en apparence, a été détournée pour réaliser une attaque par injection CSS universelle permettant l'exfiltration de données sensibles sur n'importe quel site visité.

**Points clés :**
*   **Mécanisme d'attaque :** Le pipeline d'installation des Mods autorisait le téléchargement et l'activation automatique de fichiers `.crx` sans invite de confirmation.
*   **Exfiltration de données (XS-Leak) :** En injectant des milliers de règles CSS personnalisées, un attaquant peut interroger les attributs HTML des pages visitées par la victime. En observant les requêtes réseau générées par le chargement d'images de fond spécifiques selon les sélecteurs CSS, il est possible de reconstruire des informations (telles qu'une adresse Gmail) caractère par caractère.
*   **Rapidité :** L'attaque pouvait être exécutée en quelques secondes après le chargement d'une page malveillante, avant même que l'utilisateur ne puisse réagir à la notification de modification.
*   **Impact additionnel :** Le même vecteur d'auto-installation permettait de faire planter le navigateur en mode navigation privée en chargeant un fichier `.crx` corrompu, provoquant la fermeture brutale de tous les onglets ouverts.

**Vulnérabilités :**
*   **CVE :** Aucune CVE n'a été attribuée à cette faille.
*   **Gravité :** Évaluée comme P1 (critique) par Opera, récompensée par une prime de 5 000 $.

**Recommandations :**
*   **Mise à jour immédiate :** Le correctif a été déployé dans la version **130.0.5847.89** d'Opera GX. Il est impératif de s'assurer que le navigateur est à jour via le menu `opera://about`.
*   **Vigilance utilisateur :** Bien que le correctif empêche l'auto-installation, il est conseillé de rester attentif aux notifications système et de supprimer immédiatement tout mod ou extension dont l'origine est inconnue ou suspecte.

---
[Source](https://thehackernews.com/2026/07/opera-gx-flaw-let-malicious-sites-auto.html){:target="_blank"}
