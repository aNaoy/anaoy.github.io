---
title: 'New VMScape attack breaks guest-host isolation on AMD, Intel CPUs'
date: 2025-09-11
permalink: /posts/2025/09/11/new-vmscape-attack-breaks-guest-host-isolation-on-amd-intel-cpus/
tags:
- veille-cyber
- bleepingcomp
---
**VMScape : Une nouvelle attaque contre l'isolation des machines virtuelles**

Une vulnérabilité découverte récemment, baptisée VMScape, permet à une machine virtuelle (VM) compromise de lire des informations sensibles, telles que des clés cryptographiques, à partir du processus d'hyperviseur QEMU fonctionnant sur des processeurs AMD et Intel. Cette attaque exploite une faille dans la façon dont les processeurs modernes gèrent l'exécution spéculative, contournant les protections existantes.

Les chercheurs de l'ETH Zurich ont démontré que VMScape peut être déployée sans compromettre directement l'hôte, en exploitant le partage de structures de prédiction de branchement (BPU) entre la VM invitée et l'hyperviseur hôte. L'attaque cible QEMU et utilise une technique de canal auxiliaire de cache (cache side-channel) pour extraire des données. Elle parvient également à déjouer l'ASLR (Address Space Layout Randomization) afin de localiser les informations ciblées.

Les données sont extraites à une vitesse d'environ 32 octets par seconde avec une précision élevée, ce qui permettrait de voler une clé de chiffrement de disque de 4 Ko en quelques minutes.

**Points clés :**

*   **Nature de l'attaque :** VMScape est une attaque de type "Spectre-like" qui exploite l'exécution spéculative.
*   **Cible :** Processus d'hyperviseur QEMU.
*   **Impact :** Fuite de données sensibles (clés cryptographiques, etc.) de l'hyperviseur ou d'autres VMs depuis une VM invitée compromise.
*   **Conditions :** Fonctionne sur des processeurs AMD (Zen 1 à Zen 5) et Intel ("Coffee Lake"). Ne nécessite pas la compromission de l'hôte et contourne les mitigations matérielles par défaut.
*   **Déploiement potentiel :** Un attaquant pourrait louer une VM dans un environnement cloud pour cibler l'hyperviseur ou d'autres clients.

**Vulnérabilités :**

*   **CVE-2025-40300 :** L'identifiant attribué à cette vulnérabilité.
*   **Exploitation :** Utilisation de la prédiction indirecte de branchement (via le BPU) et de canaux auxiliaires de cache pour l'extraction de données. Contournement de l'ASLR.

**Recommandations :**

*   **Mitigation par le noyau Linux :** Des correctifs ont été publiés pour le noyau Linux, ajoutant une barrière de prédiction de branchement indirect (IBPB) lors du passage de l'invité à l'hôte (VMEXIT). Cette mesure a un impact minimal sur les performances.
*   **AMD et Intel :** Les fabricants de processeurs ont été informés et des bulletins de sécurité ont été émis (AMD a publié un bulletin).

Bien que complexe à mettre en œuvre, VMScape représente une menace sérieuse pour la sécurité des environnements virtualisés et du cloud computing, soulignant la nécessité de mises à jour logicielles régulières et de vigilance constante.

---
[Source](https://www.bleepingcomputer.com/news/security/new-vmscape-attack-breaks-guest-host-isolation-on-amd-intel-cpus/){:target="_blank"}
