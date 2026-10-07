# LAB-FINANCE · Clôture comptable

> **En une phrase —** Des transactions fictives nettoyées, classées par compte, passées au crible des anomalies, puis résumées dans une fiche comptable, un tableau de bord et un rapport exportable — le code calcule, l'IA classe et rédige, un humain valide.

| ⏱️ Durée | 📂 Où | 🧩 Avant ce lab |
|:---:|:---:|:---:|
| 2 h (6 étapes) | Nouveau projet `Web app`, `finance-cloture` | LAB-TICKETING |

## 🎯 À la fin de ce lab
- Un jeu de transactions nettoyé, avec un total de contrôle recalculable.
- Chaque transaction classée par compte, avec des anomalies détectées et testées sur des cas volontairement faux.
- Une fiche comptable par compte et par mois, un tableau de bord, un rapport Excel ou PDF.

> Données fournies : [`data/transactions-septembre.csv`](data/transactions-septembre.csv) — trente transactions fictives, dont un doublon et un montant aberrant volontaires.

---

## Étape 1 · Nettoyage des transactions · ⏱️ 20 min

📋 **Prompt à coller (en Build)**

```text
Importe les transactions d'Atelier Nova depuis le fichier fourni.
Détecte et signale les doublons et les valeurs manquantes, sans les
supprimer silencieusement : affiche-les pour validation. Calcule un
total de contrôle (somme et nombre de lignes).
```

> [!TIP]
> **✅ Vous devez voir**
> Le doublon signalé, et un total de contrôle qui correspond au calcul fait à la main sur le fichier source.

## Étape 2 · Classification par compte · ⏱️ 20 min

📋 **Prompt à coller (en Build)**

```text
Pour chaque transaction, propose un compte comptable (ex. Fournitures,
Prestataires, Salaires, Divers) avec une explication courte. Le
calcul des totaux reste fait par du code classique, pas par l'IA :
l'IA ne fait que classer et rédiger le commentaire.
```

1. Vérifiez cinq classements à la main.

> [!TIP]
> **✅ Vous devez voir**
> Chaque ligne a un compte et une explication ; les cinq classements vérifiés sont cohérents.

## Étape 3 · Détection des anomalies · ⏱️ 20 min

📋 **Prompt à coller (en Build)**

```text
Liste les anomalies : doublons, montants aberrants (hors de la plage
habituelle pour la catégorie), dates incohérentes. Pour chaque
anomalie, affiche la transaction et la raison du signalement.
```

1. Introduisez volontairement une nouvelle transaction en double et un montant aberrant, puis vérifiez qu'ils sont détectés.

> [!TIP]
> **✅ Vous devez voir**
> Le doublon fourni (dans le fichier source) et les deux cas ajoutés, tous détectés et expliqués.

## Étape 4 · Fiche comptable par compte et par mois · ⏱️ 20 min

📋 **Prompt à coller (en Build)**

```text
Génère une fiche comptable : pour chaque compte, le total du mois,
le nombre de transactions, et la liste des anomalies restantes à
traiter sur ce compte.
```

1. Vérifiez que le total de chaque fiche correspond à la somme des transactions de ce compte.

> [!TIP]
> **✅ Vous devez voir**
> Des totaux justes, et une fiche lisible même par quelqu'un qui n'a pas suivi la construction.

## Étape 5 · Tableau de bord · ⏱️ 20 min

📋 **Prompt à coller (en Build)**

```text
Ajoute un tableau de bord : total général, nombre d'anomalies en
attente, répartition des montants par compte (graphique simple).
```

> [!TIP]
> **✅ Vous devez voir**
> Trois indicateurs affichés, cohérents avec les fiches comptables de l'étape 4.

## Étape 6 · Génération du rapport Excel ou PDF · ⏱️ 20 min

📋 **Prompt à coller (en Build)**

```text
Ajoute un bouton « Exporter le rapport » qui produit un fichier
Excel et un fichier PDF reprenant le tableau de bord et les fiches
comptables. Le fichier doit pouvoir être téléchargé, jamais envoyé
automatiquement à l'extérieur.
```

1. Ouvrez le fichier exporté et vérifiez trois chiffres contre le tableau de bord.

> [!WARNING]
> ⚠️ Vérifiez qu'aucun envoi automatique (e-mail, webhook) n'a été ajouté sans qu'on vous l'ait demandé.

> [!TIP]
> **✅ Vous devez voir**
> Un fichier téléchargé, dont les chiffres correspondent exactement au tableau de bord.

---

## ✅ Point de contrôle
- [ ] Total de contrôle recalculable, doublon du fichier source signalé.
- [ ] Chaque transaction a un compte, cinq classements vérifiés.
- [ ] Doublon et montant aberrant ajoutés, tous deux détectés.
- [ ] Totaux de la fiche comptable corrects.
- [ ] Tableau de bord cohérent avec les fiches.
- [ ] Rapport exporté, chiffres vérifiés, rien envoyé à l'extérieur.

## 🧠 À retenir
- Le code calcule les totaux : c'est reproductible. L'IA classe et rédige : ça se relit. L'humain valide avant de signer une clôture.
- Un chiffre qui ne se vérifie pas à la main ne se publie pas.

<details>
<summary>🆘 Si ça coince</summary>

| Ce que vous voyez | Ce que vous faites |
|---|---|
| Le total de contrôle ne correspond pas | Vérifiez si une ligne a été supprimée au lieu d'être seulement signalée à l'étape 1. |
| Le montant aberrant ajouté n'est pas détecté | `Ce montant est hors de la plage habituelle pour sa catégorie. Explique pourquoi il n'a pas été signalé, puis corrige la règle de détection.` |
| L'export échoue | Vérifiez dans la Console le message d'erreur exact, et demandez à l'Agent de l'expliquer en mode Plan avant de corriger. |

</details>

---

➡️ **Lab suivant :** [LAB-CODE-BIBLIOTHEQUES · Lecture du code et bibliothèques](LAB-CODE-BIBLIOTHEQUES.md)
