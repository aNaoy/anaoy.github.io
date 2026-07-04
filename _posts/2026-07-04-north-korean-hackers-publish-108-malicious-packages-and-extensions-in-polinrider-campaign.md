---
title: 'North Korean Hackers Publish 108 Malicious Packages and Extensions in PolinRider Campaign'
date: 2026-07-04
permalink: /posts/2026/07/04/north-korean-hackers-publish-108-malicious-packages-and-extensions-in-polinrider-campaign/
tags:
- veille-cyber
- hackernews
---
### Campagne PolinRider : La menace persistante de la chaîne d'approvisionnement logicielle

La campagne « PolinRider », orchestrée par des acteurs liés au groupe nord-coréen *Contagious Interview*, cible les développeurs et le secteur des cryptomonnaies via l'empoisonnement de bibliothèques open source. Les attaquants compromettent des comptes de mainteneurs légitimes pour publier des versions malveillantes de paquets (npm, Composer, Go) et d'extensions, incitant les victimes à exécuter du code arbitraire.

**Points clés :**
*   **Vecteurs d'attaque :** Utilisation de fichiers de tâches VS Code (`.vscode/tasks.json`) configurés pour une exécution automatique lors de l'ouverture d'un dossier, ainsi que l'injection de scripts JavaScript obfusqués dans des fichiers de configuration (ex: `tailwind.config.js`, `postcss.config.mjs`).
*   **Techniques de dissimulation :** Réécriture de l'historique Git et utilisation de "force pushes" pour antidater les commits malveillants, rendant l'activité difficile à détecter sur les interfaces GitHub.
*   **Charge utile :** Le malware télécharge des menaces avancées comme *DEV#POPPER RAT* et *OmniStealer* en communiquant avec des infrastructures blockchain (TRON, Aptos, BNB).
*   **Étendue :** Plus de 100 paquets malveillants et près de 2 000 dépôts GitHub compromis à ce jour.

**Vulnérabilités :**
Aucun CVE spécifique n'est mentionné, car l'attaque repose sur l'abus de fonctionnalités légitimes (tâches d'automatisation des IDE, mécanismes de publication de dépôts) et l'usurpation de comptes de confiance.

**Recommandations :**
*   **Audit des postes de travail :** Inspecter systématiquement les fichiers `.vscode/tasks.json` et les scripts de configuration (`config.js`, `vite.config.js`, `eslint.config.js`) pour détecter des modifications suspectes.
*   **Réponse aux incidents :** Si un paquet suspect a été installé, considérez l'environnement comme compromis. Il est impératif de réinitialiser tous les secrets exposés (clés API, identifiants) depuis une machine saine.
*   **Hygiène de développement :** Ne pas se fier aveuglément à l'historique de commit GitHub. Vérifiez les logs d'activité des dépôts et reconstruisez les projets à partir de fichiers de verrouillage (*lockfiles*) connus comme étant sains.

---
[Source](https://thehackernews.com/2026/07/north-korean-hackers-publish-108.html){:target="_blank"}
