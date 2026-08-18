---
title: 'Clop created custom web shell for Windchill data theft attacks'
date: 2026-08-18
permalink: /posts/2026/08/18/clop-created-custom-web-shell-for-windchill-data-theft-attacks/
tags:
- veille-cyber
- bleepingcomp
---
### Menace Clop : Web shell sur mesure pour les serveurs PTC Windchill

Le groupe de ransomware Clop a développé un *web shell* Java hautement spécialisé pour cibler les serveurs PTC Windchill et FlexPLM. Contrairement aux outils génériques, ce logiciel malveillant exploite les API internes et le schéma de base de données de Windchill pour automatiser le vol de données, le déchiffrement d'identifiants et l'énumération de fichiers sensibles.

**Points clés :**
*   **Mode opératoire :** Le *web shell* utilise les classes natives de l'application (ex: `MethodContext`, `WTConnection`), permettant aux requêtes malveillantes de s'exécuter avec les privilèges légitimes du service, rendant la détection par logs de base de données complexe.
*   **Commandes spécifiques :** L'outil est piloté via des en-têtes HTTP personnalisés (`X-windchill-req`) et permet, entre autres, de déchiffrer des mots de passe LDAP, de cartographier les coffres-forts de fichiers et d'exécuter du bytecode Java en mémoire.
*   **Attribution :** La campagne est liée au groupe Clop via les techniques d'extorsion observées et l'utilisation d'infrastructures de communication déjà connues pour leurs campagnes précédentes (MOVEit, GoAnywhere).

**Vulnérabilité exploitée :**
*   **CVE-2026-12569 :** Vulnérabilité critique d'exécution de code à distance (RCE) affectant PTC Windchill. Elle est activement exploitée et figure au catalogue des vulnérabilités connues (KEV) de la CISA.

**Recommandations :**
*   **Correction immédiate :** Appliquer sans délai les correctifs de sécurité fournis par PTC (disponibles depuis le 17 juin).
*   **Détection :** Rechercher la présence de fichiers JSP suspects dans les répertoires Windchill, en prêtant une attention particulière à ceux contenant des références à l'en-tête `X-windchill-req`.
*   **Remédiation post-compromission :** En cas d'intrusion avérée, réinitialiser immédiatement le mot de passe du gestionnaire LDAP ainsi que l'ensemble des identifiants d'accès à l'application Windchill, ces derniers devant être considérés comme compromis.

---
[Source](https://www.bleepingcomputer.com/news/security/clop-created-custom-web-shell-for-windchill-data-theft-attacks/){:target="_blank"}
