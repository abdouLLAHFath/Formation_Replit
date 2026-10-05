# Labs Replit — De l'idée à l'application IA métier

13 labs pratiques, un par élément fondamental (Socle + 9 éléments + Synthèse + Projet final), construits sur une seule entreprise fictive : **Atelier Nova**, agence d'événementiel et de décoration de 12 personnes.

Trois fils rouges métier, à choisir dès le [LAB-03](LAB-03-mode-plan.md) (ou à partir du [LAB-04](LAB-04-assets.md) pour le Service client) et à suivre jusqu'au bout :
- 🧵 **RH** — tri et score de CV pour un poste de coordinateur·rice administratif·ve
- 🧵 **Finance** — clôture comptable mensuelle (transactions, classification, anomalies, dashboard, routine hebdomadaire)
- 🧵 **Service client** — chatbot RAG sur une FAQ

## Données fournies

Dossier [`data/`](data/) :
- `fiche-poste-coordinateur.md` — la fiche de poste RH
- `candidats.csv` — 10 candidatures fictives (dont les cas piégés : hors sujet, incomplet, mal formaté, quasi identiques)
- `transactions-septembre.csv` — 30 transactions fictives (dont un doublon et un montant aberrant volontaires)
- `faq-atelier-nova.md` — la FAQ du service client, découpée par question

Toutes les données sont **entièrement fictives**. Aucun nom, aucune coordonnée, aucun montant réel.

## Sommaire

| # | Lab | Élément fondamental | Durée |
|---|---|---|:---:|
| 01 | [Premier compte, premier résultat](LAB-01-premier-compte.md) | Socle | 20 min |
| 02 | [Prompt vague contre prompt structuré](LAB-02-prompt-structure.md) | Socle | 15 min |
| 03 | [Cahier des charges et plan de développement](LAB-03-mode-plan.md) | EF1 · Mode Plan | 30 min |
| 04 | [Assets : page d'accueil et site vitrine](LAB-04-assets.md) | EF2 · Assets | 20 min |
| 05 | [Importer un fichier de départ](LAB-05-import.md) | EF3 · Import | 15 min |
| 06 | [Clés API et Secrets](LAB-06-cles-api-secrets.md) | EF4 · Clés API & Secrets | 25 min |
| 07 | [Construire en petites étapes](LAB-07-mode-build.md) | EF5 · Mode Build | 35 min |
| 08 | [Faire expliquer son code](LAB-08-lecture-code.md) | EF6 · Lecture du code (Plan) | 15 min |
| 09 | [Partir d'un modèle, justifier ses dépendances](LAB-09-library-bibliotheques.md) | EF7 · Library & bibliothèques | 20 min |
| 10 | [Connecteur natif et serveur MCP](LAB-10-integrations-mcp.md) | EF8 · Intégrations / MCP | 25 min |
| 11 | [Planifier une routine](LAB-11-routines.md) | EF9 · Routines | 15 min |
| 12 | [Quand l'IA se trompe](LAB-12-quand-ia-se-trompe.md) | Synthèse | 25 min |
| 13 | [Projet final](LAB-13-projet-final.md) | Projet final | reste du temps |

## Conventions utilisées dans chaque lab

| Repère | Signification |
|---|---|
| 📋 **Prompt à coller** | Texte à copier tel quel dans l'Agent |
| 🧵 | Étape spécifique à un fil rouge (RH, Finance ou Service client) |
| ✅ **Vous devez voir** | Résultat attendu, pour vérifier avant de continuer |
| ⚠️ **Piège / vigilance** | Point de sécurité ou erreur fréquente |
| 💬 Note | Précision ou nuance sur la notion |
| 🆘 Si ça coince | Dépannage, en fin de fichier |

Référence complète du programme : [`Programme_Replit_v3.xlsx`](../Programme_Replit_v3.xlsx) · Support de présentation : [`Fondamentaux-Replit/fondamentaux-replit.html`](../Fondamentaux-Replit/fondamentaux-replit.html)
