# Orséa Banque : analyse de risques IA et système de management ISO/IEC 42001

Suite du projet [SMSI ISO 27001 d'Orséa Banque](https://github.com/YlayannMR/SMSI_training). Orséa, une néobanque fictive, veut lancer Léa, un assistant conversationnel pour ses clients. Ce projet couvre la classification de ses systèmes d'IA selon l'AI Act, l'analyse d'impact et de risques de Léa, son traitement et le système de management de l'IA selon ISO/IEC 42001:2023.

Référentiels : ISO/IEC 42001:2023, règlement européen sur l'IA (AI Act) modifié par l'omnibus numérique, OWASP Top 10 pour les applications à base de grands modèles de langage (2025), RGPD, DORA.

## 1. Inventaire et classification AI Act

Orséa utilise ou prévoit trois systèmes d'IA. Le niveau de risque dépend de l'usage, pas de la technologie.

| Système | Niveau AI Act | Pourquoi | Échéance |
|---|---|---|---|
| Léa, assistant conversationnel | Risque limité | Interagit avec des personnes : obligation de transparence (article 50) | Déjà applicable |
| Détection de fraude sur les paiements | Risque minimal | L'annexe III exclut explicitement la détection de la fraude financière du haut risque | Déjà applicable (RGPD, article 22) |
| Score d'octroi de découvert | Haut risque | Évaluation de la solvabilité des personnes physiques (annexe III, point 5 b) | 2 décembre 2027 |

Fichier : [IA-01 Inventaire et classification](livrables/IA-01_Inventaire_classification_AI_Act.xlsx) (17 obligations détaillées et calendrier).

## 2. Analyse d'impact et de risques de Léa

14 risques analysés en six familles (attaques, données, erreurs, impact humain, disponibilité, conformité), chacun relié à l'OWASP Top 10 LLM, avec une analyse d'impact sur les clients, les clients vulnérables, les conseillers et la société.

Le seul risque élevé n'est pas une attaque : c'est la réponse inventée. Une banque reste responsable de ce que dit son assistant.

Un exemple de risque propre au secteur bancaire : l'injection indirecte par un libellé de virement. Un fraudeur envoie 1 € avec une consigne cachée dans le libellé ; quand le client demande à Léa de résumer ses opérations, elle lit la consigne.

Fichier : [IA-02 Analyse d'impact et registre des risques](livrables/IA-02_Analyse_impact_et_risques_Lea.xlsx).

## 3. Traitement et déclaration d'applicabilité

20 mesures techniques, organisationnelles et contractuelles. Le principe directeur : on ne peut pas empêcher toutes les injections ou les erreurs d'un modèle de langage, alors on limite ce qu'elles peuvent provoquer.

- Réponses ancrées sur les documents officiels de la banque, avec la source citée
- Libellés et contenus externes affichés tels quels, jamais interprétés comme des consignes
- Liste blanche : aucun numéro ni lien en dehors des canaux officiels
- Accès en lecture seule au seul compte du client connecté, contrôlé par le serveur
- Aucune action possible sur un compte
- Conseiller joignable à tout moment

| Niveau | Avant traitement | Après traitement |
|---|---|---|
| Élevé | 1 | 0 |
| Moyen | 11 | 5 |
| Faible | 2 | 9 |

Les 38 contrôles de l'Annexe A d'ISO/IEC 42001 sont applicables ; chacun est justifié et relié aux mesures.

Fichier : [IA-03 Traitement, risque résiduel et SoA ISO 42001](livrables/IA-03_Traitement_et_SoA_ISO42001_Lea.xlsx).

## 4. Système de management de l'IA (clauses 4 à 10)

| Clause | Exigence | Document |
|---|---|---|
| 4, 5 | Contexte, parties intéressées, périmètre, politique IA, rôles | [01-contexte-et-politique.md](aims/01-contexte-et-politique.md) |
| 6.1 | Risques, traitement, analyse d'impact | [IA-02](livrables/IA-02_Analyse_impact_et_risques_Lea.xlsx), [IA-03](livrables/IA-03_Traitement_et_SoA_ISO42001_Lea.xlsx) |
| 6.2, 6.3 | Objectifs, règle de mise en service, changements | [02-objectifs.md](aims/02-objectifs.md) |
| 7, 8 | Ressources, compétences, communication, documents, cycle de vie de Léa | [03-support-et-fonctionnement.md](aims/03-support-et-fonctionnement.md) |
| 9.1 | Indicateurs | [04-indicateurs.md](aims/04-indicateurs.md) |
| 9.2 | Audit interne (intégré au SMSI) et pré-audit | [05-audit-interne.md](aims/05-audit-interne.md) |
| 9.3 | Revue de direction | [06-revue-de-direction.md](aims/06-revue-de-direction.md) |
| 10 | Non-conformités et actions correctives | [07-amelioration.md](aims/07-amelioration.md) |

Le pré-audit a relevé deux non-conformités majeures : aucune formation à la maîtrise de l'IA alors que l'AI Act l'exige depuis février 2025 (article 4), et un contrat avec l'éditeur du modèle qui ne protège pas les conversations des clients. La revue de direction conditionne la mise en service de Léa à leur levée.

## 5. Synthèse pour la direction

[IA-04 Synthèse pour le comité exécutif](livrables/IA-04_Synthese_direction_Lea.pdf) : 6 slides, du constat aux quatre décisions demandées.

## Livrables

| Document | Fichier |
|---|---|
| Inventaire et classification AI Act | [IA-01_Inventaire_classification_AI_Act.xlsx](livrables/IA-01_Inventaire_classification_AI_Act.xlsx) |
| Analyse d'impact et registre des risques | [IA-02_Analyse_impact_et_risques_Lea.xlsx](livrables/IA-02_Analyse_impact_et_risques_Lea.xlsx) |
| Traitement, risque résiduel et SoA ISO 42001 | [IA-03_Traitement_et_SoA_ISO42001_Lea.xlsx](livrables/IA-03_Traitement_et_SoA_ISO42001_Lea.xlsx) |
| Synthèse pour le comité exécutif | [IA-04_Synthese_direction_Lea.pdf](livrables/IA-04_Synthese_direction_Lea.pdf) |
| Documents du système de management | [aims/](aims/) |

## Suite prévue

Étendre le périmètre au score de découvert, seul système à haut risque, avec l'analyse d'impact sur les droits fondamentaux exigée par l'article 27 de l'AI Act.

---

Orséa Banque est une entreprise fictive : les systèmes, les prestataires et les chiffres sont inventés pour l'exercice.
