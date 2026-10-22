# Objectifs IA et planification (ISO 42001, clauses 6.2 et 6.3)

Document : IA-OBJ · Version 1.0 · Propriétaire : Responsable IA · Revue : à chaque revue de direction

## 6.1 Rappel : risques et impacts

L'appréciation des risques (6.1.2), le traitement (6.1.3) et l'analyse d'impact sur les personnes (6.1.4) sont documentés dans les fichiers [IA-02](../livrables/IA-02_Analyse_impact_et_risques_Lea.xlsx) et [IA-03](../livrables/IA-03_Traitement_et_SoA_ISO42001_Lea.xlsx). La déclaration d'applicabilité des 38 contrôles de l'Annexe A est dans IA-03.

**Critères d'acceptation des risques** : un risque élevé n'est jamais accepté ; un risque moyen est accepté par le propriétaire métier de Léa (directeur relation client) s'il est surveillé ; un risque faible est accepté d'office.

## 6.2 Objectifs du système de management de l'IA

| Id | Objectif | Indicateur | Cible | Échéance | Responsable | Mesures |
|---|---|---|---|---|---|---|
| O-IA-1 | Léa donne des réponses justes | Part des réponses correctes sur l'échantillon relu chaque semaine | au moins 97 % | 3 mois après mise en service | Directeur relation client | T-01, T-02, T-04 |
| O-IA-2 | Léa résiste aux détournements | Part des tests d'injection et d'extraction de consigne bloqués avant chaque mise en production | 100 % des tests critiques | Avant mise en service | Équipe data | T-03, T-05, T-07, T-08 |
| O-IA-3 | Aucune donnée client ne fuit par Léa | Nombre de violations de données liées à Léa | 0 | Permanent | RSSI | T-09, T-12, T-13 |
| O-IA-4 | Les clients gardent la main | Délai pour joindre un conseiller depuis Léa | moins de 2 minutes en journée | Avant mise en service | Directeur relation client | T-14, T-15 |
| O-IA-5 | Les équipes maîtrisent l'IA | Part des personnes concernées formées (AI Act, article 4) | 100 % | 3 mois après mise en service | Responsable IA | T-20 |
| O-IA-6 | Tout système d'IA est évalué avant mise en service | Part des systèmes de l'inventaire avec une analyse d'impact | 100 % | 02/12/2027 | Responsable IA | Inventaire IA-01 |

**Règle de mise en service** : Léa n'est ouverte aux clients que si les mesures de priorité P1 marquées « avant mise en service » sont réalisées et si les tests de la mesure T-03 atteignent leur seuil. Le responsable IA donne l'accord, le directeur relation client l'approuve.

## 6.3 Planification des changements

Tout changement de Léa passe par le comité IA (responsable IA, RSSI, DPO, équipe data, directeur relation client) :

| Changement | Exigence avant mise en production |
|---|---|
| Nouvelle version du modèle de l'éditeur | Rejouer le jeu de tests complet (T-03) |
| Nouvelle fonction ou nouvel outil pour Léa | Nouvelle analyse de risques ; une action sur le compte reste interdite sans décision du COMEX (T-10) |
| Nouvelle source dans la base de connaissances | Validation à deux personnes (T-18) |
| Changement d'éditeur | Analyse fournisseur, clauses contractuelles, tests complets (T-12, T-17) |
| Nouveau système d'IA | Inscription à l'inventaire, classification AI Act, analyse d'impact |
