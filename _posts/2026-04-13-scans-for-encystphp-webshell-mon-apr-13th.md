---
title: 'Scans for EncystPHP Webshell, (Mon, Apr 13th)'
date: 2026-04-13
permalink: /posts/2026/04/13/scans-for-encystphp-webshell-mon-apr-13th/
tags:
- veille-cyber
- sans-isc
---
### Recrudescence des scans pour le Webshell EncystPHP sur FreePBX

Les attaquants intensifient leurs tentatives d'exploitation des systèmes FreePBX via le déploiement du webshell **EncystPHP**. Contrairement aux outils standards, ce dernier utilise une chaîne de caractères codée en dur agissant comme mot de passe, souvent déguisée en empreinte MD5, pour restreindre l'accès à l'interface de contrôle.

**Points clés :**
*   **Mode opératoire :** Les attaquants ciblent les installations FreePBX pour injecter le webshell, puis exécutent des scripts distants (via `wget`) pour installer des backdoors.
*   **Persistance :** Une fois le système compromis, l'attaquant ajoute de multiples comptes utilisateurs avec des mots de passe prédéfinis pour garantir un accès persistant.
*   **Infrastructure :** Les scans observés proviennent actuellement d'adresses IP situées aux Pays-Bas (ex: `160.119.76.250`), hébergeant des serveurs web non configurés.

**Vulnérabilités :**
L'article pointe vers des failles d'injection et d'exécution de code à distance (RCE) au sein de FreePBX, exploitant notamment des points d'entrée tels que `/admin/modules/phones/ajax.php` et `/restapps/applications.php`. Bien qu'aucune CVE spécifique ne soit citée, ces vecteurs sont bien documentés comme étant utilisés pour le déploiement massif de ce malware.

**Recommandations :**
*   **Audit des comptes :** Inspectez immédiatement votre système FreePBX à la recherche de comptes suspects. Les attaquants créent fréquemment des utilisateurs comme `hima`, `sugarmaint`, `spamfilter`, `juba`, ou modifient les mots de passe des comptes système (`root`, `asterisk`).
*   **Veille et mise à jour :** Appliquez systématiquement les correctifs de sécurité fournis par l'éditeur pour FreePBX afin de fermer les vulnérabilités exploitées par le webshell EncystPHP.
*   **Surveillance réseau :** Surveillez les logs pour détecter des requêtes GET suspectes contenant des paramètres `md5` ou des appels système (`system()`, `wget`) vers des serveurs externes inconnus.

---
[Source](https://isc.sans.edu/diary/rss/32892){:target="_blank"}
