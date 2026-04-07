---
title: 'Over 1,000 Exposed ComfyUI Instances Targeted in Cryptomining Botnet Campaign'
date: 2026-04-07
permalink: /posts/2026/04/07/over-1000-exposed-comfyui-instances-targeted-in-cryptomining-botnet-campaign/
tags:
- veille-cyber
- hackernews
---
### Campagne de botnet ciblant les instances ComfyUI exposées

Des attaquants exploitent actuellement plus de 1 000 instances de **ComfyUI** (plateforme de génération d'images Stable Diffusion) exposées sur Internet. La campagne vise à intégrer ces serveurs dans un botnet dédié au minage de cryptomonnaies (Monero et Conflux) et à la vente de bande passante via des nœuds proxy (Hysteria V2).

#### Points clés
*   **Mode opératoire :** Les attaquants utilisent un scanner Python pour identifier les instances ComfyUI accessibles publiquement.
*   **Vecteur d'attaque :** Exploitation de nœuds personnalisés (*custom nodes*) mal configurés qui acceptent et exécutent du code Python arbitraire sans authentification préalable.
*   **Persistance :** Mise en place de mécanismes sophistiqués incluant des scripts téléchargeant des charges utiles toutes les six heures, l'utilisation de `LD_PRELOAD` pour masquer les processus de minage, et la commande `chattr +i` pour rendre les binaires immuables et impossibles à supprimer par le root.
*   **Élimination de la concurrence :** Le script d'attaque identifie et neutralise les botnets concurrents (comme « Hisana ») en détournant leurs configurations et en occupant leurs ports de contrôle.

#### Vulnérabilités
Il n'existe pas de CVE unique car l'attaque repose sur une **mauvaise configuration de sécurité** inhérente à l'architecture de certains nœuds personnalisés dans ComfyUI. L'exploitation tire profit de la capacité de ces nœuds à exécuter des entrées non filtrées. Les familles de nœuds ciblées incluent :
*   `Vova75Rus/ComfyUI-Shell-Executor`
*   `filliptm/ComfyUI_Fill-Nodes`
*   `seanlynch/srl-nodes`
*   `ruiqutech/ComfyUI-RuiquNodes`

#### Recommandations
*   **Accès restreint :** Ne jamais exposer les instances ComfyUI directement sur Internet. Utilisez un VPN ou un tunnel SSH pour accéder à l'interface de gestion.
*   **Authentification :** Activez des couches d'authentification supplémentaires pour restreindre l'accès à l'interface utilisateur.
*   **Audit des nœuds :** Passez en revue les nœuds personnalisés installés via *ComfyUI-Manager* et supprimez ceux qui ne sont pas nécessaires ou dont la source n'est pas fiable.
*   **Surveillance système :** Surveillez l'utilisation anormale des ressources CPU/GPU et inspectez régulièrement les processus suspects ou les fichiers immuables dans les répertoires système.

---
[Source](https://thehackernews.com/2026/04/over-1000-exposed-comfyui-instances.html){:target="_blank"}
