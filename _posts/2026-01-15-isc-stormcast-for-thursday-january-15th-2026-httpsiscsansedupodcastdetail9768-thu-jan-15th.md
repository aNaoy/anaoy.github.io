---
title: 'ISC Stormcast For Thursday, January 15th, 2026 https://isc.sans.edu/podcastdetail/9768, (Thu, Jan 15th)'
date: 2026-01-15
permalink: /posts/2026/01/15/isc-stormcast-for-thursday-january-15th-2026-httpsiscsansedupodcastdetail9768-thu-jan-15th/
tags:
- veille-cyber
- sans-isc
---
### Alerte de Sécurité : Exploitation des Vulnérabilités SMBv1

Les systèmes utilisant le protocole SMBv1 sont particulièrement exposés, notamment en raison de vulnérabilités connues qui ne sont pas systématiquement corrigées. L'une des failles les plus notables est **CVE-2017-0143**, liée à l'exploitation de la façon dont SMBv1 traite des paquets malveillants, permettant à un attaquant distant d'exécuter du code arbitraire. D'autres vulnérabilités dans SMBv1 ont également été identifiées, facilitant des attaques par déni de service ou l'élévation de privilèges.

**Points Clés :**

*   Le protocole SMBv1 est obsolète et présente des risques de sécurité significatifs.
*   Des vulnérabilités critiques (ex: CVE-2017-0143) permettent l'exécution de code à distance.
*   De nombreux systèmes, en particulier dans les environnements d'entreprise, utilisent encore SMBv1 par défaut ou par compatibilité.

**Vulnérabilités Principales :**

*   **CVE-2017-0143** : Permet l'exécution de code à distance.
*   Autres vulnérabilités SMBv1 affectant la gestion des paquets, potentiellement exploitables pour des dénis de service ou l'élévation de privilèges.

**Recommandations :**

*   **Désactiver SMBv1** sur tous les systèmes et passer à SMBv2 ou SMBv3. Cette action est cruciale pour éliminer la surface d'attaque.
*   **Mettre à jour les systèmes** avec les derniers correctifs de sécurité pour atténuer les risques associés aux versions antérieures de SMB ou à d'autres protocoles vulnérables.
*   **Surveiller activement le trafic réseau** pour détecter toute activité suspecte liée aux protocoles SMB.

---
[Source](https://isc.sans.edu/diary/rss/32630){:target="_blank"}
