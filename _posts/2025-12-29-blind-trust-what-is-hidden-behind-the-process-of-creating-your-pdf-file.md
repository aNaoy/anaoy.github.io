---
title: 'Blind trust: what is hidden behind the process of creating your PDF file?'
date: 2025-12-29
permalink: /posts/2025/12/29/blind-trust-what-is-hidden-behind-the-process-of-creating-your-pdf-file/
tags:
- veille-cyber
- zerodaysfans
---
### Risques de Sécurité dans la Génération de Fichiers PDF à Partir de HTML

La conversion de documents HTML en PDF, bien que courante et souvent considérée comme une tâche technique simple, représente un point critique où des failles de sécurité peuvent être exploitées. Les bibliothèques chargées de ce processus interagissent avec le système de fichiers, le réseau et le traitement de diverses ressources (images, polices, SVG), ouvrant la porte à des vulnérabilités telles que le vol de données, la falsification de requêtes côté serveur (SSRF) et le déni de service (DoS).

Une analyse approfondie de plusieurs bibliothèques populaires (TCPDF, html2pdf, jsPDF, mPDF, snappy, dompdf, et OpenPDF) a révélé un total de 13 vulnérabilités, 7 comportements intentionnels à risque et 6 configurations erronées courantes. Ces failles touchent des classes de vulnérabilités telles que l'accès non autorisé à des fichiers ou répertoires, la désérialisation de données non fiables, la falsification de requêtes côté serveur et le déni de service.

**Points Clés et Vulnérabilités Identifiées :**

*   **Accès Non Autorisé à des Fichiers ou Répertoires :** Permet à un attaquant d'inclure des fichiers arbitraires dans le PDF généré, y compris des documents sensibles ou des fichiers système.
    *   **Exemples de CVE :** GHSA-57f3-gghm-9mhc, CVE-2021-23353, CVE-2025-29907, CVE-2025-57810.
    *   **Techniques d'Exploitation :** Exploitation de la traversée de répertoire (path traversal) via les attributs `xlink:href` ou `src` dans les tags `<img>` ou `svg`, utilisation de schémas `file://`, ou traversée de chemin dans la gestion des annotations et des watermarks.
*   **Falsification de Requêtes Côté Serveur (SSRF) :** Permet à un attaquant d'initier des requêtes depuis le serveur vers d'autres ressources, y compris des réseaux internes non accessibles publiquement.
    *   **Exemples :** Des bibliothèques comme TCPDF, spipu/html2pdf, KnpLabs/snappy, mpdf/mpdf, dompdf/dompdf et LibrePDF/OpenPDF peuvent être amenées à faire des requêtes réseau via les tags `<img>`, `<iframe>`, ou des propriétés CSS comme `background-image`.
    *   **Techniques d'Exploitation :** Utilisation de `file_get_contents`, `getimagesize`, `curl_exec` et d'autres fonctions d'accès aux ressources lorsque des URL sont spécifiées dans le contenu HTML.
*   **Désérialisation de Données Non Fiables :** Une désérialisation non sécurisée, notamment via les archives PHAR ou des chaînes POP (Property Oriented Programming), peut permettre à un attaquant de supprimer des fichiers arbitraires sur le système ou d'exécuter du code.
    *   **Exemples :** Trouvé dans TCPDF et spipu/html2pdf.
*   **Déni de Service (DoS) :** Des expressions régulières mal conçues (ReDoS) ou des boucles avec des conditions de sortie inatteignables peuvent épuiser les ressources du serveur, le rendant indisponible.
    *   **Exemples :** Détecté dans jsPDF.
*   **Exécution de Code à Distance (RCE) :** La configuration de certaines bibliothèques peut permettre l'exécution de code PHP embarqué directement dans le HTML.
    *   **Exemple :** Détecté dans dompdf/dompdf avec l'option `isPhpEnabled`.

**Comportements Intentionnels et Misconfigurations :**

Certaines bibliothèques traitent des fonctionnalités comme l'accès aux fichiers locaux ou les requêtes réseau comme des comportements intentionnels, les déplaçant de la catégorie des vulnérabilités aux configurations à surveiller attentivement. Des misconfigurations, comme l'activation de `allowAnnotationFiles` ou `showWatermarkImage` dans mpdf/mpdf, ou un `chroot` mal configuré dans dompdf/dompdf, peuvent également mener à des scénarios dangereux.

**Recommandations pour les Développeurs :**

1.  **Maintenir les Bibliothèques à Jour :** Assurez-vous que toutes les bibliothèques de génération PDF utilisées sont dans leurs dernières versions stables pour bénéficier des correctifs de sécurité.
2.  **Sanitiser l'Entrée Utilisateur :** Ne faites jamais confiance aux données fournies par l'utilisateur. Validez et nettoyez rigoureusement tout contenu HTML avant de le passer à une bibliothèque de génération PDF.
3.  **Configurer Sécuritairement :** Examinez attentivement les options de configuration des bibliothèques. Désactivez les fonctionnalités potentiellement dangereuses comme l'exécution de PHP embarqué ou l'accès aux fichiers locaux si elles ne sont pas strictement nécessaires. Limitez l'accès aux hôtes distants via des listes blanches lorsque SSRF est possible.
4.  **Surveiller les Signatures des Bibliothèques :** Identifiez la bibliothèque utilisée pour générer les PDFs (souvent visible dans les propriétés du document) et recherchez les vulnérabilités connues pour cette bibliothèque et sa version spécifique.
5.  **Comprendre les Comportements Intentionnels :** Soyez conscient des fonctionnalités qui pourraient être exploitées, même si elles sont considérées comme intentionnelles par les développeurs de la bibliothèque (ex: accès aux images locales, SSRF). Implémentez des mesures de sécurité supplémentaires au niveau de votre application.

---
[Source](https://swarm.ptsecurity.com/blind-trust-what-is-hidden-behind-the-process-of-creating-your-pdf-file/){:target="_blank"}
