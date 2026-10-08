---
title: 'Hackers hijack Google domains after breaching ccTLD registries'
date: 2026-10-08
permalink: /posts/2026/10/08/hackers-hijack-google-domains-after-breaching-cctld-registries/
tags:
- veille-cyber
- bleepingcomp
---
### Détournement de domaines via la compromission de registres ccTLD

Des attaquants ont compromis des registres de domaines de premier niveau nationaux (.GH pour le Ghana, .SL pour la Sierra Leone, .AS pour les Samoa américaines), leur permettant de modifier les enregistrements DNS faisant autorité. Cette manœuvre a permis de rediriger le trafic vers des infrastructures malveillantes et d'obtenir des certificats HTTPS légitimes par le biais de la validation par enregistrements TXT, facilitant ainsi l'usurpation d'identité de marques et de services mondiaux. Google a précisé que ses propres infrastructures n'étaient pas compromises, l'attaque ciblant la chaîne de gestion des domaines tiers.

**Points clés :**
*   **Méthode d'attaque :** Compromission du registre DNS, détournement du trafic vers des serveurs contrôlés par l'attaquant, et génération de certificats TLS valides.
*   **Impact :** Usurpation d'identité de Google et d'autres grandes organisations. Les certificats frauduleux ont été émis légitimement par des autorités de certification (CA) dupées par le contrôle DNS.
*   **Réponse :** Google a utilisé son mécanisme « CRLSets » dans Chrome pour révoquer et bloquer préventivement les certificats identifiés via l'analyse des logs *Certificate Transparency* (CT).
*   **Vulnérabilités :** L'incident ne fait pas l'objet d'une CVE spécifique, car il repose sur une faille opérationnelle au niveau de la gestion des registres DNS (n'impliquant pas un logiciel spécifique) et sur la confiance accordée au processus de validation par enregistrements TXT.

**Recommandations :**
*   **Surveillance active :** Contrôler régulièrement les journaux de *Certificate Transparency* (CT) pour l'ensemble du portefeuille de noms de domaine, y compris les domaines parqués.
*   **Durcissement DNS :** Publier des enregistrements CAA (Certification Authority Authorization) restrictifs afin de limiter la capacité des autorités de certification à émettre des certificats pour vos domaines, même en cas de détournement DNS temporaire.
*   **Limites de protection :** Garder à l'esprit que les interventions de type « CRLSets » sont spécifiques à Chrome ; les utilisateurs d'autres navigateurs pourraient rester exposés aux domaines détournés non identifiés.

---
[Source](https://www.bleepingcomputer.com/news/security/hackers-hijack-google-domains-after-breaching-cctld-registries/){:target="_blank"}
