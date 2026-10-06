---
title: 'Rejetto HFS servers now actively scanned for critical RCE flaw'
date: 2026-10-06
permalink: /posts/2026/10/06/rejetto-hfs-servers-now-actively-scanned-for-critical-rce-flaw/
tags:
- veille-cyber
- bleepingcomp
---
### Menace critique sur Rejetto HFS : Exploitation active d'une faille RCE

Les serveurs Rejetto HFS font actuellement l'objet de tentatives d'analyse et d'exploitation actives. Cette vulnérabilité permet à un attaquant non authentifié de forger des cookies de session administrateur, entraînant une prise de contrôle totale du système et l'exécution de code à distance (RCE).

**Points clés :**
*   **Origine de la faille :** Identifiée par les chercheurs d'Horizon3 via l'utilisation du modèle d'IA "Mythos", qui a mis en évidence une chaîne d'exploitation liant un générateur de nombres aléatoires non cryptographique à une fuite d'informations.
*   **Activité observée :** Des tentatives de reconnaissance ont été détectées, ciblant des serveurs aux États-Unis et au Japon.
*   **Risques :** Accès illégitime aux fichiers, installation de logiciels malveillants, vol de données ou pivot vers le réseau interne de la victime.

**Vulnérabilité :**
*   **CVE-2026-61500 :** Faiblesse dans la génération et la divulgation de la clé de signature des cookies de session dans Rejetto HFS versions 3.0.0 à 3.2.0.

**Recommandations :**
*   **Mise à jour immédiate :** Passer impérativement à la version 3.2.1 minimum.
*   **Version recommandée :** Installer la version stable la plus récente (3.3.4) pour bénéficier des derniers correctifs de sécurité.

---
[Source](https://www.bleepingcomputer.com/news/security/rejetto-hfs-servers-now-actively-scanned-for-critical-rce-flaw/){:target="_blank"}
