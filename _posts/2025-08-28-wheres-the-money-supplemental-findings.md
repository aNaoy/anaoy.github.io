---
title: 'Where’s the Money - Supplemental Findings'
date: 2025-08-28
permalink: /posts/2025/08/28/wheres-the-money-supplemental-findings/
tags:
- veille-cyber
- zerodaysfans
---
### Déséquilibres dans la Sécurité des Guichets Automatiques Diebold Nixdorf

Des recherches supplémentaires sur la suite de sécurité Vynamic Security Suite (VSS) de Diebold Nixdorf ont mis en évidence deux vulnérabilités exploitables, qualifiées de faible impact par le fournisseur. Ces failles affectent le module de chiffrement de disque de la VSS, qui utilise une partition Linux nommée Superschaf pour des vérifications d'intégrité avant le démarrage.

Les vulnérabilités identifiées exploitent des faiblesses dans la gestion des scripts d'initialisation du système d'exploitation Linux sous-jacent. Elles permettent notamment des actions non autorisées sur des partitions système critiques, ouvrant la voie à la découverte d'informations et potentiellement à l'exécution de code. Les versions VSS antérieures à 3.3.0 SR10, et plus spécifiquement SR9 et SR10, sont touchées par la première faille, tandis que la seconde vulnérabilité concerne principalement les versions antérieures à SR12.

Malgré les corrections apportées dans certaines versions, des régressions ont été observées, réintroduisant partiellement des failles dans des versions plus récentes comme VSS v3.3.0 SR16.

**Points Clés :**

*   **Architecture de Sécurité :** La VSS utilise une partition Linux (Superschaf) pour des vérifications d'intégrité avant le démarrage (PBA Phase I et II) via le binaire `Bootxsa.efi`.
*   **Index d'Intégrité :** L'intégrité de certains fichiers dans la partition Linux est validée par des sommes SHA256 stockées dans `Bootxsa.efi`. Cependant, tous les fichiers ne sont pas vérifiés.
*   **Scripts d'Initialisation :** Les vulnérabilités exploitent les scripts `mountfs` et `mountvirtfs` responsables du montage des systèmes de fichiers durant le démarrage.

**Vulnérabilités :**

*   **CVE-2024-46916 :**
    *   **Description :** Exploitation de la suppression des fichiers `/fastboot` et `/forcefsck` dans le script `mountfs`. Si ces fichiers n'existent pas, des modifications de liens symboliques dans `/etc/fstab` peuvent conduire à la persistance de l'accès aux répertoires protégés comme `/root` et `/var`. Cette vulnérabilité réapparaît dans VSS v3.3.0 SR16 où les instructions de suppression de `/fastboot` et `/forcefsck` sont toujours présentes dans `mountfs`, permettant potentiellement de modifier `/etc/fstab` pour accéder à des répertoires normalement inaccessibles.
    *   **Versions Affectées :** VSS v3.3.0 SR9, SR10, et potentiellement des versions plus récentes comme SR16 où les instructions sont réintroduites.
    *   **Impact :** Découverte d'informations, potentielle persistance d'accès.

*   **CVE-2024-46917 :**
    *   **Description :** Antérieurement à VSS v3.3.0 SR12, le script `S00mountvirtfs` s'exécutait avant `S40mountfs`. Cela permettait de déplacer ou de modifier le script `mountfs` (qui contenait des mesures de sécurité pour les répertoires `/root`, `/var`, `/tmp`) avant son exécution, rendant ces mesures inopérantes. Une autre méthode d'exploitation consistait à définir le bit d'immutabilité sur le répertoire `/root`, empêchant ainsi la suppression forcée de celui-ci lors de l'initialisation.
    *   **Versions Affectées :** VSS v3.3.0 antérieures à SR12.
    *   **Impact :** Contournement des mesures de sécurité, accès à des répertoires protégés.

**Recommandations :**

*   **Mises à Jour du Fournisseur :** Il est crucial que Diebold Nixdorf maintienne un processus de correction et de patching rigoureux pour adresser ces failles, même celles jugées de faible impact, car elles peuvent être composées avec d'autres vulnérabilités pour des attaques plus sérieuses.
*   **Surveillance des Scripts d'Initialisation :** Les équipes de sécurité devraient surveiller les modifications apportées aux scripts d'initialisation des systèmes d'exploitation embarqués et critiques.
*   **Vérification de l'Intégrité :** Renforcer les mécanismes de vérification d'intégrité pour inclure un plus large éventail de fichiers critiques sur la partition Linux, et ne pas se fier uniquement à une liste prédéfinie.
*   **Gestion des Droits d'Accès :** S'assurer que les permissions et les attributs de fichiers (comme l'immutabilité) sont correctement configurés et gérés pour prévenir les modifications non autorisées.

---
[Source](https://www.atredis.com/blog/2025/8/26/24nrgne4dqbwjxyip7txn8ep6zj057){:target="_blank"}
