---
title: 'Google Cloud Warns Three AMD Turin CPU Flaws Could Leak Data Across Processes in VMs'
date: 2026-11-12
permalink: /posts/2026/11/12/google-cloud-warns-three-amd-turin-cpu-flaws-could-leak-data-across-processes-in-vms/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilités des processeurs AMD Turin : Risques et mesures correctives

Google Cloud a émis une alerte concernant trois failles de type "Transient Scheduler Attack" (TSA) affectant les processeurs AMD EPYC de cinquième génération (nom de code Turin). Ces vulnérabilités par canaux auxiliaires permettent à un attaquant, disposant de privilèges locaux, d'extraire des données sensibles d'autres processus ou du noyau au sein d'une même machine virtuelle.

**Points clés :**
* **Impact :** Les failles permettent des fuites de données entre processus sur un même cœur de processeur.
* **Gravité :** Évaluée comme "Moyenne" par Google. Bien que complexes, ces attaques ne nécessitent que des privilèges bas.
* **Statut :** Aucune exploitation active n'a été signalée à ce jour.
* **Portée :** Concerne les séries de machines Google Cloud C4D, N4D, H4D, Z4D et G4.

**Vulnérabilités identifiées :**
* **CVE-2024-36350 (TSA-SQ) :** Faille liée à la gestion du planificateur.
* **CVE-2024-36357 (TSA-L1) :** Faille liée au cache L1.
* **CVE-2026-0004 (TSA-Fill) :** Nouvelle variante spécifique aux processeurs Zen 5, permettant l'inférence de données dans le cache L1.

**Recommandations :**
* **Mises à jour système :** Installer les correctifs fournis par l'éditeur de votre système d'exploitation dès leur disponibilité.
* **Action obligatoire :** Un simple redémarrage du système d'exploitation invité est insuffisant. Une fois le correctif appliqué, les instances doivent être **arrêtées puis démarrées** pour que les mises à jour des informations CPU soient prises en compte et que les atténuations soient activées.
* **Infrastructure sur site :** Pour les serveurs physiques utilisant des processeurs Turin, il est impératif de mettre à jour le firmware (BIOS/UEFI) ainsi que le noyau du système d'exploitation.
* **Performance :** L'application des correctifs peut entraîner une baisse de performance ; il est conseillé d'évaluer l'impact sur vos charges de travail critiques.

---
[Source](https://thehackernews.com/2026/11/google-cloud-warns-three-amd-turin-cpu.html){:target="_blank"}
