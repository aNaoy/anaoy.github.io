---
title: 'Placeholder third-party[.]com Referenced Across 1,700+ Repositories Now Serves Malicious Content'
date: 2026-09-24
permalink: /posts/2026/09/24/placeholder-third-partycom-referenced-across-1700-repositories-now-serves-malicious-content/
tags:
- veille-cyber
- hackernews
---
### Détournement de domaines factices : Une menace pour la supply chain logicielle

Le domaine `third-party[.]com`, historiquement utilisé comme espace réservé (placeholder) dans la documentation technique, a été enregistré par des acteurs malveillants. Ce domaine, référencé dans plus de 1 700 dépôts GitHub, est désormais utilisé pour mener des attaques de type **ClickFix** ciblant les utilisateurs Windows.

**Points clés :**
*   **Technique ClickFix :** Les attaquants utilisent des leurres (fausses vérifications de sécurité, CAPTCHA) pour pousser les utilisateurs à copier et exécuter des commandes malveillantes via le terminal ou la boîte de dialogue "Exécuter" de Windows.
*   **Clipboard Hijacking :** Les pages web compromettent le presse-papier de la victime pour injecter des scripts PowerShell distants.
*   **Contournement des scans :** Les analyses de sécurité statiques ne détectent pas la menace, car le contenu malveillant n'est servi qu'au moment de la requête, souvent en adaptant le contenu selon le système d'exploitation détecté (Windows vs macOS).
*   **Expansion de la menace :** Treize autres domaines couramment utilisés comme placeholders (ex: `your-domain[.]com`, `mycompany[.]com`) ont été identifiés comme servant des arnaques, des scarewares ou des sites de fraude à l'investissement, avec une exposition dans des centaines de milliers de fichiers sur GitHub.

**Vulnérabilités :**
*   Il ne s'agit pas d'une vulnérabilité logicielle avec CVE spécifique, mais d'une **vulnérabilité liée à la confiance aveugle** envers des noms de domaine non réservés par l'IANA. L'usage de domaines plausibles mais non contrôlés dans la documentation crée une surface d'attaque majeure par simple enregistrement du domaine par un tiers malveillant.

**Recommandations :**
*   **Audit de documentation :** Rechercher et supprimer les références aux domaines "placeholder" non réservés dans les bases de code, les tutoriels et les outils d'IA.
*   **Usage exclusif des domaines réservés :** Utiliser uniquement les domaines explicitement réservés par l'IANA pour les exemples techniques, tels que `example.com`, `example.org` ou `example.net`.
*   **Vigilance sur le presse-papier :** Sensibiliser les utilisateurs aux risques liés au "copier-coller" de commandes provenant de sources web non vérifiées ou de boîtes de dialogue de support technique suspectes.

---
[Source](https://thehackernews.com/2026/09/placeholder-third-partycom-referenced.html){:target="_blank"}
