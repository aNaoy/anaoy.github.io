---
title: 'August Patch Tuesday includes blasts from the (recent) past'
date: 2025-08-13
permalink: /posts/2025/08/13/august-patch-tuesday-includes-blasts-from-the-recent-past/
tags:
- veille-cyber
- sophos
---
## Point sur les correctifs de sécurité Microsoft d'août

Ce mois-ci, Microsoft a publié 109 correctifs couvrant 16 familles de produits. Parmi ceux-ci, 18 sont classés comme critiques et 31 possèdent un score CVSS de 8.0 ou plus, dont un noté 10.0 pour Azure. Aucune exploitation active en dehors des environnements de test n'est connue, bien que deux vulnérabilités Windows (CVE-2025-53786 et CVE-2025-53779) soient publiquement documentées. Neuf vulnérabilités supplémentaires sont considérées comme plus susceptibles d'être exploitées dans les 30 prochains jours.

### Points Clés :

*   **Nombre total de CVEs :** 109
*   **Vulnérabilités publiquement divulguées :** 2 (CVE-2025-53786 et CVE-2025-53779)
*   **Vulnérabilités exploitées en temps réel :** 0
*   **Gravité :** 18 critiques, 90 importantes, 1 modérée.
*   **Types d'impact :** Élévation de privilèges (44), Exécution de code à distance (35), Divulgation d'informations (18), Usurpation (7), Déni de service (4), Altération (1).
*   **Produits les plus touchés :** Windows (65), Microsoft 365 (16), Office (16), Azure (7), SQL (6).

### Vulnérabilités Notables et Recommandations :

Plusieurs vulnérabilités présentent un intérêt particulier :

*   **CVE-2025-50165 et CVE-2025-53766 :** Deux vulnérabilités critiques dans les composants graphiques de Windows et GDI+ avec des scores CVSS de 9.8. Elles permettent l'exécution de code à distance sans interaction utilisateur, notamment via le traitement d'images JPEG ou de métadonnées spécialement conçues.
    *   **Recommandation :** Appliquer les correctifs pour Windows et Office.

*   **CVE-2025-49712 :** Une vulnérabilité critique dans Microsoft SharePoint permettant l'exécution de code à distance via le réseau pour des attaquants authentifiés.
    *   **Recommandation :** Appliquer le correctif pour SharePoint.

*   **CVE-2025-53731, CVE-2025-53733, CVE-2025-53740, CVE-2025-53784 :** Quatre vulnérabilités critiques dans Microsoft Office et Word, exploitables via la fonction "Volet Aperçu".
    *   **Recommandation :** Appliquer les correctifs pour Office et Word.

*   **CVE-2025-53774 et CVE-2025-53787 :** Deux vulnérabilités critiques affectant Microsoft 365 Copilot (Business Chat) qui permettent la divulgation d'informations. Bien que mitigées par Microsoft, elles sont notables pour leurs implications futures.
    *   **Recommandation :** Rester vigilant et suivre les mises à jour de sécurité pour Microsoft 365.

*   **CVE-2025-53786 :** Une vulnérabilité importante dans les déploiements hybrides de Microsoft Exchange Server, permettant une élévation de privilèges. Elle est jugée susceptible d'être exploitée dans les 30 jours.
    *   **Recommandation :** Appliquer le correctif pour Exchange Server, en particulier pour les environnements hybrides.

*   **CVE-2025-53767 :** Une vulnérabilité critique avec un score CVSS de 10.0 concernant Azure OpenAI, permettant une élévation de privilèges. Elle a déjà été atténuée par Microsoft.
    *   **Recommandation :** Vérifier les mesures de sécurité pour les services Azure concernés.

Les utilisateurs sont encouragés à télécharger et appliquer les mises à jour cumulatives pour leurs systèmes via le catalogue Windows Update ou Windows Update pour mitiger ces risques.

---
[Source](https://news.sophos.com/en-us/2025/08/13/august-patch-tuesday-includes-blasts-from-the-recent-past/){:target="_blank"}
