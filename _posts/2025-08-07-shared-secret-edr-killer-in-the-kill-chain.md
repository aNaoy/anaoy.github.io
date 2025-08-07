---
title: 'Shared secret: EDR killer in the kill chain'
date: 2025-08-07
permalink: /posts/2025/08/07/shared-secret-edr-killer-in-the-kill-chain/
tags:
- veille-cyber
- sophos
---
## Affaiblissement des défenses : une arme sophistiquée contre les solutions de sécurité

Une menace croissante dans les cyberattaques multi-étapes consiste à neutraliser les solutions de sécurité Endpoint Detection and Response (EDR). Des outils de plus en plus sophistiqués, parfois développés par des groupes de ransomware ou acquis sur le marché noir, visent spécifiquement à désactiver ces défenses, permettant aux acteurs malveillants d'opérer sans être détectés. L'utilisation de packers comme HeartCrypt obscurcit ces outils.

L'article détaille une campagne utilisant un outil, baptisé "AVKiller", qui s'insère dans des logiciels légitimes comme Beyond Compare. Une fois exécuté, il tente de désactiver les logiciels de sécurité en chargeant un pilote système malveillant.

### Points Clés

*   **Technique d'évasion :** L'outil cherche un pilote avec un nom aléatoire et utilise des certificats signés, souvent compromis ou expirés, pour masquer ses activités.
*   **Ciblage varié :** Les versions de cet outil ciblent une liste étendue de produits de sécurité, tels que Sophos, Microsoft Defender, SentinelOne, Kaspersky, McAfee, Bitdefender, et bien d'autres.
*   **Diffusion inter-groupes :** Des preuves suggèrent un partage d'outils et de connaissances techniques entre différents groupes de ransomware, comme RansomHub, Qilin, DragonForce et INC, qui utilisent des versions modifiées de cet outil, souvent obscurcies par le packer HeartCrypt.
*   **Cas d'usage :** L'outil est fréquemment observé en conjonction avec des attaques de ransomware, servant à éliminer les défenses avant le chiffrement des données.

### Vulnérabilités

*   **Certificats compromis/expirés :** L'utilisation de certificats signés par des entités comme "Changsha Hengxiang Information Technology Co., Ltd." et "Fuzhou Dingxin Trade Co., Ltd.", dont certains sont révoqués depuis longtemps (ex: 2016, 2012), permet de contourner les protections basées sur la signature. Aucune CVE spécifique n'est mentionnée pour l'outil lui-même, mais l'exploitation de certificats invalides est une technique d'évasion.

### Recommandations

*   **Surveillance des certificats :** Les équipes de sécurité doivent être vigilantes quant aux certificats utilisés pour signer les pilotes système, en particulier ceux émis par des entités chinoises ou de Hong Kong qui ont été précédemment associés à des activités malveillantes.
*   **Détection comportementale :** Les mécanismes de défense dynamiques (SysCall, DynamicShellcode, HollowProcess) et les détections statiques génériques (Mal/HCrypt-, Troj/HCrypt-, Mal/Isher-Gen) sont importants pour identifier et bloquer ces outils.
*   **Partage d'informations :** Le partage d'informations sur les tactiques, techniques et procédures (TTP) entre les équipes de défense est crucial pour comprendre et contrer les menaces évolutives, notamment la coopération entre groupes de ransomware.
*   **Mises à jour et correctifs :** S'assurer que toutes les solutions de sécurité sont à jour et que les logiciels d'entreprise sont patchés pour éviter l'exploitation de vulnérabilités (comme potentiellement avec SimpleHelp mentionné dans le cas de MedusaLocker).

---
[Source](https://news.sophos.com/en-us/2025/08/06/shared-secret-edr-killer-in-the-kill-chain/){:target="_blank"}
