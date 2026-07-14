---
title: 'Grok Build Uploaded Entire Git Repositories to xAI Storage, Not Just Files It Read'
date: 2026-07-14
permalink: /posts/2026/07/14/grok-build-uploaded-entire-git-repositories-to-xai-storage-not-just-files-it-read/
tags:
- veille-cyber
- hackernews
---
### Fuite de données massive dans Grok Build

L'outil en ligne de commande « Grok Build » de xAI a été identifié comme extrayant l'intégralité des dépôts Git des utilisateurs — incluant l'historique complet des commits — vers un bucket Google Cloud Storage, dépassant largement les besoins fonctionnels de l'agent.

**Points clés**
*   **Exfiltration systématique :** Contrairement aux attentes, l'outil envoyait des gigaoctets de données (fichiers non lus, secrets, historique Git) via un canal de stockage distinct, même lorsque l'option « Améliorer le modèle » était désactivée.
*   **Absence de cloisonnement :** Les fichiers contenant des identifiants (comme les fichiers `.env`) étaient téléversés sans aucune expurgation, exposant ainsi des secrets même après leur suppression dans le répertoire de travail.
*   **Contrôle trompeur :** L'option de confidentialité proposée aux utilisateurs ne concernait que l'entraînement du modèle et non le transfert des données vers les serveurs de stockage.
*   **Persistance du code :** Le code responsable de l'upload est toujours présent dans le binaire ; son activation est pilotée par un réglage côté serveur, permettant à xAI de réactiver la collecte à distance à tout moment.

**Vulnérabilités**
Aucune CVE n'est associée à cet incident, car il s'agit d'une faille de conception intentionnelle (exfiltration de données par défaut) et non d'une vulnérabilité logicielle classique. La sécurité est compromise par le non-respect de la confidentialité des données sources (secrets dans l'historique Git).

**Recommandations**
*   **Rotation immédiate des secrets :** Considérer comme compromis tout mot de passe, clé API ou jeton d'accès présent dans un dépôt ayant été analysé par Grok Build, y compris ceux ayant été supprimés dans l'historique des commits.
*   **Utilisation de commandes de purge :** Pour les utilisateurs individuels, exécuter la commande `/privacy` dans l'interface CLI pour tenter de désactiver la rétention et demander la suppression des données déjà synchronisées.
*   **Vigilance réseau :** Surveiller les flux sortants des outils de développement basés sur le cloud pour vérifier le volume de données réellement transmises.
*   **Prudence :** Ne pas considérer les outils d'IA comme « locaux » ; par défaut, ces outils peuvent transmettre tout ou partie de votre environnement de travail à des serveurs distants.

---
[Source](https://thehackernews.com/2026/07/grok-build-uploads-entire-git.html){:target="_blank"}
