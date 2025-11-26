---
title: 'Microsoft: Security keys may prompt for PIN after recent updates'
date: 2025-11-26
permalink: /posts/2025/11/26/microsoft-security-keys-may-prompt-for-pin-after-recent-updates/
tags:
- veille-cyber
- bleepingcomp
---
**Clés de sécurité FIDO2 : une nouvelle exigence de code PIN sous Windows**

Suite aux mises à jour Windows publiées depuis septembre 2025, les clés de sécurité FIDO2 peuvent désormais demander la saisie d'un code PIN lors de la connexion. Ce changement affecte les appareils sous Windows 11 versions 24H2 et 25H2 lorsqu'un fournisseur d'identité requiert une vérification utilisateur.

Cette modification est conforme aux spécifications WebAuthn, qui régissent la manière dont les méthodes d'authentification gèrent les demandes de vérification. La vérification utilisateur confirme la présence et l'autorisation de l'utilisateur à utiliser une clé de sécurité. Conformément aux normes WebAuthn, cette vérification peut être déconseillée, préférée ou requise. Lorsque le paramètre est sur "préféré", la norme impose la configuration d'un code PIN si le dispositif d'authentification prend en charge la vérification utilisateur.

Ce comportement survient lorsque le fournisseur de services ou d'identité demande une vérification utilisateur "préférée" et que la clé FIDO2 n'a pas de code PIN configuré. Le support de cette fonctionnalité a été déployé progressivement après la mise à jour préliminaire KB5065789 et finalisé avec la mise à jour de sécurité KB5068861. L'ajout de la configuration du code PIN vise à assurer la cohérence entre les flux d'enregistrement et d'authentification.

**Points clés :**

*   Les clés de sécurité FIDO2 peuvent maintenant demander un code PIN sous Windows 11 après des mises à jour récentes.
*   Ce comportement est lié aux spécifications WebAuthn et à la configuration de la vérification utilisateur "préférée".
*   Il concerne les versions Windows 11 24H2 et 25H2.

**Vulnérabilités :**

*   Aucune vulnérabilité spécifique (avec CVE) n'est mentionnée dans l'article. Le changement est présenté comme une évolution intentionnelle pour se conformer aux standards.

**Recommandations :**

*   Les organisations et services qui souhaitent éviter la création ou la saisie de codes PIN pour les clés de sécurité peuvent configurer la vérification utilisateur sur "déconseillée" dans leurs paramètres de configuration WebAuthn.
*   Les utilisateurs devront potentiellement créer un code PIN pour se connecter avec une clé de sécurité, même s'il n'était pas requis initialement.

---
[Source](https://www.bleepingcomputer.com/news/microsoft/microsoft-fido2-security-keys-may-prompt-for-pin-after-recent-windows-updates/){:target="_blank"}
