---
title: 'Simple bypass of the link preview function in Outlook Junk folder, (Thu, May 14th)'
date: 2026-05-14
permalink: /posts/2026/05/14/simple-bypass-of-the-link-preview-function-in-outlook-junk-folder-thu-may-14th/
tags:
- veille-cyber
- sans-isc
---
### Contournement de la prévisualisation des liens dans le dossier Courrier indésirable d'Outlook

Le dossier « Courrier indésirable » d'Outlook est une mesure de sécurité utile qui supprime le formatage des e-mails pour afficher les URL réelles des liens, permettant ainsi d'inspecter les messages suspects. Cependant, cette fonctionnalité présente une faille de conception qui permet à des attaquants de dissimuler des liens malveillants.

**Points clés :**
* La prévisualisation des liens dans le dossier indésirable repose sur l'analyse syntaxique des balises `HREF`.
* Un lien peut être rendu invisible par cette fonction si son URI est syntaxiquement invalide (absence de schéma/protocole, comme `http://` ou `https://`).
* Malgré cette invisibilité dans le dossier indésirable, le lien reste parfaitement fonctionnel et cliquable une fois le message déplacé dans un autre dossier.

**Vulnérabilités :**
* Aucune CVE associée (comportement lié à une limitation de l'analyseur syntaxique d'Outlook). La vulnérabilité réside dans la confiance accordée au mécanisme de « nettoyage » du dossier indésirable, qui échoue à normaliser ou révéler les liens dont le protocole est absent.

**Recommandations :**
* Ne pas considérer le dossier « Courrier indésirable » comme un environnement d'analyse infaillible pour inspecter les liens suspects.
* Sensibiliser les utilisateurs au fait qu'un lien caché ou absent dans ce dossier peut toujours être actif et dangereux.
* Privilégier des outils d'analyse d'URL externes (sandboxes ou services de réputation) pour examiner les liens suspects plutôt que de se fier uniquement à l'affichage d'Outlook.

---
[Source](https://isc.sans.edu/diary/rss/32990){:target="_blank"}
