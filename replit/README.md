# Labs Replit — De l'idée à l'application IA métier

9 labs pratiques, un par fil de la formation (Socle + 7 blocs métier + Débogage + Routines/Déploiement), construits sur une seule entreprise fictive : **Atelier Nova**, agence d'événementiel et de décoration de 12 personnes.

Chaque lab est **unique à son fil** et se déroule en **étapes numérotées**, chacune d'au plus 20 minutes. Le bloc « Import et assets » (élément 7) reste théorique, sans lab : voir la présentation.

## Données fournies

Dossier [`data/`](data/) :
- `fiche-poste-coordinateur.md` — la fiche de poste RH
- `candidats.csv` — 10 candidatures fictives (dont les cas piégés : hors sujet, incomplet, mal formaté, quasi identiques)
- `transactions-septembre.csv` — 30 transactions fictives (dont un doublon et un montant aberrant volontaires)
- `faq-atelier-nova.md` — non utilisé par les labs actuels (ancien fil Service client), conservé pour référence

Toutes les données sont **entièrement fictives**. Aucun nom, aucune coordonnée, aucun montant réel.

## Sommaire

| # | Lab | Étapes | Éléments fondamentaux | Durée |
|---|---|:---:|---|:---:|
| 1 | [Replit Agent et socle](LAB-SOCLE.md) | 3 | Socle, EF1, EF5 | 55 min |
| 2 | [RH · Tri et score de CV](LAB-RH.md) | 9 | EF1, EF4, EF5, débogage, sécurité | 2 h 40 |
| 3 | [Ticketing · Suivi des demandes](LAB-TICKETING.md) | 6 | EF5, EF8 (à confirmer), débogage | 1 h 45 |
| 4 | [Finance · Clôture comptable](LAB-FINANCE.md) | 6 | EF5 | 2 h |
| 5 | [Lecture du code et bibliothèques](LAB-CODE-BIBLIOTHEQUES.md) | 4 | EF6, EF7 | 1 h |
| 6 | [Project Management](LAB-PROJECT-MANAGEMENT.md) | 4 | EF1, EF5, EF6, débogage | 1 h 15 |
| 7 | *(théorie seule : import, EF3, et assets, EF2 — voir la présentation)* | — | EF2, EF3 | 20 min |
| 8 | [Mini CRM · Site, formulaire, leads et prospects](LAB-MINI-CRM.md) | 9 | EF2, EF5, EF8, débogage | 2 h 55 |
| 9 | [Débogage · Cinq cas, un par fil](LAB-DEBOGAGE.md) | 5 | Débogage | 1 h 15 |
| 10 | [Routines, secrets et mise en ligne](LAB-ROUTINES-DEPLOIEMENT.md) | 3 | EF9, EF4, déploiement | 50 min |

Le bloc 11 (récapitulatif) est une théorie de clôture, sans lab : voir la présentation.

## Conventions utilisées dans chaque lab

| Repère | Signification |
|---|---|
| 📋 **Prompt à coller** | Texte à copier tel quel dans l'Agent |
| ✅ **Vous devez voir** | Résultat attendu, pour vérifier avant de continuer |
| ⚠️ **Piège / vigilance** | Point de sécurité ou erreur fréquente |
| 💬 Note | Précision ou nuance sur la notion |
| 🆘 Si ça coince | Dépannage, en fin de fichier |

Référence complète du programme : [`Plan_Formation_Replit.docx`](Plan_Formation_Replit.docx) · Support de présentation : [`Fondamentaux-Replit/formation-replit.html`](../Fondamentaux-Replit/formation-replit.html)

## Anciens labs

Les 13 anciens labs (`LAB-01` à `LAB-13`, à un élément par fichier, avec choix de fil dès le LAB-03) ont été remplacés par les 9 labs ci-dessus, chacun dédié à un seul fil. Ils ne sont plus dans ce dossier ; ils restent consultables dans l'historique Git si besoin.
