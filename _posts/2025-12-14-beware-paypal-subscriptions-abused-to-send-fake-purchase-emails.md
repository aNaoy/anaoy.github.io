---
title: 'Beware: PayPal subscriptions abused to send fake purchase emails'
date: 2025-12-14
permalink: /posts/2025/12/14/beware-paypal-subscriptions-abused-to-send-fake-purchase-emails/
tags:
- veille-cyber
- bleepingcomp
---
**Arnaque par e-mail : Utilisation frauduleuse des abonnements PayPal pour de fausses notifications d'achats**

Une campagne d'hameçonnage exploite la fonctionnalité de facturation "Abonnements" de PayPal pour envoyer des e-mails légitimes contenant de fausses notifications d'achats. Ces e-mails, envoyés depuis l'adresse officielle "service@paypal.com", indiquent qu'un paiement important a été effectué pour un article coûteux (comme un appareil Sony, un MacBook ou un iPhone). Le montant facturé est généralement compris entre 1 300 et 1 600 $.

Pour tenter de masquer leur nature frauduleuse, les messages incluent des caractères Unicode afin de modifier l'apparence du texte et d'éviter les filtres anti-spam. Ils comportent également une URL de service client qui incorpore le détail de la fausse transaction et un numéro de téléphone destiné à annuler ou contester le paiement.

L'objectif de ces e-mails est de pousser les destinataires à contacter le faux support PayPal afin de les escroquer, potentiellement en leur faisant réaliser une fraude bancaire ou en les incitant à installer des logiciels malveillants.

**Points Clés :**

*   **Origine légitime des e-mails :** Les e-mails proviennent directement de PayPal ("service@paypal.com") et passent les contrôles de sécurité (DKIM, SPF), les rendant difficiles à distinguer des notifications authentiques.
*   **Exploitation de la fonction "Abonnements" :** Les fraudeurs utilisent la fonction "Abonnements" de PayPal pour générer ces e-mails. En suspendant un abonnement, PayPal envoie automatiquement une notification. Les escrocs semblent exploiter une faille ou une méthode non publique pour insérer des informations frauduleuses dans le champ URL du service client.
*   **Mécanisme de diffusion :** Les e-mails sont envoyés à une adresse e-mail associée à un faux abonné créé par les fraudeurs. Cette adresse est ensuite configurée pour transférer les e-mails à une liste de destinataires ciblés, souvent via une liste de diffusion Google Workspace.

**Vulnérabilités :**

*   La méthode exacte d'insertion de texte non-URL dans le champ "Customer Service URL" de PayPal n'est pas encore totalement élucidée, suggérant une possible faille dans la validation des données pour certaines configurations d'abonnements ou via des API spécifiques.
*   L'utilisation d'une fonction légitime de PayPal pour générer des communications frauduleuses permet de contourner les filtres de sécurité habituels.

**Recommandations :**

*   **Ignorer les e-mails suspects :** Ne jamais appeler le numéro de téléphone indiqué dans ces e-mails.
*   **Vérifier directement sur le compte PayPal :** En cas de doute concernant un paiement, se connecter à son compte PayPal directement via le site officiel ou l'application pour vérifier la présence de transactions non autorisées.
*   **Être vigilant :** Rester attentif aux messages inattendus et aux demandes inhabituelles.

PayPal a été contacté et a déclaré être conscient de cette campagne d'hameçonnage, rappelant l'importance de la vigilance et invitant les clients à contacter directement le support via les canaux officiels en cas de suspicion.

---
[Source](https://www.bleepingcomputer.com/news/security/beware-paypal-subscriptions-abused-to-send-fake-purchase-emails/){:target="_blank"}
