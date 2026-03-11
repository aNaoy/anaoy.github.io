---
title: 'New PhantomRaven NPM attack wave steals dev data via 88 packages'
date: 2026-03-11
permalink: /posts/2026/03/11/new-phantomraven-npm-attack-wave-steals-dev-data-via-88-packages/
tags:
- veille-cyber
- bleepingcomp
---
### Campagne PhantomRaven : Recrudescence d'attaques par paquets NPM malveillants

La campagne « PhantomRaven » persiste et s'intensifie, ciblant les développeurs JavaScript via la publication massive de paquets malveillants sur le registre NPM. Depuis août 2025, plus de 200 paquets frauduleux ont été identifiés. Les attaquants utilisent le *typosquatting* (imitation de noms de bibliothèques populaires comme Babel ou GraphQL) pour tromper les utilisateurs, souvent en générant des noms de paquets via l'IA.

**Points clés :**
*   **Technique d'évasion :** Utilisation de dépendances dynamiques distantes (RDD). Le fichier `package.json` pointe vers une URL externe, permettant de télécharger le code malveillant à l'exécution et de contourner l'analyse automatisée des outils de sécurité.
*   **Objectifs :** Exfiltration de données sensibles incluant les fichiers `.gitconfig`, `.npmrc`, les variables d'environnement, ainsi que les jetons d'accès CI/CD (GitHub, GitLab, Jenkins, CircleCI).
*   **Infrastructures :** Les attaquants utilisent des domaines hébergés sur AWS EC2, sans certificat TLS, et conservent une structure de code quasi identique d'une vague à l'autre.
*   **Vulnérabilités :** Aucune CVE spécifique n'est associée, car il s'agit d'une attaque par ingénierie sociale exploitant le mécanisme natif de gestion des dépendances de NPM pour exécuter du code arbitraire.

**Recommandations :**
*   **Vérification rigoureuse :** Valider systématiquement la légitimité des paquets et la réputation des éditeurs avant toute installation.
*   **Méfiance vis-à-vis de l'IA :** Ne pas copier-coller aveuglément les suggestions de noms de bibliothèques provenant de chatbots ou de sources non vérifiées.
*   **Audit des dépendances :** Surveiller les fichiers `package.json` pour détecter des références suspectes vers des URLs externes inhabituelles.
*   **Gestion des secrets :** Éviter de stocker des jetons d'accès ou des identifiants dans des fichiers de configuration locale.

---
[Source](https://www.bleepingcomputer.com/news/security/new-phantomraven-npm-attack-wave-steals-dev-data-via-88-packages/){:target="_blank"}
