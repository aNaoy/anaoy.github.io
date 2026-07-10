---
title: 'Laser Attack Resets Tangem Wallet Passwords on Cards That Cant Be Patched'
date: 2026-07-10
permalink: /posts/2026/07/10/laser-attack-resets-tangem-wallet-passwords-on-cards-that-cant-be-patched/
tags:
- veille-cyber
- hackernews
---
### Vulnérabilité physique critique des portefeuilles Tangem

Des chercheurs de l'équipe « Donjon » de Ledger ont découvert qu'une impulsion laser ciblée peut réinitialiser le mot de passe d'une carte Tangem, permettant à un attaquant de définir un nouveau code et d'accéder aux fonds sans connaître l'ancien. Cette faille repose sur une injection de faute laser qui trompe la puce sécurisée en lui faisant croire qu'elle est en mode de récupération.

**Points clés :**
* **Inaccessibilité d'un correctif :** Les cartes Tangem ne supportent pas les mises à jour logicielles (firmware). La faille est permanente pour l'ensemble des produits déjà en circulation.
* **Complexité élevée :** L'attaque nécessite un accès physique à la carte, un équipement de laboratoire spécialisé (estimé à 250 000 $) et une manipulation invasive (découpage de la carte).
* **Risque limité pour l'utilisateur moyen :** Compte tenu du coût de l'équipement et de l'incertitude sur la valeur contenue dans une carte volée, le risque pratique est considéré comme très faible pour le grand public.
* **Nature de la vulnérabilité :** Il s'agit d'une vulnérabilité liée au code applicatif (firmware) et non à la puce elle-même (EAL6+), rendant les protections matérielles inopérantes face à cette manipulation spécifique.

**Vulnérabilité :**
* La faille réside dans le mécanisme de vérification du firmware lors de la procédure de changement de mot de passe, qui peut être court-circuité par injection de faute laser. *Note : Aucune référence CVE n'est mentionnée dans l'article.*

**Recommandations :**
* **Prévention physique :** Conserver la carte dans un endroit sécurisé pour éviter tout vol.
* **Réaction en cas de perte :** Si une carte est perdue ou volée et qu'elle contient des fonds importants, l'utilisateur doit immédiatement transférer ses actifs vers un autre portefeuille ou une autre carte du set, car le mot de passe ne peut plus garantir la protection des fonds contre une attaque physique sophistiquée.

---
[Source](https://thehackernews.com/2026/07/laser-attack-resets-tangem-wallet.html){:target="_blank"}
