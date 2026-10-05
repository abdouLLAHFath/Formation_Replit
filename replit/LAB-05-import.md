# LAB-05 · Importer un fichier de départ

> **En une phrase —** Vous importez un fichier CSV fourni, Replit construit une application autour de ces données, et vous obtenez un chiffre de contrôle recalculable avant de continuer.

| ⏱️ Durée | 📂 Où | 🧩 Avant ce lab |
|:---:|:---:|:---:|
| 15 min | replit.com/import | LAB-03 (ou LAB-04 pour le fil Service client) |

## 🎯 À la fin de ce lab
- Vous savez importer un fichier CSV et laisser l'Agent construire l'application qui en découle.
- 🧵 Fil Finance : votre fichier de transactions est nettoyé, avec un chiffre de contrôle exact.
- 🧵 Fil RH : vos dix candidatures sont importées, prêtes pour le score du LAB-07.

> Si vous suivez le fil Service client, ce lab est facultatif aujourd'hui : passez directement au LAB-06.

---

## Étape 1 · Télécharger le fichier fourni · ⏱️ 2 min

- 🧵 Fil RH : récupérez `data/candidats.csv` (dix candidatures fictives pour le poste de coordinateur·rice administratif·ve).
- 🧵 Fil Finance : récupérez `data/transactions-septembre.csv` (trente transactions fictives de septembre 2026).

## Étape 2 · Importer · ⏱️ 5 min

1. Allez sur **replit.com/import**.
2. Choisissez la source **Excel / CSV**.
3. Sélectionnez le fichier téléchargé à l'étape précédente.
4. Laissez l'Agent créer une application avec une base de données remplie de ces lignes.

> [!NOTE]
> 💬 Ne confondez pas deux sens du mot import : **l'Import de Replit** (ce que vous faites ici, apporter un fichier dans Replit) et **l'import de données dans une application** que vous auriez codée vous-même. Aujourd'hui, c'est le premier sens.

## Étape 3 · Vérifier ce qui n'a pas suivi · ⏱️ 3 min

📋 **Prompt à coller**

```text
Montre-moi un aperçu des données importées : nombre de lignes, noms
des colonnes, et dis-moi si une configuration (secrets, commande de
lancement) est encore à faire.
```

> [!TIP]
> **✅ Vous devez voir**
> - 🧵 RH : 10 lignes, colonnes `identifiant, intitule_cv, annees_experience_declarees, diplome_declare, langues_declarees, remarque`.
> - 🧵 Finance : 30 lignes, colonnes `id, date, fournisseur, categorie, montant_eur, piece_jointe, statut`.
> - Dans les deux cas, l'Agent signale qu'aucune clé API n'a été importée : normal, ce sera le LAB-06.

## Étape 4 · 🧵 Fil Finance seulement — nettoyer et dédoublonner · ⏱️ 5 min

📋 **Prompt à coller**

```text
Contrôle la qualité des données importées. En code, pas par
estimation : détecte les doublons exacts (même fournisseur, même
date, même montant) et retire-les. Donne-moi un rapport : lignes
lues, lignes retirées (avec leurs identifiants), lignes conservées,
montant total des lignes conservées.
```

> [!TIP]
> **✅ Vous devez voir un rapport proche de :**
> ```text
> Lignes lues : 30
> Doublon détecté : TX-0907 (identique à TX-0902 : même fournisseur,
>   même montant 86,40 €)
> Lignes conservées : 29
> Montant total : 64 840,35 €
> ```
> Le montant exact peut varier de quelques centimes selon l'arrondi choisi par l'Agent : l'important est 29 lignes et un seul doublon détecté.

> [!WARNING]
> ⚠️ Vous verrez aussi une ligne à 45 000,00 € (TX-0919, « Fournisseur Inconnu SARL ») : c'est volontaire, mais elle n'est **pas** un doublon — ne la laissez pas supprimer à cette étape. Elle sera traitée comme anomalie au LAB-09.

---

## ✅ Point de contrôle
- [ ] Fichier CSV importé, application créée par l'Agent.
- [ ] 🧵 RH : 10 candidatures visibles.
- [ ] 🧵 Finance : 29 lignes après dédoublonnage, montant total ≈ 64 840,35 €, la ligne à 45 000 € toujours présente (pas supprimée).

## 🧠 À retenir
- L'Import ne reprend ni les secrets, ni les données d'une base externe, ni les réglages d'origine : à refaire à part.
- Le nettoyage (doublons) est un travail de **code déterministe**, pas une estimation du modèle : on le demande explicitement.

<details>
<summary>🆘 Si ça coince</summary>

| Ce que vous voyez | Ce que vous faites |
|---|---|
| L'import échoue sur l'encodage ou le séparateur | Précisez dans le prompt : `Le séparateur est le point-virgule, l'encodage est UTF-8.` |
| Plus ou moins de 29 lignes après nettoyage | `Recompte : seules les lignes strictement identiques en fournisseur, date et montant sont des doublons. Montre-moi les lignes que tu as retirées.` |
| La ligne à 45 000 € a été supprimée | `Remets TX-0919 (45 000 €) dans les données : ce n'est pas un doublon, seulement un montant à vérifier plus tard.` |

</details>

---

➡️ **Lab suivant :** [LAB-06 · Clés API et Secrets](LAB-06-cles-api-secrets.md)
