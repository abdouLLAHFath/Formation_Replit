# LAB-TICKETING · Suivi des demandes

> **En une phrase —** Une file de support partagée pour Atelier Nova : un formulaire public qui crée des tickets, une assignation manuelle, des statuts suivis jusqu'à la clôture.

| ⏱️ Durée | 📂 Où | 🧩 Avant ce lab |
|:---:|:---:|:---:|
| 1 h 45 (6 étapes, en 3 parties) | Nouveau projet `Web app`, `atelier-nova-tickets` | LAB-RH |

## 🎯 À la fin de ce lab
- Un formulaire public qui crée des tickets sans que le client soit connecté.
- Des tickets internes, assignables à un commercial actif de l'entreprise.
- Des statuts (Open, In progress, Closed) et des priorités, suivis manuellement.
- La liaison entre le formulaire public et la liste des tickets, vérifiée de bout en bout.

---

## Partie 1 · Le formulaire public

### Étape 1 · Formulaire public · ⏱️ 20 min

📋 **Prompt à coller (en Build)**

```text
Crée une page publique de demande de support pour Atelier Nova, sans
connexion requise : sujet, description, nom du demandeur, e-mail,
priorité (Basse, Moyenne, Haute, Urgente). À l'envoi, affiche un
message « Demande reçue » et crée un ticket avec statut Open, non
assigné, source « Formulaire public ».
```

> [!TIP]
> **✅ Vous devez voir**
> Après l'envoi, « Demande reçue » à l'écran, et un nouveau ticket en Open, non assigné.

1. Copiez le lien public de ce formulaire et notez-le : vous le réutiliserez à l'étape 5.

### Étape 2 · Tickets internes · ⏱️ 15 min

📋 **Prompt à coller (en Build)**

```text
Ajoute, côté équipe, un bouton « Nouveau ticket » qui ouvre le même
formulaire (sujet, description, nom, e-mail, priorité), mais marque
le ticket créé avec la source « Interne » et l'auteur connecté.
```

> [!TIP]
> **✅ Vous devez voir**
> Un ticket créé avec la source « Interne » et votre nom comme auteur.

## Partie 2 · Assignation et suivi

### Étape 3 · Assignation, statuts, priorités · ⏱️ 20 min

📋 **Prompt à coller (en Build)**

```text
Sur la page de détail d'un ticket, ajoute un champ « Assigné à » qui
ne propose que des utilisateurs actifs de la même entreprise avec un
rôle Sales ou Super Sale, un champ Statut (Open, In progress, Closed)
et un bouton « Save changes » qui enregistre les modifications.
```

1. Assignez un ticket à un commercial actif.
2. Passez son statut en **In progress**, puis en **Closed**. Cliquez sur **Save changes** après chaque changement.

> [!WARNING]
> ⚠️ Un ticket peut rester non assigné : ce n'est pas une erreur. Il n'y a pas d'assignation automatique dans ce module.

> [!TIP]
> **✅ Vous devez voir**
> Le statut et l'assignation enregistrés après rechargement de la page.

### Étape 4 · Recherche et filtres · ⏱️ 20 min

📋 **Prompt à coller (en Build)**

```text
Sur la liste des tickets, ajoute une recherche par sujet, description,
nom ou e-mail du demandeur, des filtres par statut et par priorité,
et trie par défaut du ticket le plus récent au plus ancien. Affiche
une étiquette indiquant si le ticket vient du formulaire public ou de
l'interne.
```

> [!TIP]
> **✅ Vous devez voir**
> Une recherche qui filtre correctement, et le tri du plus récent au plus ancien par défaut.

## Partie 3 · Vérifier et corriger

### Étape 5 · Liaison formulaire → tickets · ⏱️ 15 min

1. Ouvrez le lien public noté à l'étape 1 dans un nouvel onglet (sans être connecté).
2. Envoyez une demande de test.
3. Revenez à la liste des tickets et retrouvez-la.

> [!NOTE]
> 💬 Ceci vérifie une liaison applicative interne, pas une intégration externe (EF8) : à confirmer avec votre formateur selon la version déployée.

> [!TIP]
> **✅ Vous devez voir**
> Le ticket test apparaît en moins d'une minute, en Open, non assigné, source « Formulaire public ».

### Étape 6 · Ticket mal assigné · ⏱️ 15 min

1. Essayez d'assigner un ticket à un utilisateur qui n'est ni Sales ni Super Sale (ou inactif).
2. Si l'application l'accepte, diagnostiquez en Plan, puis corrigez en Build.

📋 **Prompt à coller (en Plan)**

```text
Explique pourquoi ce ticket a pu être assigné à un utilisateur qui
n'est ni Sales ni Super Sale, ou qui est inactif. Ne modifie rien.
```

> [!TIP]
> **✅ Vous devez voir**
> Après correction, l'assignation à un utilisateur non éligible est refusée ou impossible à sélectionner.

---

## ✅ Point de contrôle
- [ ] Ticket créé par le formulaire public, en Open, non assigné.
- [ ] Ticket interne créé, source et auteur corrects.
- [ ] Assignation, statut et priorité enregistrés après Save changes.
- [ ] Recherche et filtres fonctionnels.
- [ ] Liaison formulaire → tickets vérifiée.
- [ ] Assignation invalide corrigée.

## 🧠 À retenir
- Ce module ne fait ni assignation automatique, ni e-mail de notification, ni fil de réponses : l'équipe contacte le client séparément, puis met à jour le ticket.
- Fermer un ticket le conserve ; seule la suppression (réservée aux administrateurs) le retire définitivement.

<details>
<summary>🆘 Si ça coince</summary>

| Ce que vous voyez | Ce que vous faites |
|---|---|
| Le ticket du formulaire public n'apparaît pas | Vérifiez que le formulaire enregistre bien l'entreprise associée au lien, pas une entreprise par défaut. |
| « Save changes » ne semble rien faire | Rechargez la page : le changement est peut-être enregistré mais l'écran ne s'est pas rafraîchi. |
| Tous les utilisateurs sont proposés pour l'assignation | Revoyez le filtre de rôle (Sales, Super Sale) et de statut (actif) dans le prompt de l'étape 3. |

</details>

---

➡️ **Lab suivant :** [LAB-FINANCE · Clôture comptable](LAB-FINANCE.md)
