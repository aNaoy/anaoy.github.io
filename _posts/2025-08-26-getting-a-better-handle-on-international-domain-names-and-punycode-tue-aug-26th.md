---
title: 'Getting a Better Handle on International Domain Names and Punycode, (Tue, Aug 26th)'
date: 2025-08-26
permalink: /posts/2025/08/26/getting-a-better-handle-on-international-domain-names-and-punycode-tue-aug-26th/
tags:
- veille-cyber
- sans-isc
---
### Comprendre les Noms de Domaine Internationaux et le Punycode

Les noms de domaine internationaux (IDN) permettent d'utiliser des caractères non latins dans les adresses web. Lorsqu'ils sont traités dans le système DNS, ils sont encodés en Punycode, reconnaissable à son préfixe "xn--".

**Anomalies Potentielles et Détection :**

*   **Punycode Invalide :** Le processus d'encodage peut parfois générer des domaines Punycode non conformes au standard RFC 3492.
*   **Scripts Mixtes :** Une préoccupation majeure est l'utilisation de caractères provenant de différents systèmes d'écriture (scripts) au sein d'un même nom de domaine. Si les navigateurs modernes tendent à afficher ces noms avec prudence, leur analyse révèle des mélanges de scripts. Des outils, comme le module Python `unicodedata2`, permettent d'identifier le script d'un caractère (par exemple, en examinant la première partie de son nom Unicode). Un nom de domaine légitime est généralement censé utiliser un seul script.

**Points Clés :**

*   Les noms de domaine internationaux sont encodés en Punycode avec le préfixe "xn--".
*   Il est possible de rencontrer des anomalies comme un Punycode invalide ou un mélange de scripts au sein d'un domaine.
*   L'identification du script d'un caractère peut se faire via des modules Python comme `unicodedata2`.
*   Un mélange de scripts dans un nom de domaine est suspect, les noms légitimes tendant à se limiter à un seul langage/script.

**Vulnérabilités :**

Aucune vulnérabilité spécifique avec un identifiant CVE n'est mentionnée dans ce texte.

**Recommandations :**

*   Lors de l'analyse du trafic DNS, soyez attentif aux domaines encodés en Punycode.
*   Utilisez des outils, tels que des modules Python, pour détecter les domaines Punycode invalides et ceux contenant des scripts mixtes.
*   Soyez particulièrement vigilant face aux noms de domaine mélangeant différents systèmes d'écriture.

---
[Source](https://isc.sans.edu/diary/rss/32234){:target="_blank"}
