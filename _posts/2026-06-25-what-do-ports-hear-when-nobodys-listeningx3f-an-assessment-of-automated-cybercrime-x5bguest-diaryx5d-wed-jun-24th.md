---
title: 'What do Ports Hear When Nobodys Listening&#x3f; An Assessment of Automated Cybercrime &#x5b;Guest Diary&#x5d;, (Wed, Jun 24th)'
date: 2026-06-25
permalink: /posts/2026/06/25/what-do-ports-hear-when-nobodys-listeningx3f-an-assessment-of-automated-cybercrime-x5bguest-diaryx5d-wed-jun-24th/
tags:
- veille-cyber
- sans-isc
---
### Anatomie du bruit de fond : Analyse des botnets automatisés

L’analyse des journaux d’un *honeypot* révèle que le trafic malveillant « de masse » n’est pas un simple bruit statique, mais un écosystème complexe et multi-niveaux. Les attaquants exploitent massivement des vulnérabilités connues, souvent avec des scripts peu soignés, tout en utilisant des infrastructures de rebond disparates (cloud public, appareils domestiques compromis).

#### Points clés
*   **Stratégie opportuniste :** Les botnets (Terrabot, r00ts3c, RondoDox) scannent en continu l’Internet pour trouver des appareils non corrigés, priorisant le volume à la sophistication.
*   **Erreurs de script :** De nombreuses attaques échouent à cause d'erreurs de syntaxe grossières (ex: espaces non encodés, mauvais en-têtes HTTP), témoignant d’une automatisation rapide et mal testée.
*   **Adaptabilité :** Les botnets comme RondoDox font preuve d'une maturité tactique supérieure en utilisant des charges utiles "fileless" (sans fichier) et en modifiant dynamiquement leurs serveurs de commande (C2) pour éviter la détection.
*   **Le cycle de vie du botnet :** Un appareil domestique compromis devient lui-même un scanner, créant une boucle de propagation automatique dont le propriétaire est souvent inconscient.

#### Vulnérabilités exploitées
Les attaquants ciblent principalement des failles anciennes mais toujours présentes sur des équipements IoT/Routeurs :
*   **CVE-2016-20016 :** Backdoor RCE dans les DVR MVPower (JAWS Webserver).
*   **CVE-2016-20017 :** Injection de commande dans les routeurs D-Link DSL.
*   **CVE-2018-10561 :** Contournement d'authentification dans les routeurs Dasan GPON.
*   **CVE-2018-6000 :** Manipulation NVRAM sur ASUS AsusWRT.
*   **CVE-2021-44228 (Log4Shell) :** Utilisation de l'injection dans les en-têtes HTTP.
*   **CVE-2023-26801 :** Injection de commande sur routeurs LB-LINK.
*   **CVE-2023-48022 (ShadowRay) :** Exécution à distance sur frameworks Ray.
*   **CVE-2025-34037 :** Injection de commande persistante sur routeurs Linksys E-series.

#### Recommandations
*   **Mise à jour proactive :** Le maintien à jour du micrologiciel (*firmware*) des routeurs et appareils IoT est la première ligne de défense, ces équipements étant les cibles privilégiées des botnets.
*   **Segmenter et isoler :** Placer les appareils IoT sur un réseau isolé (VLAN) pour limiter la propagation en cas de compromission.
*   **Analyse de logs :** Ne pas ignorer les tentatives répétitives dans les journaux de bord. La détection d'anomalies (ex: requêtes HTTP avec des en-têtes suspects ou des payloads encodés) permet d'identifier des scans ciblés avant qu'ils ne réussissent.
*   **Durcissement (Hardening) :** Désactiver les services de gestion à distance (Telnet, interface web d'administration) sur les ports WAN, et supprimer les fonctionnalités de diagnostic (ping, diagnostic tools) si elles ne sont pas nécessaires.

---
[Source](https://isc.sans.edu/diary/rss/33104){:target="_blank"}
