---
title: 'SOAPwn: Pwning .NET Framework Applications Through HTTP Client Proxies And WSDL'
date: 2025-12-10
permalink: /posts/2025/12/10/soapwn-pwning-net-framework-applications-through-http-client-proxies-and-wsdl/
tags:
- veille-cyber
- zerodaysfans
---
### Exploitation de Proxies HTTP .NET via WSDL

Une vulnérabilité critique a été découverte dans le framework .NET, permettant l'exécution de code à distance (RCE) dans des applications .NET. Cette faille découle du comportement inattendu des classes clientes HTTP du framework, telles que `SoapHttpClientProtocol`, `DiscoveryClientProtocol` et `HttpSimpleClientProtocol`. Ces classes, bien que conçues pour interagir via HTTP, peuvent être détournées pour écrire des données directement dans le système de fichiers local, ou même sur des partages réseau.

Le problème fondamental réside dans la manière dont la méthode `GetWebRequest` gère la création d'objets `WebRequest`. Au lieu de forcer un cast vers `HttpWebRequest`, elle utilise l'opérateur `as`, qui renvoie `null` si le schéma de l'URI n'est pas HTTP/HTTPS. Le code retourne ensuite l'objet `WebRequest` original, permettant ainsi l'utilisation de protocoles comme `file://` ou `ftp://` sans validation adéquate.

**Points Clés et Vulnérabilités :**

*   **Invalid Cast dans `HttpWebClientProtocol`:** Les classes clientes HTTP .NET peuvent être amenées à utiliser des gestionnaires non-HTTP (ex: `FileWebRequest`) si l'URL contrôlée par l'attaquant utilise un schéma différent de HTTP/HTTPS.
    *   **CVE-2025-34392:** Vulnérabilité spécifique au Barracuda Service Center RMM, permettant une RCE pré-authentifiée.
*   **Exploitation via WSDL Imports:** L'utilisation de `ServiceDescriptionImporter` pour générer des proxies SOAP à partir de fichiers WSDL contrôlés par l'attaquant offre un vecteur d'exploitation puissant. L'attaquant peut définir l'URL cible dans le WSDL, ce qui conduit à l'utilisation de schémas de fichiers dans le proxy généré. Cela permet :
    *   **Écriture de Fichiers Arbitraire:** Possibilité d'écrire le corps de la requête SOAP dans un fichier contrôlé par l'attaquant.
    *   **Téléchargement de Webshells ASPX:** En contrôlant les arguments de méthodes SOAP complexes ou les espaces de noms dans le WSDL, il est possible de déposer des webshells (ex: `.cshtml`) dans des emplacements web exécutables.
    *   **Livraison de Scripts Malveillants:** L'injection de code malveillant via les espaces de noms du WSDL permet l'exécution de scripts PowerShell.
*   **Relais NTLM/Divulgation de Challenge:** En pointant la requête SOAP vers un partage UNC (`file://\attacker.server\shareile`), un attaquant peut capturer les identifiants NTLM et tenter des attaques de relais.

**Produits Affectés (liste non exhaustive) :**

*   Barracuda Service Center RMM (CVE-2025-34392)
*   Ivanti Endpoint Manager (EPM)
*   Umbraco 8 CMS
*   Microsoft PowerShell
*   Microsoft SQL Server Integration Services

**Recommandations :**

*   **Mise à Jour des Applications:** Les développeurs utilisant les classes clientes HTTP .NET doivent s'assurer que les URLs utilisées sont strictement validées et proviennent de sources de confiance. Il est crucial de ne jamais consommer d'entrées non fiables pour définir ces URLs.
*   **Contrôle des WSDL:** Les applications générant des proxies SOAP à partir de WSDL doivent s'assurer que ces WSDL ne proviennent pas de sources non fiables.
*   **Surveillance des Activités:** Les équipes de sécurité doivent rechercher les utilisations suspectes de `ServiceDescriptionImporter` et des classes clientes HTTP .NET dans leurs environnements.
*   **Patchs des Fournisseurs:** Les utilisateurs des produits affectés devraient appliquer les correctifs disponibles. Microsoft a catégorisé ce problème comme un défaut d'implémentation de l'application plutôt qu'une faille du framework, privilégiant les mises à jour des produits finaux plutôt qu'une correction au niveau du framework.

---
[Source](https://labs.watchtowr.com/soapwn-pwning-net-framework-applications-through-http-client-proxies-and-wsdl/){:target="_blank"}
