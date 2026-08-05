---
title: 'Veeam, Terraform MCP, Django Patch Critical Flaws, Led by CVSS 10.0 Cross-Tenant Bug'
date: 2026-08-05
permalink: /posts/2026/08/05/veeam-terraform-mcp-django-patch-critical-flaws-led-by-cvss-100-cross-tenant-bug/
tags:
- veille-cyber
- hackernews
---
### Failles critiques : Alertes de sécurité sur Veeam, Terraform et Django

Des correctifs ont été publiés pour 11 vulnérabilités affectant Veeam Service Provider Console, HashiCorp Terraform MCP Server et le framework Django. Aucune exploitation active n'a été signalée à ce jour.

#### Points clés par technologie

**Veeam Service Provider Console (VSPC)**
*   **Vulnérabilités :**
    *   **CVE-2026-58073 (CVSS 9.5) :** Permet à un attaquant non authentifié d'usurper l'identité d'un agent géré et de récupérer ses identifiants.
    *   **CVE-2026-58072 (CVSS 9.0) :** Écriture arbitraire de fichiers sur le serveur de gestion, pouvant mener à une exécution de code à distance (RCE) via un compte à faible privilège.
    *   **CVE-2026-58067 & CVE-2026-58071 :** Déni de service et exposition d'API.
*   **Recommandation :** Mettre à jour vers la version **9.3.0.35057**.

**HashiCorp Terraform MCP Server**
*   **Vulnérabilités :**
    *   **CVE-2026-16498 (CVSS 10.0) :** Faille d'isolation cross-tenant dans le mode stateless HTTP. Des jetons Terraform peuvent être réutilisés par d'autres utilisateurs.
    *   **CVE-2026-16496 (CVSS 8.9) :** Problème similaire en mode stateful (défaut).
    *   **CVE-2026-14869 (CVSS 8.6) :** Faille de falsification de requête côté serveur (SSRF).
*   **Recommandation :** Mettre à jour vers la version **1.1.0 ou ultérieure**. Restreindre l'accès réseau au listener HTTP aux seuls utilisateurs de confiance.

**Django**
*   **Vulnérabilité majeure :**
    *   **CVE-2026-15307 :** Vulnérabilité dans GeoDjango permettant, via des lookups spatiaux, l'écriture de fichiers sur le disque et potentiellement une exécution de code (nécessite un accès compte staff).
*   **Autres failles :** CVE-2026-15920 (XSS), CVE-2026-15830 (DoS), CVE-2026-15337 (DoS).
*   **Recommandation :** Mettre à jour vers les versions **6.0.8 ou 5.2.17**. Notez que le correctif de GeoDjango introduit une rupture de compatibilité ascendante.

---
[Source](https://thehackernews.com/2026/08/veeam-terraform-mcp-django-patch.html){:target="_blank"}
