---
title: 'Application Control Bypass for Data Exfiltration, (Tue, Mar 31st)'
date: 2026-03-31
permalink: /posts/2026/03/31/application-control-bypass-for-data-exfiltration-tue-mar-31st/
tags:
- veille-cyber
- sans-isc
---
### Contournement des pare-feu de nouvelle génération pour l'exfiltration de données

Les pare-feu dits de "nouvelle génération" (NGFW) utilisent des mécanismes de classification du trafic (comme App-ID chez Palo Alto) pour identifier et bloquer les applications en temps réel. Cependant, ces systèmes nécessitent généralement l'analyse des premiers kilo-octets (généralement 5 à 10 Ko) d'une session pour établir une signature fiable. Ce délai de classification crée une fenêtre d'opportunité permettant d'exfiltrer des données par petits segments.

**Points clés :**
* **Vulnérabilité de classification :** Le pare-feu autorise le début du flux avant d'avoir pu identifier l'application, ce qui permet l'envoi de petits paquets de données sous le seuil de détection.
* **Technique de contournement :** En segmentant un fichier en petits morceaux (ex: 3 Ko) et en les envoyant via une série de connexions TCP distinctes, il est possible de transférer des volumes de données importants sans jamais dépasser le seuil de classification qui déclencherait le blocage.
* **Discrétion :** Cette méthode évite les pics de bande passante suspects, rendant l'exfiltration difficile à repérer par des outils d'analyse de trafic traditionnels.

**Vulnérabilités :**
* Il n'existe pas de CVE spécifique, car il s'agit d'une limite inhérente au fonctionnement des moteurs d'inspection profonde de paquets (DPI) qui privilégient la performance en autorisant le trafic avant une identification complète.

**Recommandations :**
* **Surveillance du comportement réseau :** Détecter les anomalies basées sur le volume de connexions répétitives vers une même destination externe, qui ressemblent à du "malware beaconing".
* **Inspection SSL/TLS :** Utiliser le déchiffrement SSL pour permettre aux pare-feu d'inspecter le contenu réel des flux, même si l'application semble "inconnue".
* **Politiques de "Zero Trust" :** Appliquer des règles de sortie strictes par défaut ("deny all"), n'autorisant que les flux nécessaires et identifiés, plutôt que de se reposer uniquement sur la classification automatique des applications.
* **Analyse IDS/IPS :** Renforcer la détection des modèles de communication suspects (micro-connexions) via des solutions EDR ou SIEM.

---
[Source](https://isc.sans.edu/diary/rss/32850){:target="_blank"}
