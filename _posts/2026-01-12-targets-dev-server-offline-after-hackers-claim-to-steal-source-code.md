---
title: 'Targets dev server offline after hackers claim to steal source code'
date: 2026-01-12
permalink: /posts/2026/01/12/targets-dev-server-offline-after-hackers-claim-to-steal-source-code/
tags:
- veille-cyber
- bleepingcomp
---
**Vente de code source interne de Target : serveur Git hors ligne après des allégations de vol**

Des pirates informatiques affirment avoir volé et proposent à la vente des parties importantes du code source interne de Target, ainsi que des documents de développement. Ils ont publié des échantillons sur la plateforme Gitea, révélant des noms de dépôts tels que "wallet-services-wallet-pentest-collections", "TargetIDM-TAPProvisioingAPI" et "Secrets-docs". Ces dépôts contenaient des listes détaillées de tens de milliers de fichiers, représentant un volume total d'environ 860 Go de données prétendument dérobées. Les métadonnées des commits et la documentation mentionnent des serveurs de développement internes et des noms d'ingénieurs de Target.

Suite à la notification de ces allégations, les dépôts Gitea ont été retirés et le serveur Git de Target, `git.target.com`, est devenu inaccessible depuis Internet. Auparavant, il redirigeait vers une page de connexion nécessitant un VPN ou un accès sécurisé. L'indexation par des moteurs de recherche de quelques ressources du sous-domaine `git.target.com` suggère que certains contenus auraient pu être accessibles publiquement par le passé, bien que la configuration exacte et la période restent incertaines.

Les structures de répertoires, la dénomination des dépôts et les références aux systèmes internes observées dans les échantillons correspondent à un environnement Git d'entreprise, et ne semblent pas correspondre aux projets open-source de Target.

**Points clés :**

*   Allégations de vol et de mise en vente de code source interne de Target.
*   Publication d'échantillons sur Gitea par des acteurs malveillants.
*   Le serveur Git de Target (`git.target.com`) a été rendu inaccessible.
*   Les échantillons semblent cohérents avec une infrastructure de développement d'entreprise privée.

**Vulnérabilités :**

*   Aucune vulnérabilité spécifique avec un identifiant CVE n'est mentionnée dans l'article. L'accès au code source suggère une compromission des systèmes internes de Target.

**Recommandations :**

*   Les dépôts hébergés sur Gitea ont été retirés.
*   Le serveur Git de Target a été mis hors ligne.
*   Il est conseillé aux employés de Target de vérifier la sécurité de leurs accès et des systèmes de développement.

---
[Source](https://www.bleepingcomputer.com/news/security/targets-dev-server-offline-after-hackers-claim-to-steal-source-code/){:target="_blank"}
