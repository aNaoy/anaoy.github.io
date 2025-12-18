---
title: 'Libbiosig, Grassroot DiCoM, Smallstep step-ca vulnerabilities'
date: 2025-12-18
permalink: /posts/2025/12/18/libbiosig-grassroot-dicom-smallstep-step-ca-vulnerabilities/
tags:
- veille-cyber
- zerodaysfans
---
**Alertes de Sécurité : Libbiosig, Grassroot DiCoM et Smallstep step-ca**

Des failles de sécurité ont été identifiées dans les logiciels suivants : Libbiosig, Grassroot DiCoM et Smallstep step-ca. Ces vulnérabilités ont été découvertes par l'équipe de recherche de Cisco Talos.

**Points Clés :**

*   **Libbiosig :** Plusieurs vulnérabilités de débordement de tampon basé sur la pile ont été trouvées dans la fonctionnalité de parsing MFER de la version 3.9.1 de libbiosig. La manipulation d'un fichier MFER spécialement conçu peut permettre à un attaquant d'exécuter du code arbitraire.
    *   **Vulnérabilités (avec CVE) :** TALOS-2025-2296 (CVE-2025-66043 à CVE-2025-66048)
    *   **Recommandations :** Mettre à jour vers une version corrigée de libbiosig.

*   **Grassroot DiCoM :** Trois vulnérabilités de lecture hors limites ont été détectées dans cette bibliothèque de traitement de fichiers DICOM. La soumission d'un fichier malveillant peut déclencher ces failles.
    *   **Vulnérabilités (avec CVE) :**
        *   TALOS-2025-2210 (CVE-2025-53618, CVE-2025-53619) : Fuite d'informations.
        *   TALOS-2025-2211 (CVE-2025-52582) : Fuite d'informations.
        *   TALOS-2025-2214 (CVE-2025-48429) : Fuite de données du tas (heap).
    *   **Recommandations :** Ces vulnérabilités sont considérées comme des "zero-days" et nécessitent une vigilance accrue et des mesures d'atténuation spécifiques en attendant les correctifs.

*   **Smallstep step-ca :** Une vulnérabilité de contournement d'authentification a été découverte dans step-ca, une autorité de certification en ligne pour la gestion de certificats X.509 et SSH. Un attaquant peut exploiter cette faille pour créer des certificats sans respecter les vérifications d'autorisation du protocole.
    *   **Vulnérabilités (avec CVE) :** TALOS-2025-2242 (CVE-2025-44005)
    *   **Recommandations :** Mettre à jour step-ca vers une version corrigée.

Les fournisseurs concernés ont publié des correctifs pour la plupart de ces vulnérabilités, conformément à la politique de divulgation de Cisco. Des règles Snort sont disponibles pour détecter les tentatives d'exploitation.

---
[Source](https://blog.talosintelligence.com/libbiosig-grassroot-dicom-smallstep-step-ca-vulnerabilities/){:target="_blank"}
