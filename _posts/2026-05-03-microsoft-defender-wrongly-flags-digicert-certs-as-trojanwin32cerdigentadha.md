---
title: 'Microsoft Defender wrongly flags DigiCert certs as Trojan:Win32/Cerdigent.A!dha'
date: 2026-05-03
permalink: /posts/2026/05/03/microsoft-defender-wrongly-flags-digicert-certs-as-trojanwin32cerdigentadha/
tags:
- veille-cyber
- bleepingcomp
---
### Faux positifs de Microsoft Defender sur les certificats DigiCert

Une mise à jour des signatures de Microsoft Defender (30 avril) a provoqué une vague de faux positifs mondiaux en identifiant à tort des certificats racines légitimes de DigiCert comme étant le cheval de Troie `Trojan:Win32/Cerdigent.A!dha`. Cette détection erronée a conduit le système à supprimer automatiquement certains certificats du magasin de confiance Windows.

**Points clés :**
* **Nature du problème :** Classification erronée de certificats racines légitimes en logiciels malveillants.
* **Impact :** Suppression automatique de certificats vitaux dans la base de registre (`HKLM\SOFTWARE\Microsoft\SystemCertificates\AuthRoot\Certificates\`), perturbant potentiellement la validation des connexions sécurisées.
* **Contexte potentiel :** Cet incident survient dans un climat de méfiance suite à une récente compromission chez DigiCert, où des attaquants ont réussi à obtenir des certificats de signature de code valides pour signer le malware "Zhong Stealer". Microsoft n'a toutefois pas confirmé de lien officiel entre ces événements.

**Vulnérabilités :**
* Aucun CVE associé : il s'agit d'une erreur de détection logicielle par l'antivirus (faux positif) et non d'une faille de sécurité exploitée sur le système de l'utilisateur.

**Recommandations :**
* **Mise à jour :** Microsoft a déployé un correctif dans la version **1.449.430.0** (et supérieures) de ses définitions de sécurité. Les utilisateurs doivent forcer la mise à jour via : *Sécurité Windows > Protection contre les virus et menaces > Mises à jour de protection > Rechercher les mises à jour*.
* **Restauration :** Le correctif devrait restaurer automatiquement les certificats supprimés. En cas de persistance, une vérification manuelle du magasin de certificats peut être nécessaire.

---
[Source](https://www.bleepingcomputer.com/news/security/microsoft-defender-wrongly-flags-digicert-certs-as-trojan-win32-cerdigentadha/){:target="_blank"}
