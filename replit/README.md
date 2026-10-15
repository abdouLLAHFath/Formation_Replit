# Formation Replit - Atelier pratique

Ce dépôt rassemble les supports et les labos pratiques d'une formation sur Replit, centrée sur une approche pédagogique concrète et progressive.

Objectif : apprendre à concevoir, développer, tester, sécuriser et déployer des applications métier en tirant parti de l'Agent Replit — en travaillant par étapes courtes (Plan → Build → Test → Debug).

---

## Contenu du dépôt

- Dossier principal des labs : `replit/` (fichiers Markdown pour chaque lab, jeux de données dans `replit/data/`).
- Diaporama complet de présentation : `replit/replit-presentation-globale.html` (40 diapositives, 8 parties) — utile pour une vue d'ensemble et comme support de cours.

Structure (extrait) :

```text
replit/
├── replit-presentation-globale.html   # diaporama 40 slides
├── LAB-1-SOCLE.md
├── LAB-2-MINI-CRM.md
├── LAB-3-PROJECT-MANAGEMENT.md
├── LAB-4-RH.md
├── LAB-5-TICKETING.md
├── data/
```

---

## À qui s'adresse la formation

- Débutants en programmation et professionnels souhaitant prototyper une application métier rapidement.
- Public de formation et enseignants voulant montrer le cycle complet : besoin → prototype → test → déploiement.

Prérequis : aucun en programmation. Un compte Replit (Starter suffit pour la plupart des labs), un navigateur et une connexion Internet.

---

## Que couvre la formation (en un coup d'œil)

Le diaporama `replit-presentation-globale.html` et les labs couvrent :

- Création de compte et plans (Starter / Core / Pro / Enterprise) — limites et points à vérifier.
- L'Agent Replit : modes Plan et Build, prompts structurés, Routines, points de retour.
- Environnement : éditeur, Console / Shell, checkpoints, collaboration en direct.
- Données & sécurité : Secrets, Replit Database, Postgres intégré, bonnes pratiques.
- Déploiement : types (Autoscale, Static, Reserved VM, Scheduled), suivi, logs et coûts.
- Cas pratiques par fil métier : RH (tri et scoring CV), Ticketing, Project Management, Mini CRM, Debugging.

---

## Les labs disponibles

Chaque lab est un guide pas à pas (prompts prêts à coller, objectifs, vérifications) :

- LAB-1-SOCLE.md — Replit Agent et prise en main (Plan / Build / point de retour)
- LAB-2-MINI-CRM.md — Site vitrine, formulaire, mini CRM, conversion lead→prospect
- LAB-3-PROJECT-MANAGEMENT.md — Suivi de projet : tâches, statuts, bug volontaire
- LAB-4-RH.md — Tri et scoring de CV assisté par IA (DeepSeek), décisions humaines
- LAB-5-TICKETING.md — Formulaire public, tickets, assignation, filtres et validation

Consultez chaque fichier pour les prompts, la durée estimée et les points de contrôle.

---

## Méthode pédagogique

- Plan : définir le besoin et découper la tâche (lecture seule — aucun fichier modifié).
- Build : laisser l'Agent générer/modifier le code (un point de retour est créé pour chaque tâche).
- Test : valider le comportement visible (preview / déploiement local).
- Debug : diagnostiquer à partir des logs/console, corriger et retester.
- Retour arrière : utiliser les checkpoints si une modification aggrave la situation.

Règle pratique : "un prompt — un test — un point de retour".

---

## Sécurité et bonnes pratiques

- Ne jamais stocker de clés dans le code : utiliser l'onglet Secrets et des variables d'environnement.
- En formation, n'utilisez que des données factices.
- Relire systématiquement le code généré avant publication.
- Restreindre les permissions des clés externes au strict nécessaire.

---

## Parcours recommandé

1. LAB-1 — Socle et prise en main
2. LAB-4 — RH (IA & données sensibles)
3. LAB-5 — Ticketing (formulaire public → ticket)
4. LAB-3 — Project Management (tâches et suivi)
5. LAB-2 — Mini CRM (site vitrine, leads et prospection)

Ce parcours suit la logique pédagogique des fichiers et prépare à affronter les cas de debug et de sécurité.

---

## Ressources

- Diaporama (présentation globale) : `replit/replit-presentation-globale.html` — 40 diapositives, 8 parties
- Documentation Replit : https://docs.replit.com
- Tarifs et plans : https://replit.com/pricing (vérifier avant la session)

---
