---
title: 'ActivID administrator account takeover : the story behind HID-PSA-2025-002'
date: 2025-12-12
permalink: /posts/2025/12/12/activid-administrator-account-takeover-the-story-behind-hid-psa-2025-002/
tags:
- veille-cyber
- zerodaysfans
---
Voici un résumé des découvertes concernant la sécurité du produit ActivID Appliance de HID.

**Titre : Contournement d'authentification sur ActivID Appliance permettant la prise de contrôle du compte administrateur**

Une vulnérabilité a été découverte dans le produit ActivID Appliance de HID, utilisé mondialement pour sécuriser l'accès aux infrastructures critiques et aux données. Cette vulnérabilité, nommée HID-PSA-2025-002, permet un contournement d'authentification via l'API SOAP, menant à un accès administratif.

**Points Clés et Vulnérabilités :**

*   **Identification de la version :** La version spécifique du produit a été identifiée comme la 8.5 grâce à un artefact dans l'accord de licence de l'instance du client.
*   **Surface d'attaque :** L'analyse a révélé plusieurs services exposés, notamment SSH, nginx sur le port 443, et des services Java sur les ports 8443, 8445, etc., filtrés par un pare-feu (iptables).
*   **Architecture du produit :** Le produit utilise un proxy Nginx qui redirige les requêtes vers des services Java hébergés par Weblogic sur localhost. Ces services Java sont déployés sous forme de fichiers EAR et WAR.
*   **Analyse du code Java :** Les archives EAR et WAR ont été décompressées et leurs JARs décompilés. L'analyse de `web.xml` a permis de mapper les URL vers des classes Java spécifiques (Servlets et Filtres).
*   **Mécanisme d'authentification JAXWS :** Les EJBs exposés via JAXWS utilisent un `HandlerChain` (notamment `LoginHandler.java`) qui traite les en-têtes SOAP. Ce handler extrait un `MySubject` contenant potentiellement un ALSI (valeur utilisée comme session côté serveur).
*   **Vulnérabilité principale :** Le `SubjectHolder.subject` (un champ statique lié au thread) est utilisé pour gérer le contexte de sécurité.
    *   Si un en-tête SOAP `mySubjectHeader` avec un ALSI est fourni, mais qu'il n'est pas valide dans la base de données, une `AuthorizationException` est générée.
    *   Si **aucun en-tête d'authentification n'est fourni**, le `SubjectHolder.subject` reste tel qu'il a été défini précédemment. Ce comportement permet à un utilisateur non authentifié d'agir avec les privilèges de l'utilisateur dont le sujet a été défini en dernier.
*   **Scénario d'exploitation 1 (Bypass SYS_PKI) :** En effectuant des appels à `/ssp` sans authentification, puis un appel SOAP authentifié (qui échoue mais définit le sujet `AT_SYSPKI`), il devient possible d'exécuter des appels SOAP authentifiés en tant qu'utilisateur `AT_SYSPKI`. Ceci permet de récupérer des informations utilisateur.
*   **Scénario d'exploitation 2 (Création de compte administrateur) :** En s'authentifiant d'abord en tant qu'administrateur (par exemple, `ftadmin`), puis en utilisant l'exploitation précédente pour agir en tant que cet administrateur, il est possible de créer un nouveau compte utilisateur (`synacktivadm`) avec des privilèges d'administrateur (`RL_USERADM`). Ce nouveau compte peut ensuite être utilisé pour se connecter à la console d'administration.
*   **`CVE-2025-XXXX` (non spécifié dans l'article, mais implicitement lié à HID-PSA-2025-002).**

**Recommandations :**

*   **Mise à jour du logiciel :** HID Global a publié une mise à jour (FIXS2510005) pour corriger cette vulnérabilité. Il est impératif de mettre à jour le produit ActivID Appliance vers la dernière version disponible.
*   **Durcissement de l'authentification SOAP :** L'implémentation de l'authentification des services JAXWS devrait être revue pour s'assurer qu'une session valide est toujours requise et que les en-têtes SOAP ne sont pas utilisés pour contourner les mécanismes d'authentification existants. Le `SubjectHolder.subject` devrait être explicitement réinitialisé ou invalidé après utilisation ou en cas d'échec d'authentification.
*   **Surveillance des journaux :** Surveiller les journaux pour détecter les tentatives d'accès aux API SOAP et les erreurs d'autorisation inhabituelles peut aider à identifier des activités suspectes.

---
[Source](https://www.synacktiv.com/en/publications/activid-administrator-account-takeover-the-story-behind-hid-psa-2025-002){:target="_blank"}
