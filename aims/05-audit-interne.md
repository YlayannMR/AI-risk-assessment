# Audit interne (ISO 42001, clause 9.2)

Document : IA-AUD · Version 1.0 · Propriétaire : Responsable de l'audit interne · Revue : annuelle

## Programme

Le système de management de l'IA est audité chaque année, **en même temps que le SMSI ISO 27001** : les deux normes ont la même structure (clauses 4 à 10), ce qui permet un audit intégré. L'auditeur est indépendant du responsable IA et de l'équipe data.

| Année | Périmètre | Période |
|---|---|---|
| 2027 | Clauses 4 à 10, contrôles A.5 (analyses d'impact), A.6 (cycle de vie), A.10 (éditeur du modèle) | Juin 2027 |
| 2028 | Clauses 4 à 10, contrôles A.2 à A.4, A.7 à A.9 | Juin 2028 |

Critères : ISO/IEC 42001:2023, politique IA d'Orséa, AI Act. Méthode : entretiens, revue documentaire, rejeu d'un échantillon des tests de sécurité, relecture de conversations.

## Pré-audit du 22 octobre 2026

- **Périmètre** : clauses 4 à 10 et déclaration d'applicabilité, avant la mise en service de Léa
- **Méthode** : revue documentaire

**Points forts**

- Inventaire des systèmes d'IA avec une classification AI Act argumentée, y compris le piège de la détection de fraude
- Analyse d'impact sur les personnes et registre des risques appuyé sur l'OWASP Top 10 LLM
- Choix de conception qui limite fortement les risques : Léa n'agit jamais sur un compte

**Constats**

| Id | Type | Exigence | Constat |
|---|---|---|---|
| NC-IA-01 | Non-conformité majeure | AI Act, article 4 ; ISO 42001, 7.2 et A.4.6 | Aucune formation à la maîtrise de l'IA n'a été dispensée, alors que l'obligation s'applique depuis février 2025. |
| NC-IA-02 | Non-conformité majeure | A.10.3 | Le contrat avec l'éditeur du modèle n'interdit pas la conservation ni l'entraînement sur les conversations des clients. |
| NC-IA-03 | Non-conformité mineure | 5.2 | La politique IA est rédigée mais pas encore approuvée par la direction. |
| NC-IA-04 | Non-conformité mineure | A.6.2.4 | Le jeu de tests d'avant mise en service n'est pas encore constitué. |
| NC-IA-05 | Non-conformité mineure | 8.4 ; RGPD, article 35 | L'analyse d'impact relative à la protection des données (AIPD) de Léa n'a pas été réalisée par le DPO. |
| OBS-IA-01 | Observation | 4.3 | Le score de découvert, seul système à haut risque de l'inventaire, est hors du périmètre. Il devra y entrer avant le 02/12/2027. |
| OBS-IA-02 | Observation | 9.1 | Les indicateurs sont définis mais ne pourront être mesurés qu'à la mise en service. |

**Conclusion** : le système est bien conçu. Léa ne doit pas être ouverte aux clients tant que les non-conformités majeures NC-IA-01 et NC-IA-02 ne sont pas levées.
