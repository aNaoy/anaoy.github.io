---
title: 'Microsoft to stop Exchange 2016 / 2019 security updates in October'
date: 2026-07-22
permalink: /posts/2026/07/22/microsoft-to-stop-exchange-2016-2019-security-updates-in-october/
tags:
- veille-cyber
- bleepingcomp
---
### Fin du support étendu pour Microsoft Exchange 2016 et 2019

Microsoft a confirmé l'arrêt définitif du programme de mises à jour de sécurité étendues (ESU) pour Exchange Server 2016 et 2019 en octobre 2026. Contrairement aux extensions précédentes, aucune prolongation supplémentaire ne sera accordée. Passé cette date, les serveurs concernés ne recevront plus aucun correctif, exposant les infrastructures à des risques critiques de sécurité.

**Points clés :**
* **Échéance finale :** Octobre 2026 marque la fin totale du support, incluant le programme ESU "Période 2".
* **Absence d'extension :** Microsoft a été explicite sur le fait qu'aucune dérogation ou report ne sera mis en place.
* **Risque métier :** Les serveurs non mis à jour resteront vulnérables aux futures failles exploitables, sans possibilité de remédiation officielle.

**Vulnérabilités :**
* Aucune CVE spécifique n'est mentionnée dans l'article, mais le maintien de systèmes en fin de vie (End-of-Life) rend les serveurs Exchange intrinsèquement vulnérables aux futures attaques par exécution de code à distance (RCE) et autres vecteurs d'attaque courants sur cette plateforme.

**Recommandations :**
* **Migration vers Exchange Server Subscription Edition (SE) :** Microsoft recommande une mise à niveau directe (in-place upgrade) depuis Exchange 2019 vers la version SE, qui bénéficie d'un support actif.
* **Migration vers le Cloud :** Pour les organisations souhaitant sortir de la gestion d'infrastructures sur site, une transition vers Exchange Online ou Microsoft 365 est préconisée.
* **Planification immédiate :** Les administrateurs doivent initier dès maintenant les projets de migration pour garantir la continuité de la sécurisation avant l'échéance d'octobre 2026.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-exchange-2016-and-2019-esu-program-ends-in-october/){:target="_blank"}
