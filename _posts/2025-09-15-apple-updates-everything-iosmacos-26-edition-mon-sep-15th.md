---
title: 'Apple Updates Everything - iOS/macOS 26 Edition, (Mon, Sep 15th)'
date: 2025-09-15
permalink: /posts/2025/09/15/apple-updates-everything-iosmacos-26-edition-mon-sep-15th/
tags:
- veille-cyber
- sans-isc
---
### Mise à jour de sécurité Apple : Correctifs et Vulnérabilités

Apple a publié des mises à jour corrigeant un nombre important de vulnérabilités affectant iOS et macOS. Ces failles peuvent permettre à des applications malveillantes d'accéder à des données sensibles, d'outrepasser des restrictions de sécurité, d'exécuter du code arbitraire ou de provoquer des plantages système.

**Points Clés et Vulnérabilités :**

*   **Accès aux données sensibles :** Plusieurs vulnérabilités (ex: CVE-2025-24197, CVE-2025-31255, CVE-2025-43207, CVE-2025-43292, CVE-2025-43303, CVE-2025-43307, CVE-2025-43314, CVE-2025-43315, CVE-2025-43317, CVE-2025-43319, CVE-2025-43321, CVE-2025-43325, CVE-2025-43337) permettent à des applications d'accéder à des informations utilisateur privées, y compris les données de localisation, les informations de contact, ou de capturer des captures d'écran.
*   **Contournement des restrictions et élévation de privilèges :** Des failles permettent à des applications de contourner les restrictions de bac à sable (CVE-2025-43204, CVE-2025-43286, CVE-2025-43299, CVE-2025-43330, CVE-2025-43332, CVE-2025-43340) ou d'obtenir des privilèges root (CVE-2025-43298, CVE-2025-43304, CVE-2025-43316, CVE-2025-43333, CVE-2025-43341).
*   **Exécution de code et corruption mémoire :** Le traitement de contenu web, d'audio ou d'images spécialement conçus peut mener à une redirection URL inattendue (CVE-2025-31254, CVE-2025-43272, CVE-2025-43342, CVE-2025-43343, CVE-2025-43368), à un crash système (CVE-2025-43283, CVE-2025-43302, CVE-2025-43312, CVE-2025-43344, CVE-2025-43346, CVE-2025-43349), ou à une corruption de mémoire (CVE-2025-43277, CVE-2025-43287, CVE-2025-43353, CVE-2025-43346, CVE-2025-43372).
*   **Informations sensibles sur l'écran de verrouillage :** Des suggestions de clavier peuvent révéler des informations sensibles (CVE-2025-24133). Les appels FaceTime peuvent apparaître sur un appareil verrouillé (CVE-2025-31271). Les onglets de navigation privée pourraient être accessibles sans authentification (CVE-2025-30468).
*   **Exploitation avancée :** Une vulnérabilité dans ImageIO (CVE-2025-43300) est connue pour avoir été exploitée dans des attaques sophistiquées contre des individus ciblés.
*   **Autres vulnérabilités :** Incluent la contournement du mode restreint USB, l'usurpation de l'adresse de la barre d'adresse Safari, l'accès non autorisé à des notes verrouillées, et la surveillance des frappes clavier.

**Recommandations :**

Il est fortement recommandé aux utilisateurs de mettre à jour leurs appareils Apple (iPhone, iPad, Mac) vers les dernières versions d'iOS et de macOS dès que possible pour bénéficier des correctifs de sécurité.

---
[Source](https://isc.sans.edu/diary/rss/32286){:target="_blank"}
