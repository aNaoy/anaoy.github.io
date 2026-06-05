---
title: 'Hola Browser for Windows compromised to deliver cryptominer'
date: 2026-06-05
permalink: /posts/2026/06/05/hola-browser-for-windows-compromised-to-deliver-cryptominer/
tags:
- veille-cyber
- bleepingcomp
---
### Compromission de la chaîne d'approvisionnement de Hola Browser

La version Windows du navigateur Hola a été victime d'une attaque par chaîne d'approvisionnement, injectant un logiciel malveillant à l'insu de l'éditeur. La menace a été détectée lors de tests de certification effectués par AppEsteem.

**Points clés :**
* **Nature de l'attaque :** Un exécutable non déclaré, nommé `me.exe`, était intégré au logiciel.
* **Fonctionnalité malveillante :** Le binaire a été identifié comme un mineur de cryptomonnaie (Monero).
* **Persistance :** Le malware crée une exclusion dans Windows Defender, se copie sous le nom `HolaMonitorService.exe` et installe un service automatique (`hola_monitor_svc`) qui s'exécute lorsque l'ordinateur est inactif.
* **Impact limité :** Hola affirme que seulement 0,1 % de sa base d'utilisateurs a été touchée et nie toute fuite de données personnelles.

**Vulnérabilités :**
* Aucune CVE n'est associée à cet incident, car il s'agit d'une compromission de l'infrastructure de distribution (chaîne d'approvisionnement) et non d'une faille logicielle exploitée par des tiers sur les machines des utilisateurs. Le fichier malveillant n'était ni signé numériquement, ni horodaté, et utilisait du code obfusqué.

**Recommandations :**
* **Pour l'éditeur :** Hola a procédé à une reconstruction complète de son pipeline de distribution, renforcé la vérification des signatures de code, mis en place des contrôles d'accès stricts et instauré une surveillance continue de l'infrastructure.
* **Pour les utilisateurs :** En cas de doute, vérifier la présence du service `hola_monitor_svc` ou de l'exécutable `HolaMonitorService.exe` dans le dossier `C:\Program Files\Hola\` et supprimer ces éléments si nécessaire. Il est conseillé de maintenir ses logiciels à jour et d'effectuer une analyse complète avec une solution antivirus robuste.

---
[Source](https://www.bleepingcomputer.com/news/security/hola-browser-for-windows-compromised-to-deliver-cryptominer/){:target="_blank"}
