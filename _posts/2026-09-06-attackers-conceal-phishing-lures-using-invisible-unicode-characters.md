---
title: 'Attackers conceal phishing lures using invisible Unicode characters'
date: 2026-09-06
permalink: /posts/2026/09/06/attackers-conceal-phishing-lures-using-invisible-unicode-characters/
tags:
- veille-cyber
- bleepingcomp
---
### Contre-mesures face à la fraude par « ASCII Smuggling »

Des acteurs malveillants exploitent la technique du « smuggling ASCII » pour contourner les filtres de sécurité des e-mails. Cette méthode consiste à insérer des caractères Unicode invisibles (bloc U+E0000–U+E007F) au sein de mots-clés financiers (ex: « funding » devient « fun[caractère invisible]ding ») afin de tromper les systèmes de détection basés sur des listes de mots ou des expressions régulières. Une campagne massive, utilisant cette technique, a été observée avec des pics atteignant jusqu'à 2,37 millions de messages quotidiens.

**Points clés :**
*   **Origine :** La technique provient initialement des attaques par injection de prompt sur les IA, avant d'être détournée pour le phishing à grande échelle.
*   **Infrastructure :** Les messages ont été diffusés via la plateforme de marketing légitime *ActiveCampaign*.
*   **Efficacité :** Bien que la technique permette d'échapper à l'analyse textuelle simple, les solutions de sécurité modernes (comme Microsoft Defender) parviennent à bloquer plus de 99 % de ces messages grâce à une analyse multicritères (réputation de l'expéditeur, IP, domaine).
*   **Vulnérabilités :** Il ne s'agit pas d'une vulnérabilité CVE spécifique, mais d'une faiblesse logique dans les moteurs de filtrage qui n'effectuent pas de normalisation du texte avant l'analyse.

**Recommandations :**
*   **Normalisation du contenu :** Supprimer ou normaliser les caractères Unicode invisibles et les points de code « tags » avant toute application de filtres (mots-clés, regex, signatures).
*   **Détection d'anomalies :** Configurer les outils de sécurité pour signaler la présence inhabituelle de caractères issus du bloc « tags » comme un indicateur de compromission potentiel.
*   **Sécurisation des IA :** Appliquer cette même normalisation avant de transmettre le contenu des e-mails à des assistants IA pour prévenir les injections de prompts malveillants.

---
[Source](https://www.bleepingcomputer.com/news/security/attackers-conceal-phishing-lures-using-invisible-unicode-characters/){:target="_blank"}
