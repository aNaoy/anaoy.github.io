---
title: 'Predator spyware hooks iOS SpringBoard to hide mic, camera activity'
date: 2026-02-21
permalink: /posts/2026/02/21/predator-spyware-hooks-ios-springboard-to-hide-mic-camera-activity/
tags:
- veille-cyber
- bleepingcomp
---
**Predator : Le logiciel espion qui neutralise les indicateurs d'activité de votre iPhone**

Le logiciel malveillant Predator, développé par la société de surveillance Intellexa, est capable de masquer les indicateurs d'activité du microphone et de la caméra sur les appareils iOS. Cette fonctionnalité permet aux opérateurs de Predator de diffuser secrètement des flux audio et vidéo sans que l'utilisateur ne s'en rende compte.

Le fonctionnement de cette dissimulation repose sur l'exploitation d'un accès de niveau noyau précédemment obtenu par le logiciel espion. Predator ne tire pas parti de vulnérabilités logicielles spécifiques à iOS pour masquer son activité. Il détourne plutôt les indicateurs système introduits dans iOS 14 (le point vert pour la caméra, le point orange pour le microphone) directement au niveau de l'interface utilisateur.

Des chercheurs ont analysé le processus : Predator injecte une fonction dans "SpringBoard", le processus principal d'iOS, qui intercepte les appels du système lorsque l'activité des capteurs change. En "accrochant" (hooking) une méthode spécifique (_handleNewDomainData:), Predator empêche les informations sur l'activation de la caméra ou du microphone d'atteindre la couche d'affichage de l'interface utilisateur. Cela se fait en annulant l'objet responsable des mises à jour d'activité des capteurs (SBSensorActivityDataProvider), qui, dans le langage Objective-C, ignore silencieusement les appels à un objet nul. Cette approche permet de masquer à la fois les indicateurs de la caméra et du microphone avec une seule modification. Des traces de code suggèrent une tentative antérieure d'intercepter directement le gestionnaire d'indicateurs d'enregistrement, mais cette méthode semble avoir été abandonnée.

Pour l'accès à la caméra, un module distinct utilise des techniques de correspondance de modèles d'instructions et de redirection de code pour contourner les vérifications d'autorisations.

Bien que les chercheurs aient identifié des signes techniques de processus malveillants tels que des mappages mémoire inattendus ou des ports d'exception, l'absence d'indicateurs visuels rend l'activité de Predator particulièrement insidieuse pour l'utilisateur moyen.

**Points clés :**

*   Predator masque les indicateurs d'utilisation de la caméra et du microphone sur iOS.
*   Il exploite un accès de niveau noyau préexistant pour détourner les indicateurs système.
*   Le mécanisme implique une interception des mises à jour d'activité des capteurs dans SpringBoard.
*   Cette méthode neutralise les indicateurs verts (caméra) et oranges (microphone).

**Vulnérabilités :**

*   Aucune vulnérabilité logicielle iOS spécifique n'est exploitée pour le masquage des indicateurs. Le logiciel espion s'appuie sur un accès de niveau noyau déjà obtenu.
*   L'article mentionne que Predator a été livré via des attaques exploitant des failles "zero-day" (non corrigées) dans Apple et Chrome, ainsi que via des mécanismes d'infection "0-click". Les CVE spécifiques ne sont pas fournies dans cet extrait.

**Recommandations :**

*   Bien que l'article se concentre sur le fonctionnement du logiciel espion, l'implication est que les utilisateurs devraient être vigilants face à des signes potentiels de compromission (mentionnés comme des mappings mémoire inattendus, des ports d'exception, des points d'arrêt, etc.).
*   Maintenir les systèmes d'exploitation et les applications à jour est crucial pour se prémunir contre l'exploitation de vulnérabilités "zero-day".
*   L'utilisation de solutions de gestion des appareils mobiles (MDM) peut aider à détecter des comportements anormaux sur les appareils.

---
[Source](https://www.bleepingcomputer.com/news/security/predator-spyware-hooks-ios-springboard-to-hide-mic-camera-activity/){:target="_blank"}
