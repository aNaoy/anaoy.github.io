---
title: 'DDoS attacks over 1 Tbps surged fivefold in the second quarter'
date: 2026-08-11
permalink: /posts/2026/08/11/ddos-attacks-over-1-tbps-surged-fivefold-in-the-second-quarter/
tags:
- veille-cyber
- bleepingcomp
---
### Explosion des attaques DDoS massives au deuxième trimestre 2026

Le second trimestre 2026 a été marqué par une intensification spectaculaire des attaques par déni de service distribué (DDoS). Cloudflare rapporte une augmentation de 519 % des attaques dépassant le seuil critique de 1 Tbps par rapport au trimestre précédent, illustrée notamment par une attaque record de 31,4 Tbps orchestrée par le botnet Aisuru/Kimwolf.

**Points clés :**
*   **Volume record :** Plus de 800 attaques supérieures à 1 Tbps ont été mitigées au T2, contre 130 au T1.
*   **Tendance globale :** Le nombre total d'attaques DDoS au niveau réseau a progressé de 31,2 %, tandis que le volume de requêtes HTTP malveillantes a augmenté de 32,4 %.
*   **Techniques privilégiées :** Les attaques par inondation DNS (DNS floods) dominent, représentant 40 % des incidents au T2. Les inondations CLDAP ont bondi de 881,9 %.
*   **Cibles privilégiées :** Le secteur des médias et de l'édition est le plus visé, suivi par le secteur gouvernemental, particulièrement exposé en raison de tensions géopolitiques et d'actes de hacktivisme.
*   **Impact de la répression :** Une baisse de l'activité a été observée après avril, corrélée à l'opération *PowerOFF*, qui a démantelé plusieurs services de « DDoS à la demande ».

**Vulnérabilités :**
*   **Amplification DNS/CLDAP :** L'exploitation de ces protocoles reste un vecteur majeur permettant d'amplifier considérablement le trafic vers les cibles.
*   **Absence de CVE spécifique :** Bien que l'article mentionne des techniques d'amplification, il ne cite pas de vulnérabilités logicielles spécifiques (CVE) liées à ces attaques, celles-ci reposant davantage sur le détournement de protocoles réseaux standards que sur l'exploitation de failles logicielles précises.

**Recommandations :**
*   **Protection contre l'amplification :** Mettre en place des mesures de filtrage pour limiter les réponses DNS et CLDAP non sollicitées.
*   **Infrastructure résiliente :** Utiliser des services de protection Cloud capables d'absorber des pics de trafic massifs (Cloudflare souligne sa capacité à filtrer des attaques dépassant 30 Tbps).
*   **Surveillance proactive :** Renforcer la vigilance pour les secteurs sensibles (médias, gouvernement) face aux campagnes de hacktivisme en période de fortes tensions politiques.

---
[Source](https://www.bleepingcomputer.com/news/security/ddos-attacks-over-1-tbps-surged-fivefold-in-the-second-quarter/){:target="_blank"}
