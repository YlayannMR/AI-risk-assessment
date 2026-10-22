# Support et fonctionnement (ISO 42001, clauses 7 et 8)

Document : IA-SUP · Version 1.0 · Propriétaire : Responsable IA · Revue : annuelle

## 7.1 Ressources

| Ressource | Description |
|---|---|
| Responsable IA | Rattaché à la direction des risques, pilote le système de management de l'IA |
| Équipe data | Deux personnes : conception, tests et surveillance de Léa |
| Sécurité | Le RSSI et le SOC du SMSI couvrent Léa (filtres, journaux, incidents) |
| Outils | Plateforme de tests, filtres d'entrée et de sortie, tableau de bord qualité |
| Éditeur du modèle | Modèle de langage appelé par API, contrat avec clauses de protection des données |

## 7.2 Compétences

| Rôle | Compétences requises | Preuve attendue |
|---|---|---|
| Responsable IA | ISO 42001, AI Act, gestion des risques | Certification ISO 42001 |
| Équipe data | Conception d'assistants à base de modèles de langage, tests de robustesse, sécurité des modèles (OWASP LLM) | Formation et expérience documentées |
| Conseillers | Reprise des conversations transférées, signalement des réponses fausses | Formation interne |
| COMEX | Enjeux et risques de l'IA | Session annuelle (AI Act, article 4) |

## 7.3 Sensibilisation

Toute personne qui conçoit, utilise ou supervise Léa connaît la politique IA, les limites de Léa (elle informe, elle n'agit pas) et la façon de signaler une réponse fausse ou un comportement anormal. La formation à la maîtrise de l'IA est obligatoire depuis février 2025 (AI Act, article 4).

## 7.4 Communication

| Quoi | À qui | Quand | Comment |
|---|---|---|---|
| « Vous échangez avec une IA » | Clients | À chaque conversation | Message d'accueil de Léa |
| Notice sur l'usage de l'IA par Orséa | Clients et public | Permanent | Page du site et de l'appli |
| Tableau de bord qualité de Léa | Comité IA, COMEX | Chaque mois, chaque trimestre | Comité IA, revue de direction |
| Incident grave lié à Léa | Autorités (CNIL, ACPR), clients concernés | Dans les délais légaux | Procédure d'incident du SMSI |
| Incident chez l'éditeur | Orséa | Selon le contrat | Clause de notification |

## 7.5 Informations documentées

| Document | Clause | Emplacement |
|---|---|---|
| Domaine d'application, politique, rôles | 4.3, 5.2, 5.3 | [01-contexte-et-politique.md](01-contexte-et-politique.md) |
| Inventaire et classification | 6.1 | [IA-01](../livrables/IA-01_Inventaire_classification_AI_Act.xlsx) |
| Appréciation des risques et analyse d'impact | 6.1.2, 6.1.4, 8.2, 8.4 | [IA-02](../livrables/IA-02_Analyse_impact_et_risques_Lea.xlsx) |
| Traitement des risques et déclaration d'applicabilité | 6.1.3, 8.3 | [IA-03](../livrables/IA-03_Traitement_et_SoA_ISO42001_Lea.xlsx) |
| Objectifs | 6.2 | [02-objectifs.md](02-objectifs.md) |
| Indicateurs | 9.1 | [04-indicateurs.md](04-indicateurs.md) |
| Audit interne | 9.2 | [05-audit-interne.md](05-audit-interne.md) |
| Revue de direction | 9.3 | [06-revue-de-direction.md](06-revue-de-direction.md) |
| Non-conformités | 10.2 | [07-amelioration.md](07-amelioration.md) |

Les règles de maîtrise documentaire du SMSI d'Orséa s'appliquent : identifiant, version, propriétaire, approbation, archivage.

## 8. Fonctionnement : le cycle de vie de Léa

| Phase | Ce qui est fait | Point de contrôle |
|---|---|---|
| 1. Besoin | Usage prévu défini : informer et orienter, aucune action sur le compte | Inscription à l'inventaire, classification AI Act |
| 2. Analyse | Analyse d'impact et de risques (8.2, 8.4) | Validation par le comité IA |
| 3. Conception | Consigne système, connexion aux données en lecture seule, filtres, liste blanche | Revue de conception par le RSSI |
| 4. Tests | Jeu de tests : exactitude, injections, extraction de consigne, clients vulnérables | Seuil de réussite atteint |
| 5. Mise en service | Mesures P1 réalisées, mention IA active | Accord du responsable IA, approbation du propriétaire métier |
| 6. Exploitation | Relecture d'échantillons, indicateurs, gestion des incidents | Comité IA mensuel |
| 7. Changement ou retrait | Nouvelle version, nouvel éditeur, arrêt du service | Procédure de la clause 6.3 |

Les appréciations des risques (8.2) et les analyses d'impact (8.4) sont refaites chaque année et à chaque changement important. Le traitement (8.3) est suivi dans le plan de traitement du fichier IA-03.
