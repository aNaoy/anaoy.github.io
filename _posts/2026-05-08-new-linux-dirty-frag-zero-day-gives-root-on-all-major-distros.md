---
title: 'New Linux Dirty Frag zero-day gives root on all major distros'
date: 2026-05-08
permalink: /posts/2026/05/08/new-linux-dirty-frag-zero-day-gives-root-on-all-major-distros/
tags:
- veille-cyber
- bleepingcomp
---
### Découverte de la faille Linux « Dirty Frag » : une escalade de privilèges critique

Une nouvelle vulnérabilité zero-day, baptisée **Dirty Frag**, permet à un attaquant local d'obtenir des privilèges root sur la plupart des distributions Linux majeures (Ubuntu, RHEL, CentOS, Fedora, etc.). Cette faille, présente depuis environ neuf ans dans l'interface cryptographique `algif_aead` du noyau Linux, permet de modifier des fichiers système protégés en mémoire. Contrairement à d'autres vulnérabilités similaires, il s'agit d'un bug de logique déterministe qui ne nécessite pas de condition de concurrence (*race condition*), garantissant un taux de réussite très élevé.

**Points clés :**
*   **Mécanisme :** Enchaînement de deux vulnérabilités distinctes d'écriture dans le cache de pages (Page-Cache Write).
*   **Impact :** Élévation immédiate de privilèges (obtention des droits root).
*   **Disponibilité :** Un PoC (preuve de concept) public est disponible, suite à la rupture de l'embargo initial.
*   **Absence de correctif :** Au moment de la divulgation, aucun patch n'est disponible.

**Vulnérabilités associées :**
*   **CVE-2026-43284 :** Vulnérabilité d'écriture dans le cache de pages liée à `xfrm-ESP`.
*   **CVE-2026-43500 :** Vulnérabilité d'écriture dans le cache de pages liée à `RxRPC`.

**Recommandations :**
En attendant la publication de correctifs officiels, il est possible d'atténuer le risque en désactivant les modules noyau vulnérables (`esp4`, `esp6` et `rxrpc`) via la commande suivante :

```bash
sh -c "printf 'install esp4 /bin/false
install esp6 /bin/false
install rxrpc /bin/false
' > /etc/modprobe.d/dirtyfrag.conf; rmmod esp4 esp6 rxrpc 2>/dev/null; true"
```
*Note : Cette mesure entraînera l'interruption du fonctionnement des VPN IPsec et des systèmes de fichiers réseau AFS.*

---
[Source](https://www.bleepingcomputer.com/news/security/new-linux-dirty-frag-zero-day-with-poc-exploit-gives-root-privileges/){:target="_blank"}
