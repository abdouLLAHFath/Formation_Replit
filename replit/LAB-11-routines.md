# LAB-11 · Planifier une routine

> **En une phrase —** Une routine planifiée depuis le chat relance un travail chaque semaine sans que vous soyez devant l'écran — avec un budget fixé et aucune action irréversible.

| ⏱️ Durée | 📂 Où | 🧩 Avant ce lab |
|:---:|:---:|:---:|
| 15 min | Barre latérale **Routines** | LAB-09 (fil Finance) ou tout projet |

## 🎯 À la fin de ce lab
- Une routine planifiée, son résultat lu, son budget fixé, puis mise en pause.
- 🧵 Fil Finance : une routine hebdomadaire qui relance l'analyse du dernier fichier de transactions.

> [!WARNING]
> ⚠️ **Vérifiez votre offre avant de commencer.** Les routines sont indisponibles sur l'offre Starter ; limitées à 5 routines actives par utilisateur sur Core, 10 sur Pro ; et fonctionnent uniquement en mode Power ou Max. Si votre offre ne le permet pas, suivez ce lab en **démonstration** avec le formateur plutôt qu'en pratique.

---

## Étape 1 · Planifier une routine simple · ⏱️ 6 min

1. Ouvrez **Routines** dans la barre latérale.
2. Créez une routine.

📋 **Prompt à coller**

```text
Chaque lundi à 9h, relis le dernier rapport du tableau de bord
financier et donne-moi un résumé en 5 lignes dans ce fil : montant
total, anomalies en attente, pièces manquantes. N'envoie rien à
l'extérieur, ne modifie aucun fichier, contente-toi de résumer.
```

3. Validez l'intervalle (une semaine, minimum une heure entre deux exécutions).

> [!TIP]
> **✅ Vous devez voir**
> - La routine apparaît dans la liste, avec son intervalle et son prochain déclenchement.

## Étape 2 · Fixer le budget · ⏱️ 3 min

1. Dans les réglages de la routine, fixez un **budget par exécution**.
2. Notez ce budget : c'est ce qui protège contre une routine qui dérape silencieusement.

## Étape 3 · Lire un résultat · ⏱️ 3 min

Si un déclenchement de test est possible, lancez-le et lisez le résumé renvoyé dans le fil. Sinon, décrivez à voix haute ce que vous attendez de voir dimanche prochain.

> [!NOTE]
> 💬 Par défaut, une routine utilise du **code déterministe** (moins coûteux), et ne fait appel à l'Agent que si un raisonnement est nécessaire — ici, la rédaction du résumé.

## Étape 4 · Mettre en pause · ⏱️ 3 min

1. Retournez dans **Routines**.
2. Mettez la routine en **pause**.
3. Vérifiez qu'elle apparaît bien comme « en pause », pas supprimée : vous pourriez la réactiver plus tard.

---

## ✅ Point de contrôle
- [ ] Routine planifiée avec un intervalle d'au moins une heure.
- [ ] Budget par exécution fixé.
- [ ] Routine mise en pause en fin de lab (ou capture de la démonstration du formateur).

## 🧠 À retenir
- Une routine travaille sans vous : budget, lecture régulière du résultat, et jamais d'action irréversible ni d'envoi externe sans validation.
- Starter n'y a pas accès ; vérifiez l'offre avant de promettre ce lab à un groupe.

<details>
<summary>🆘 Si ça coince</summary>

| Ce que vous voyez | Ce que vous faites |
|---|---|
| L'option Routines n'apparaît pas | Votre offre ne le permet pas (Starter, ou mode autre que Power/Max) : suivez la démonstration du formateur plutôt que de bloquer. |
| La routine semble vouloir envoyer un message à l'extérieur | Relisez le prompt : ajoutez explicitement `N'envoie rien à l'extérieur` et recréez la routine. |
| Pas de déclenchement de test possible | Décrivez simplement, à l'oral, le résultat attendu au prochain lundi — ce n'est pas bloquant pour la suite. |

</details>

---

➡️ **Lab suivant :** [LAB-12 · Quand l'IA se trompe](LAB-12-quand-ia-se-trompe.md)
