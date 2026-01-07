---
title: 'A phishing campaign with QR codes rendered using an HTML table, (Wed, Jan 7th)'
date: 2026-01-07
permalink: /posts/2026/01/07/a-phishing-campaign-with-qr-codes-rendered-using-an-html-table-wed-jan-7th/
tags:
- veille-cyber
- sans-isc
---
## Contournement des détections de QR codes malveillants

Une campagne de hameçonnage exploite une technique consistant à générer des QR codes non pas sous forme d'image, mais à l'aide d'un tableau HTML. Cette méthode, bien que connue, est peu répandue et permet de contourner les mécanismes de détection actuels qui analysent les images incluses dans les e-mails.

Les messages observés, envoyés entre le 22 et le 26 décembre, contenaient un texte limité et un QR code apparemment normal. Cependant, l'analyse du code source révèle que le QR code était construit par des cellules de tableau avec des couleurs de fond noir et blanc.

Les liens contenus dans ces QR codes redirigeaient vers des sous-domaines du domaine "lidoustoo[.]click". La structure des URL variait, incluant le domaine du destinataire, une chaîne de caractères, et enfin le domaine principal, le tout suivi du courriel du destinataire.

Cette approche souligne les limites des contrôles de sécurité purement techniques qui se basent sur des hypothèses quant à la représentation du contenu malveillant. Elle rappelle l'importance de la vigilance des utilisateurs et de l'amélioration continue des mesures de sensibilisation face à un paysage de menaces en constante évolution.

### Points Clés :

*   Utilisation de QR codes générés par des tableaux HTML pour contourner la détection.
*   Redirection vers des domaines malveillants spécifiques ("lidoustoo[.]click").
*   Structure d'URL conçue pour potentiellement tromper les filtres et les utilisateurs.
*   Nécessité d'une approche de sécurité combinant la technique et la sensibilisation des utilisateurs.

### Vulnérabilités :

*   Aucune vulnérabilité spécifique (CVE) n'est mentionnée dans l'article. La technique contourne les mécanismes de détection existants plutôt qu'elle n'exploite une faiblesse logicielle connue.

### Recommandations :

*   Les mécanismes de sécurité doivent être mis à jour pour analyser le contenu généré par des tableaux HTML, et pas seulement les images.
*   Les utilisateurs doivent rester vigilants face aux QR codes, même s'ils semblent légitimes, et vérifier la destination avant de les scanner.
*   La sensibilisation des utilisateurs aux techniques de hameçonnage actuelles est cruciale.

---
[Source](https://isc.sans.edu/diary/rss/32606){:target="_blank"}
