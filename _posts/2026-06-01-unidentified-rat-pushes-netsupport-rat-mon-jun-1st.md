---
title: 'Unidentified RAT pushes NetSupport RAT, (Mon, Jun 1st)'
date: 2026-06-01
permalink: /posts/2026/06/01/unidentified-rat-pushes-netsupport-rat-mon-jun-1st/
tags:
- veille-cyber
- sans-isc
---
### Analyse de la campagne malveillante SmartApeSG et NetSupport RAT

La campagne « SmartApeSG », utilisant la technique « ClickFix », propage un RAT (Remote Access Trojan) initial non identifié sur les systèmes Windows. Ce malware sert de vecteur pour télécharger et installer une charge utile secondaire : le célèbre NetSupport Manager RAT.

**Points clés :**
*   **Mode opératoire :** L'attaque commence par une fausse page de vérification incitant l'utilisateur à exécuter des instructions « ClickFix ».
*   **Persistance :** L'infection initiale déploie des scripts (`processor.vbs`, `token.bat`) qui extraient un fichier CAB (`setup.cab`), installent NetSupport RAT, puis s'auto-suppriment pour effacer leurs traces.
*   **Infrastructure C2 :** 
    *   Le RAT initial communique via TCP port 443 (trafic non chiffré) avec l'IP `89.110.110.119`.
    *   NetSupport RAT communique avec le serveur `185.163.47.217` sur le port 443.
*   **Évolutivité :** Les indicateurs de compromission (domaines, hashs) sont hautement dynamiques et changent quotidiennement.

**Vulnérabilités :**
*   L'article n'identifie pas de CVE spécifique exploitée ; il s'agit d'une attaque basée sur l'ingénierie sociale (ClickFix) exploitant la confiance de l'utilisateur pour exécuter des scripts malveillants.

**Recommandations :**
*   **Sensibilisation :** Former les utilisateurs à la méfiance envers les pages web demandant d'exécuter des scripts ou de copier-coller des commandes dans un terminal (« ClickFix »).
*   **Filtrage réseau :** Bloquer les connexions sortantes vers les adresses IP suspectes et surveiller le trafic TCP 443 ne correspondant pas au protocole HTTPS standard.
*   **Surveillance système :** Surveiller la création de fichiers et l'exécution de scripts dans `C:\ProgramData\`, notamment les fichiers `.vbs` et `.bat` suspects.
*   **Veille active :** Étant donné le caractère éphémère des indicateurs, suivre des sources spécialisées comme le flux Mastodon `@monitorsg` pour obtenir les IOC les plus récents.

---
[Source](https://isc.sans.edu/diary/rss/33034){:target="_blank"}
