---
title: 'How And Why We Hacked Cypherock Hardware Wallet: The Full Story'
date: 2025-11-21
permalink: /posts/2025/11/21/how-and-why-we-hacked-cypherock-hardware-wallet-the-full-story/
tags:
- veille-cyber
- zerodaysfans
---
## Attaque sur le Cypherock X1 Vault

Une analyse approfondie a révélé plusieurs vulnérabilités dans le Cypherock X1 Vault, remettant en question ses prétentions à la sécurité. Ces failles permettent à un attaquant, potentiellement via une attaque de la chaîne d'approvisionnement, de prendre le contrôle total du dispositif, de contourner les protections fondamentales et d'accéder aux phrases mnémotechniques nouvellement générées.

**Points Clés :**

*   **Architecture Distincte :** Le Cypherock X1 Vault utilise une architecture où la phrase mnémonique est divisée en 5 fragments, stockés sur le dispositif et 4 cartes NFC. La reconstruction de la clé privée et la vérification du code PIN reposent sur l'interaction entre le Vault et ces cartes. L'élément sécurisé (SE) présent est uniquement utilisé pour la vérification de l'authenticité de l'appareil.
*   **Contrôle du Flux d'Exécution :** Des vulnérabilités dans le firmware open-source, telles qu'un accès hors limites sur un ID d'application lors du traitement des paquets USB, permettent à un attaquant de contrôler un pointeur de fonction. L'absence de protections comme Canary et Execute-Never facilite ensuite le détournement du flux d'exécution pour exécuter du code arbitraire (ROP ou shellcode).
*   **"Open-Source" Limité :** Bien que le firmware applicatif soit open-source, le Bootloader et le code de la zone de pare-feu (Firewall) ne le sont pas et sont conçus pour être non-modifiables. Ces sections non-publiques contiennent la logique de vérification du firmware.
*   **Contournement de la Protection Pare-feu :** Le mécanisme de pare-feu, censé isoler des zones de mémoire sensibles, présente une faille dans sa fonction d'écriture. Un attaquant peut exploiter cette faiblesse pour copier le code protégé du pare-feu dans la zone NVDATA, puis lire ces données.
*   **Logique de Mise à Jour Fragmentée :** Le processus de mise à jour du firmware est vulnérable. Les tâches du pare-feu peuvent être exécutées dans le désordre, et les signatures de firmware ne sont jamais écrites dans la mémoire Flash. De plus, la vérification à l'amorçage ne contrôle que l'intégrité et non l'authenticité. Ceci permet de remplacer le firmware par une version malveillante et de simuler une signature valide.
*   **Vérification d'Authenticité Illusoire :** La vérification d'authenticité de l'appareil, effectuée par l'élément sécurisé, repose sur une signature de firmware fournie par le logiciel de l'appareil. Le dispositif ne vérifie pas l'authenticité du cloud, et le cloud ne peut pas lire directement le firmware. Un attaquant peut donc facilement tromper ce système en renvoyant un résultat de succès localement.
*   **Attitude du Fabricant :** Le fabricant, Cypherock, a une approche jugée problématique concernant la gestion des vulnérabilités. Les rapports de failles sont souvent ignorés ou corrigés sans communication transparente, laissant les utilisateurs dans l'incertitude quant à la sécurité de leurs appareils.

**Vulnérabilités :**

*   **Contrôle du Flux d'Exécution (Control Flow Hijacking) :** Provient d'un accès hors limites (OOB) dans la fonction `registry_get_app_desc` lors de la sélection d'un applet basé sur `applet_id`.
*   **Écriture dans la Zone Pare-feu Protégée :** La fonction d'écriture du pare-feu permet à l'adresse `data` de pointer vers n'importe quelle adresse, y compris la zone de code du pare-feu, permettant sa copie dans NVDATA.
*   **Logique de Mise à Jour du Firmware :** L'indépendance des tâches du pare-feu et le manque de vérification d'authenticité du firmware à l'amorçage.
*   **Vérification d'Authenticité Unidirectionnelle :** L'appareil ne vérifie pas l'intégrité de la communication avec le cloud.

**Recommandations :**

*   Il est impératif que les utilisateurs soient conscients des risques potentiels liés à l'utilisation du Cypherock X1 Vault, compte tenu des vulnérabilités découvertes.
*   Les fabricants de portefeuilles matériels doivent adopter une approche transparente et proactive dans la gestion des failles de sécurité, en communiquant clairement avec leurs utilisateurs et la communauté de sécurité.
*   Une revue de code plus approfondie et des tests de pénétration réguliers sont nécessaires pour identifier et corriger les vulnérabilités avant qu'elles ne soient exploitées.

---
[Source](https://www.darknavy.org/blog/how_and_why_we_hacked_cypherock_hardware_wallet_the_full_story/){:target="_blank"}
