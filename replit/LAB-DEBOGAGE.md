# LAB-DEBOGAGE · Cinq cas, un par fil

> **En une phrase —** Cinq cas piégés, un par projet construit aujourd'hui, et toujours la même méthode en cinq temps : expliquer, choisir, corriger, tester, revenir en arrière si besoin.

| ⏱️ Durée | 📂 Où | 🧩 Avant ce lab |
|:---:|:---:|:---:|
| 1 h 15 (5 cas) + 15 min de théorie | Les cinq projets construits aujourd'hui | LAB-MINI-CRM |

## 🎯 À la fin de ce lab
- Cinq cas corrigés avec la méthode en cinq temps, dans cinq projets différents.
- Un réflexe : jamais deux corrections à la fois, toujours un test après chaque correction.
- Un retour arrière pratiqué au moins une fois pendant le lab.

> [!IMPORTANT]
> **🧭 La méthode, à chaque cas**
> 1. **Expliquer** en Plan, sans rien modifier.
> 2. **Choisir** la cause la plus probable.
> 3. **Corriger** en Build, une seule correction ciblée.
> 4. **Tester.**
> 5. **Revenir** au point de retour précédent si ça aggrave le problème.

---

## Cas 1 · RH — un CV mal lu · ⏱️ 15 min

Projet `rh-tri-cv`.

1. Reprenez **CAND-02** (un profil d'ingénieur logiciel senior, hors sujet pour un poste de coordinateur administratif, déjà présent dans `data/candidats.csv`).
2. Observez le score que l'IA lui donne.

📋 **Prompt à coller (en Plan)**

```text
Explique pourquoi CAND-02, qui a un profil d'ingénieur logiciel
senior et postule à un poste de coordinateur administratif, obtient
le score qu'il obtient. Ne modifie rien.
```

3. Corrigez en Build pour que le score reflète clairement l'inadéquation, avec l'explication qui le dit explicitement.

> [!TIP]
> **✅ Vous devez voir**
> Un score bas, avec une explication qui nomme l'inadéquation de métier — pas un score moyen sans justification.

## Cas 2 · Finance — un montant aberrant · ⏱️ 15 min

Projet `finance-cloture`.

1. Ajoutez une transaction fictive de 50 000 € pour la catégorie « Fournitures ».
2. Vérifiez si elle est signalée en anomalie.

📋 **Prompt à coller**

```text
Un montant de 50 000 € pour la catégorie Fournitures doit être
signalé comme anomalie, quelle que soit la plage actuellement
utilisée. Explique pourquoi il ne l'a pas été, puis corrige la règle.
```

> [!TIP]
> **✅ Vous devez voir**
> La transaction signalée en anomalie après correction, et la règle de détection ajustée (pas seulement ce cas particulier).

## Cas 3 · Ticketing — une assignation invalide · ⏱️ 15 min

Projet `atelier-nova-tickets`.

1. Essayez d'assigner un ticket à un utilisateur Marketing (ni Sales, ni Super Sale).

📋 **Prompt à coller (en Plan)**

```text
Explique pourquoi ce ticket a pu être assigné à un utilisateur
Marketing. Ne modifie rien.
```

2. Corrigez en Build pour que seuls les utilisateurs Sales et Super Sale actifs soient proposés.

> [!TIP]
> **✅ Vous devez voir**
> L'assignation à un utilisateur Marketing devient impossible ou refusée.

## Cas 4 · Projet — un statut non sauvegardé · ⏱️ 15 min

Projet `atelier-nova-projets`.

Si le bug de l'étape 4 du LAB-PROJECT-MANAGEMENT n'a pas été corrigé, ou pour vous entraîner une seconde fois :

1. Changez le statut d'une tâche, rechargez la page.
2. Si le statut est revenu en arrière, diagnostiquez en Plan, corrigez en Build.
3. Si la correction aggrave la situation (par exemple, plus aucun statut ne s'affiche), revenez au point de retour précédent.

> [!TIP]
> **✅ Vous devez voir**
> Le statut persiste après correction, et un retour arrière pratiqué si la première correction a aggravé le problème.

## Cas 5 · Mini CRM — un lien cassé · ⏱️ 15 min

Projet `atelier-nova-crm`.

1. Modifiez volontairement le formulaire de contact pour qu'il ne crée plus de lead (par exemple, en changeant le nom du champ attendu côté CRM).

📋 **Prompt à coller (à des fins de démonstration)**

```text
Renomme le champ « besoin » du formulaire en « message », sans mettre
à jour le mini CRM qui attend encore « besoin ».
```

2. Envoyez un formulaire test : constatez qu'aucun lead n'apparaît.
3. Diagnostiquez en Plan, corrigez en Build, retestez.

> [!TIP]
> **✅ Vous devez voir**
> Après correction, le formulaire test crée à nouveau un lead visible.

---

## ✅ Point de contrôle
- [ ] Cinq cas traités avec la méthode en cinq temps.
- [ ] Une seule correction ciblée par cas, jamais deux à la fois.
- [ ] Au moins un retour arrière pratiqué.
- [ ] Un journal noté pour chaque cas : cause trouvée, correction appliquée, résultat du test.

## 🧠 À retenir
- La méthode ne change pas d'un projet à l'autre : expliquer, choisir, corriger, tester, revenir en arrière si besoin.
- Un bug qu'on ne sait pas reproduire est un bug qu'on ne peut pas confirmer corrigé.

<details>
<summary>🆘 Si ça coince</summary>

| Ce que vous voyez | Ce que vous faites |
|---|---|
| Un cas ne se reproduit pas comme prévu | Reformulez le prompt de provocation du bug en étant plus précis sur le champ ou la règle concernée. |
| La correction casse autre chose | Revenez au point de retour précédent et redemandez une correction plus ciblée, en citant le fichier concerné. |
| Vous ne savez plus quelle était la cause initiale | Reconsultez votre journal de débogage : c'est pour ça qu'on le tient au fil de l'eau. |

</details>

---

➡️ **Lab suivant :** [LAB-ROUTINES-DEPLOIEMENT · Routines, secrets et mise en ligne](LAB-ROUTINES-DEPLOIEMENT.md)
