---
title: 'BdThemes plugins supply-chain hack creates rogue WordPress admins'
date: 2026-08-11
permalink: /posts/2026/08/11/bdthemes-plugins-supply-chain-hack-creates-rogue-wordpress-admins/
tags:
- veille-cyber
- bleepingcomp
---
### Compromission de la chaîne d'approvisionnement des plugins BdThemes

Une attaque par chaîne d'approvisionnement a ciblé l'infrastructure de BdThemes, développeur de plugins WordPress populaires (Element Pack, Prime Slider, etc.). En compromettant le serveur API, les attaquants ont injecté du code malveillant dans un flux JSON utilisé par les plugins pour afficher des bannières promotionnelles dans le tableau de bord des administrateurs. Cette injection permet de créer des comptes administrateurs dissimulés et d'installer des portes dérobées (webshells) pour assurer la persistance sur les sites infectés.

**Points clés :**
*   **Vecteur d'attaque :** Empoisonnement du flux JSON via une compromission du serveur API (Sigmative API).
*   **Mode opératoire :** Le script malveillant s'exécute automatiquement lorsqu'un administrateur se connecte, sans nécessiter de mise à jour du plugin.
*   **Dissimulation :** Le code malveillant manipule les requêtes de la base de données pour masquer les comptes administrateurs créés frauduleusement.
*   **Impact :** Plus de 350 000 installations potentiellement exposées. Les plugins ont été retirés du répertoire WordPress.org par mesure de sécurité.

**Vulnérabilité :**
*   **Type :** Cross-Site Scripting (XSS) stocké.
*   **Localisation :** Bibliothèque "Biggop" utilisée par le composant "Biggopti".
*   **Cause :** Absence de nettoyage des sorties (insufficient output escaping) sur le paramètre `display_id`.
*   **CVE :** Non attribuée (classée sévérité "moyenne").

**Recommandations :**
*   **Vérification immédiate :** Inspecter la liste des utilisateurs de l'administration WordPress pour détecter tout compte suspect ou non autorisé.
*   **Audit de sécurité :** Rechercher la présence de fichiers suspects (ex: `emer-run.php`) ou de plugins installés sans approbation.
*   **Mise à jour :** Suivre les recommandations de l'équipe WordPress et du développeur pour appliquer les correctifs dès leur disponibilité.
*   **Surveillance :** En cas de doute, restaurer le site à partir d'une sauvegarde saine antérieure à juin 2026 et réinitialiser tous les mots de passe des comptes administrateurs.

---
[Source](https://www.bleepingcomputer.com/news/security/bdthemes-plugins-supply-chain-hack-creates-rogue-wordpress-admins/){:target="_blank"}
