---
title: 'DSLRoot, Proxies, and the Threat of ‘Legal Botnets’'
date: 2025-08-26
permalink: /posts/2025/08/26/dslroot-proxies-and-the-threat-of-legal-botnets/
tags:
- veille-cyber
- krebs
---
### Le Marché Gris des Proxies Résidentiels : DSLRoot et ses Risques

DSLRoot opère comme un fournisseur de services de proxy résidentiels, permettant à des individus aux États-Unis de monétiser leur connexion Internet en échange d'une rémunération mensuelle. Leurs clients, situés à l'étranger, utilisent ces connexions pour simuler une présence géographique américaine. L'entreprise, originaire d'Europe de l'Est et basée aux Bahamas, recrute des "agents régionaux" via des publicités et des forums en ligne, leur demandant d'installer du matériel dédié, comme des ordinateurs portables, connectés à leur réseau domestique.

Le modèle économique de DSLRoot, ainsi que d'autres acteurs similaires, suscite des inquiétudes majeures en matière de cybersécurité. Ces réseaux de proxies résidentiels, parfois qualifiés de "botnets légaux", peuvent être utilisés à des fins malveillantes, comme le contournement des restrictions géographiques, la diffusion de logiciels malveillants, ou encore la dissimulation d'activités illégales. L'affaire d'un membre de l'Air National Guard acceptant de fournir sa connexion à DSLRoot a mis en lumière les risques, notamment pour les personnes ayant des autorisations de sécurité élevées.

L'historique de DSLRoot remonte à au moins 2010, avec des liens établis entre ses opérateurs et des forums où étaient échangées des pratiques à la limite de la légalité, comme des programmes "pay-per-install" pour distribuer des logiciels indésirables. Des informations indiquent une connexion entre DSLRoot et des activités liées à l'incorporation d'entreprises et à la fourniture de cartes prépayées pour des transactions transfrontalières. L'opérateur présumé, Andrei Holas, aurait des liens avec la Biélorussie et les services de renseignement russes.

Le logiciel utilisé par DSLRoot pour gérer ces connexions résidentielles est capable d'exploiter des vulnérabilités spécifiques aux équipements réseau et de contrôler ces derniers à distance. Il peut également identifier les réseaux Wi-Fi voisins, étendant potentiellement son champ d'action au-delà de la connexion principale. L'entreprise semble avoir ajusté son modèle, se concentrant désormais uniquement sur les lignes DSL, une décision potentiellement motivée par la concurrence accrue et la complexité du marché des proxies résidentiels.

**Points Clés :**

*   **Modèle économique :** Monétisation des connexions Internet résidentielles américaines par des particuliers pour le compte d'entreprises de proxies.
*   **Risques associés :** Utilisation à des fins malveillantes (fraude, diffusion de malwares, dissimulation d'activités illégales), risque pour la sécurité nationale si utilisé par des acteurs étatiques hostiles.
*   **Historique :** Origines dans des pratiques de marketing en ligne douteuses et des liens potentiels avec des activités financières opaques.
*   **Technologie :** Logiciel permettant le contrôle à distance des équipements réseau des hôtes.
*   **Évolution du marché :** Intensification de la concurrence et possible restructuration des acteurs du secteur.

**Vulnérabilités et Exploits :**

*   L'article ne mentionne pas de CVE spécifiques. Cependant, le logiciel utilisé par DSLRoot est décrit comme performant des "exploits spécifiques aux fournisseurs" et l'utilisation d'"identifiants administratifs codés en dur" pour le contrôle à distance des équipements réseau. Cela implique une exploitation potentielle de faiblesses connues ou inconnues dans les appareils ciblés.
*   L'identification des réseaux Wi-Fi environnants pourrait être exploitée pour des attaques de type "man-in-the-middle" ou pour trouver d'autres cibles vulnérables.

**Recommandations :**

*   **Pour les utilisateurs domestiques :** Ne jamais accepter d'installer de matériel ou de logiciel provenant d'entreprises inconnues pour monétiser sa connexion Internet. Vérifier les termes de service de son fournisseur d'accès Internet (FAI) qui interdisent souvent ce type de revente.
*   **Pour les professionnels de la cybersécurité :** Être vigilant quant à l'émergence et à l'utilisation de réseaux de proxies résidentiels. Éduquer le grand public sur les risques associés à ces services.
*   **Pour les organisations :** Renforcer la surveillance du trafic réseau pour détecter toute activité suspecte ou non autorisée. Sensibiliser les employés aux risques de partager des informations ou des accès réseau avec des tiers non approuvés.

---
[Source](https://krebsonsecurity.com/2025/08/dslroot-proxies-and-the-threat-of-legal-botnets/){:target="_blank"}
