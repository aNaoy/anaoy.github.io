---
title: 'Block the Prompt, Not the Work: The End of "Doctor No"'
date: 2026-04-01
permalink: /posts/2026/04/01/block-the-prompt-not-the-work-the-end-of-doctor-no/
tags:
- veille-cyber
- hackernews
---
### La fin de la « sécurité théâtrale » : protéger le flux plutôt que l'accès

La stratégie de cybersécurité traditionnelle, fondée sur le blocage systématique des outils (IA, partage de fichiers) et l'usage d'agents lourds sur les terminaux (« Doctor No »), est devenue obsolète et contre-productive. En entravant l'efficacité des utilisateurs, ces mesures poussent ces derniers vers des solutions non maîtrisées (le « shadow IT »), créant des risques invisibles pour l'entreprise.

**Points clés :**
*   **L'inefficacité des méthodes héritées :** Les agents EDR invasifs et le déchiffrement SSL imposé par les passerelles web (SWG/SASE) nuisent aux performances et brisent souvent les applications modernes.
*   **L'angle mort du navigateur :** Le navigateur est devenu le système d'exploitation principal, mais la majorité des outils de sécurité restent aveugles à ce qui s'y déroule réellement, notamment via les extensions de navigateur malveillantes.
*   **Le paradoxe du blocage :** Bloquer un domaine (ex: DeepSeek) ne protège pas contre les risques si les utilisateurs utilisent des extensions tierces (« wrappers ») qui contournent les contrôles réseau pour exfiltrer des données.

**Vulnérabilités associées :**
*   **Exfiltration via extensions de navigateur :** Les extensions peuvent capturer des données ou des identifiants en amont de toute inspection réseau.
*   **Contournement de politiques (Shadow IT) :** L'usage de comptes personnels ou d'outils non autorisés pour compenser les blocages IT crée des trous de sécurité.
*   *Note : Aucune CVE spécifique n'est mentionnée, car le problème relève d'une faille architecturale systémique plutôt que d'une vulnérabilité logicielle isolée.*

**Recommandations :**
*   **Passer à une gouvernance au niveau de la session :** Déplacer la sécurité du terminal vers le navigateur pour une visibilité accrue, indépendamment du type d'appareil (BYOD, prestataires).
*   **Implémenter le DLP au niveau du prompt :** Analyser et filtrer les données sensibles (PII, code source) en temps réel, directement dans le tampon du navigateur avant l'envoi de la requête.
*   **Gérer la couche des extensions :** Évaluer et noter le risque des extensions de navigateur, souvent vecteurs d'exfiltration silencieuse.
*   **Adopter une approche "agentless" :** Privilégier des outils de contrôle qui ne nécessitent pas de modifications au niveau du noyau (kernel) du système, évitant ainsi l'impact sur la productivité des utilisateurs.

---
[Source](https://thehackernews.com/2026/04/block-prompt-not-work-end-of-doctor-no.html){:target="_blank"}
