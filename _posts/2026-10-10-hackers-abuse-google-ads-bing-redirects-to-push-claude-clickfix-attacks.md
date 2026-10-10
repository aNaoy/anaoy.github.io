---
title: 'Hackers abuse Google Ads, Bing redirects to push Claude ClickFix attacks'
date: 2026-10-10
permalink: /posts/2026/10/10/hackers-abuse-google-ads-bing-redirects-to-push-claude-clickfix-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Menace "Adception" : Malvertising ciblant les utilisateurs de Claude

Une nouvelle campagne de malvertising, baptisée « Adception », détourne les redirections légitimes de Bing pour tromper les filtres de sécurité de Google Ads. Cette méthode permet aux attaquants d'afficher des publicités crédibles menant à de faux sites de téléchargement pour l'application macOS de Claude, utilisant une technique d'attaque par « ClickFix » pour compromettre les terminaux des victimes.

**Points clés :**
*   **Contournement de sécurité :** L'usage du domaine `bing.com` comme destination de la publicité permet de masquer la nature malveillante du lien et d'échapper à la détection initiale.
*   **Cloaking sophistiqué :** Les attaquants utilisent plusieurs couches de filtrage (vérification du référent, des en-têtes du navigateur et de la source du trafic) pour bloquer les scanners de sécurité et les accès directs, renvoyant une erreur 404 aux analystes.
*   **Manipulation du presse-papier :** La victime est incitée à copier une commande d'installation apparemment légitime. Cependant, le bouton « copier » injecte une commande malveillante détournée qui télécharge et exécute silencieusement un script distant via `zsh` sur macOS.
*   **Infrastructure :** Les attaquants utilisent des sites WordPress compromis comme relais avant d'atteindre la page de téléchargement factice.

**Vulnérabilités :**
*   **Aucune CVE spécifique n'est associée :** Cette attaque repose sur l'ingénierie sociale (ClickFix) et l'exploitation de fonctionnalités légitimes de redirection publicitaire (Open Redirect) plutôt que sur une faille logicielle répertoriée.

**Recommandations :**
*   **Vigilance accrue :** Ne jamais copier-coller ou exécuter des commandes provenant de terminaux ou de scripts récupérés sur des sites tiers, même si le site semble officiel.
*   **Vérification des URL :** Inspecter systématiquement la destination réelle des liens sponsorisés avant de cliquer et privilégier les sources de téléchargement officielles (sites directement saisis dans le navigateur).
*   **Gestion du presse-papier :** Être conscient que les sites web peuvent modifier le contenu du presse-papier lors d'un « copier » ; il est conseillé de vérifier la commande copiée dans un éditeur de texte brut avant toute exécution dans le Terminal.
*   **Sécurité des sites :** Pour les administrateurs, sécuriser les sites WordPress (mises à jour, plugins, monitoring) afin d'éviter qu'ils ne soient détournés en plateformes de redirection malveillante.

---
[Source](https://www.bleepingcomputer.com/news/security/hackers-abuse-google-ads-bing-redirects-to-push-claude-clickfix-attacks/){:target="_blank"}
