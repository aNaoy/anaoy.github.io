---
title: 'ClickFix has never been bigger, and AI tools are its most convincing lure yet'
date: 2026-10-21
permalink: /posts/2026/10/21/clickfix-has-never-been-bigger-and-ai-tools-are-its-most-convincing-lure-yet/
tags:
- veille-cyber
- bleepingcomp
---
### L'essor des attaques « ClickFix » via les outils d'IA

La technique « ClickFix » est devenue en 2026 une menace majeure, représentant jusqu'à 67 % des détections de certaines plateformes de sécurité. Ce vecteur d'attaque, qui incite les utilisateurs à copier-coller des commandes malveillantes dans leur terminal, exploite désormais la popularité croissante des outils d'intelligence artificielle.

**Points clés :**
*   **Vecteur principal :** 80 % des attaques proviennent des moteurs de recherche (publicités malveillantes, SEO poisoning) et non d'e-mails, contournant ainsi les passerelles de sécurité classiques.
*   **Adaptation à l'IA :** Les attaquants usurpent des outils comme Claude ou ChatGPT. Ils utilisent des pages de téléchargement factices affichant des commandes légitimes, mais copiant un script malveillant dans le presse-papier de l'utilisateur.
*   **Méthode "LLMshare" :** Les pirates exploitent les fonctionnalités de partage de conversations ou de "GPT personnalisés" sur les plateformes d'IA pour diffuser des liens vers des pages de phishing, bénéficiant de la réputation de confiance de ces sites.
*   **Efficacité :** Ces attaques réussissent à convertir près de 96,3 % des intrusions en exécution de malware, car les commandes s'exécutent en mémoire (sans écriture sur disque) via un shell légitime, échappant aux solutions EDR.

**Vulnérabilités exploitées :**
*   **Comportement utilisateur :** La normalisation de l'installation d'outils via le terminal et la recherche systématique de logiciels sur les moteurs de recherche plutôt que via des accès directs.
*   **Contournement de la réputation :** Utilisation de domaines légitimes (sites compromis, Google Sites, plateformes d'IA) et stockage de configurations sur des contrats intelligents blockchain (EtherHiding) pour éviter tout blocage.
*   **Absence de protection spécifique :** Vulnérabilité accrue sur les postes de travail non protégés par EDR (BYOD, prestataires).
*   *Note : Aucune CVE spécifique n'est associée, car il s'agit d'une technique d'ingénierie sociale exploitant des fonctionnalités légitimes (abus de processus).*

**Recommandations :**
*   **Sensibilisation :** Éduquer les utilisateurs sur les risques liés au copier-coller de commandes depuis des pages web, même si elles semblent provenir de sources officielles.
*   **Accès direct :** Encourager l'utilisation de favoris ou d'adresses URL saisies manuellement pour accéder aux outils professionnels au lieu de passer par des moteurs de recherche.
*   **Sécurité du navigateur :** Déployer des solutions offrant une visibilité sur les attaques basées sur le navigateur pour intercepter ces menaces avant que la commande ne soit exécutée sur le terminal.
*   **Renforcement EDR :** Configurer les outils de sécurité pour surveiller et restreindre l'exécution de scripts suspicieux, même lorsqu'ils sont lancés via des interpréteurs de commandes standards.

---
[Source](https://www.bleepingcomputer.com/news/security/clickfix-has-never-been-bigger-and-ai-tools-are-its-most-convincing-lure-yet/){:target="_blank"}
