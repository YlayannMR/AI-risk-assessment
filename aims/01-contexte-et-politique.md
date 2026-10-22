# Contexte et politique IA (ISO 42001, clauses 4 et 5)

Document : IA-POL · Version 1.0 · Propriétaire : Responsable IA · Revue : annuelle

## 4.1 Enjeux internes et externes

Orséa Banque veut améliorer son service client avec Léa, un assistant conversationnel intégré à l'application mobile. Léa répond aux questions des clients et les aide à consulter leurs opérations. Elle s'appuie sur un grand modèle de langage fourni par un éditeur externe.

**Rôle d'Orséa** : fournisseur et déployeur du système Léa (elle l'assemble et le met en service sous son nom), utilisateur du modèle de l'éditeur.

**Enjeux externes**

| Enjeu | Effet sur le système d'IA |
|---|---|
| AI Act | Obligation de transparence (article 50) depuis le 02/08/2026 ; maîtrise de l'IA (article 4) |
| RGPD | Les conversations contiennent des données personnelles et bancaires ; une analyse d'impact (AIPD) est nécessaire |
| DORA | L'éditeur du modèle est un prestataire TIC : contrat, suivi, stratégie de sortie |
| Secret bancaire | Les informations du client ne doivent pas être divulguées à un tiers |
| Menaces propres aux modèles de langage | Injection de prompt, contournement des protections, fuite de données, réponses inventées |
| Attentes des clients | Réponses rapides et justes, à toute heure, en langage simple |

**Enjeux internes**

| Enjeu | Effet sur le système d'IA |
|---|---|
| Support client saturé | Léa doit traiter les questions simples pour libérer les conseillers |
| Équipe data réduite | Peu de compétences internes en sécurité des modèles de langage |
| Dépendance à un éditeur unique | Risque en cas de panne, de changement de prix ou de conditions |
| SMSI ISO 27001 en place | Le système de management de l'IA s'appuie sur les processus existants (risques, incidents, fournisseurs) |

## 4.2 Parties intéressées

Une attente est toujours ce que la partie intéressée attend **d'Orséa**.

| Partie intéressée | Ce qu'elle attend d'Orséa | Exigence retenue |
|---|---|---|
| Clients | Des réponses justes, la confidentialité de leurs données, savoir qu'ils parlent à une IA, pouvoir joindre un humain | Oui |
| Clients vulnérables | Ne pas être induits en erreur sur leurs frais, leur découvert ou leurs droits | Oui |
| Conseillers du service client | Des conversations transmises avec leur historique, des réponses de Léa cohérentes avec les procédures | Oui |
| Direction d'Orséa | Un meilleur service client, sans incident d'image ni sanction | Oui |
| Délégué à la protection des données | Le respect du RGPD : minimisation, AIPD, droits des personnes | Oui |
| CNIL | Le respect du RGPD sur les données traitées par Léa | Oui |
| ACPR | La maîtrise du risque TIC et du prestataire (DORA), la protection de la clientèle | Oui |
| Autorité de surveillance de l'AI Act | Le respect de l'obligation de transparence | Oui |
| Éditeur du modèle de langage | Le respect de ses conditions d'utilisation, l'absence d'usage détourné, le signalement des incidents | Oui |
| Hébergeur cloud | Le respect du contrat et de la responsabilité partagée | Oui |

## 4.3 Domaine d'application du système de management de l'IA

**Intitulé** : « Le système de management de l'IA couvre la conception, le déploiement et l'exploitation de Léa, l'assistant conversationnel client d'Orséa Banque, y compris le modèle de langage externe qu'elle utilise et les données qu'elle traite. »

- **Inclus** : l'assistant Léa, ses consignes système, ses connexions aux données des clients, l'interface avec l'éditeur du modèle, le transfert vers un conseiller, les journaux de conversation.
- **Exclus pour l'instant** : le modèle de détection de fraude (risque minimal) et le score de découvert (haut risque, qui fera l'objet d'une analyse dédiée).
- **Interfaces** : SMSI ISO 27001 d'Orséa (gestion des incidents, des fournisseurs et des accès), processus RGPD du DPO.

## 5.2 Politique IA

Orséa Banque utilise l'intelligence artificielle pour mieux servir ses clients, dans le respect de leurs droits et de leur confiance. Elle s'engage à :

1. **Informer** : tout client sait qu'il échange avec une IA et peut demander un conseiller humain à tout moment.
2. **Protéger** : aucune donnée client n'est utilisée pour entraîner un modèle externe ; seules les données nécessaires à la réponse sont transmises.
3. **Garder l'humain dans la boucle** : Léa ne prend aucune décision sur le compte d'un client ; elle informe et oriente.
4. **Maîtriser les risques** : chaque système d'IA est inventorié, classé selon l'AI Act et fait l'objet d'une analyse d'impact et de risques avant sa mise en service.
5. **Surveiller** : la qualité des réponses, les incidents et les tentatives de détournement sont suivis en continu.
6. **Former** : les personnes qui conçoivent, utilisent ou supervisent un système d'IA sont formées.

## 5.3 Rôles et responsabilités

| Rôle | Responsabilité |
|---|---|
| Comité exécutif | Approuve la politique IA et les risques résiduels |
| Responsable IA (rattaché à la direction des risques) | Pilote le système de management de l'IA, l'inventaire et les analyses |
| Directeur relation client | Propriétaire métier de Léa, accepte les risques résiduels |
| Équipe data | Conçoit, teste et surveille Léa |
| RSSI | Sécurité de Léa et de son intégration, gestion des incidents |
| DPO | Analyse d'impact RGPD, droits des personnes |
| Achats | Contrat avec l'éditeur du modèle, clauses DORA |
