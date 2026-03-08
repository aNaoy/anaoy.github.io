---
title: 'Hackers abuse .arpa DNS and ipv6 to evade phishing defenses'
date: 2026-03-08
permalink: /posts/2026/03/08/hackers-abuse-arpa-dns-and-ipv6-to-evade-phishing-defenses/
tags:
- veille-cyber
- bleepingcomp
---
### Détournement des domaines .arpa et IPv6 pour contourner les défenses anti-phishing

Des cybercriminels exploitent actuellement le domaine de premier niveau `.arpa`, réservé à l'infrastructure réseau (notamment pour les résolutions DNS inversées), afin de masquer des campagnes de phishing et échapper aux passerelles de sécurité.

**Points clés :**
*   **Abus du DNS inversé :** Les attaquants obtiennent des blocs d'adresses IPv6 et configurent des enregistrements DNS (type A) sur leurs zones `ip6.arpa`, détournant ainsi une fonctionnalité d'infrastructure légitime pour héberger des liens malveillants.
*   **Contournement de la réputation :** L'utilisation de fournisseurs DNS réputés (comme Cloudflare ou Hurricane Electric) et l'absence de données WHOIS ou d'historique de domaine propre au `.arpa` permettent de tromper les outils de filtrage automatique.
*   **Techniques combinées :** Les attaquants utilisent des systèmes de distribution de trafic (TDS) pour valider leurs cibles et alternent avec d'autres méthodes comme le détournement de CNAME (*dangling CNAME*) et le *subdomain shadowing*.
*   **Éphémérité :** Les liens sont activés sur une très courte durée pour entraver l'analyse par les chercheurs en sécurité.

**Vulnérabilités :**
*   Il n'existe pas de vulnérabilité logicielle spécifique (CVE) unique, mais plutôt une **faille de configuration et de validation** chez certains fournisseurs DNS qui autorisent la création d'enregistrements (autres que PTR) dans les zones de recherche inversée IPv6.

**Recommandations :**
*   **Renforcement du filtrage DNS :** Les administrateurs de sécurité doivent examiner les politiques de leurs fournisseurs DNS pour bloquer la création d'enregistrements non destinés au routage inverse dans les zones `.arpa`.
*   **Vigilance accrue :** Sensibiliser les utilisateurs à la méfiance envers les liens suspects et privilégier l'accès direct aux services officiels via le navigateur plutôt que de cliquer sur des images ou des liens intégrés dans des emails.
*   **Détection comportementale :** Mettre en place des solutions capables d'analyser le comportement des URLs lors du clic (via un *sandbox* ou une analyse de redirection) plutôt que de se baser uniquement sur la réputation du domaine.

---
[Source](https://www.bleepingcomputer.com/news/security/hackers-abuse-arpa-dns-and-ipv6-to-evade-phishing-defenses/){:target="_blank"}
