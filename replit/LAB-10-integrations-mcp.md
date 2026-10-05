# LAB-10 · Connecteur natif et serveur MCP

> **En une phrase —** Vous connectez un compte de test deux façons différentes — un connecteur natif (OAuth) et un serveur MCP (installé en un clic) — vous les utilisez depuis l'application, puis vous coupez les deux accès.

| ⏱️ Durée | 📂 Où | 🧩 Avant ce lab |
|:---:|:---:|:---:|
| 25 min | replit.com/integrations, puis votre projet | LAB-06 |

## 🎯 À la fin de ce lab
- Un connecteur natif (Drive ou Slack) connecté, utilisé, puis déconnecté.
- Un serveur MCP installé en un clic, utilisé dans le chat, puis déconnecté.
- Vous savez dire lequel des deux demande une autorisation OAuth, et lequel une URL.

---

## Étape 1 · Connecteur natif · ⏱️ 8 min

1. Dans la barre latérale, ouvrez **Integrations**.
2. Recherchez **Google Drive** ou **Slack**, choisissez un compte de **test**.
3. Autorisez via l'écran d'authentification du fournisseur.

> [!WARNING]
> ⚠️ Compte de test uniquement, **aucune donnée réelle**. Replit ne voit que ce que ce compte a le droit de voir.

### 🧵 Fil Finance

📋 **Prompt à coller**

```text
Quand le rapport Excel du tableau de bord est généré, dépose-le
automatiquement dans un dossier de test sur le Drive connecté
(ou envoie-le dans un canal Slack de test).
```

### 🧵 Fil Service client

📋 **Prompt à coller**

```text
Stocke la FAQ dans le Drive connecté au lieu du fichier local assets/,
et lis-la depuis là pour le chatbot.
```

> [!TIP]
> **✅ Vous devez voir**
> - Le fichier déposé dans le dossier de test, ou le message envoyé dans le canal de test.

## Étape 2 · Serveur MCP · ⏱️ 10 min

1. Toujours sur **replit.com/integrations**, repérez la section **MCP Servers for Replit Agent**.
2. Choisissez un serveur simple et gratuit à tester : **Notion** ou **Linear**.
3. Cliquez **Add to Replit** : l'autorisation s'ouvre directement dans l'éditeur.

> [!NOTE]
> 💬 Un serveur MCP installé, l'Agent récupère automatiquement la liste de ses outils. Pas de configuration de plus : on le nomme simplement dans le chat.

📋 **Prompt à coller**

```text
Utilise Notion (ou Linear) pour créer une page qui résume ce projet :
son objectif, son état d'avancement, et un lien vers l'application
publiée.
```

> [!TIP]
> **✅ Vous devez voir**
> - L'Agent choisit l'outil du serveur MCP correspondant sans que vous ayez eu à préciser lequel.
> - Une page ou un ticket créé côté Notion/Linear.

> [!WARNING]
> ⚠️ Un serveur MCP peut exposer des données et des actions sensibles, exactement comme un connecteur natif. On ne connecte que des serveurs **de confiance** — le catalogue Replit en est un, un serveur personnalisé inconnu ne l'est pas forcément.

## Étape 3 · Couper les deux accès · ⏱️ 5 min

1. Retournez sur **Integrations**.
2. Déconnectez le connecteur natif (Drive ou Slack).
3. Déconnectez le serveur MCP.
4. Vérifiez qu'un nouvel appel à l'un ou l'autre échoue désormais (c'est le signe que la coupure a bien fonctionné).

> [!NOTE]
> 💬 **Pour information, dans l'autre sens :** Replit peut lui-même être un serveur MCP (`mcp.replit.com/server/mcp`), piloté depuis Claude, ChatGPT ou Slack pour créer, chercher ou publier une Replit App. Pas pratiqué aujourd'hui, juste à savoir que ça existe.

---

## ✅ Point de contrôle
- [ ] Connecteur natif connecté, utilisé, puis déconnecté.
- [ ] Serveur MCP installé en un clic, utilisé dans le chat sans configuration supplémentaire, puis déconnecté.
- [ ] Vous pouvez expliquer en une phrase la différence entre les deux parcours.

## 🧠 À retenir
- Deux portes vers les mêmes outils externes : connecteurs natifs (OAuth, catalogue de 450+ services) et serveurs MCP (catalogue dédié, ou serveur personnalisé par URL).
- Compte de test, droits minimaux, accès révocable : la règle ne change pas selon la porte utilisée.

<details>
<summary>🆘 Si ça coince</summary>

| Ce que vous voyez | Ce que vous faites |
|---|---|
| Le fournisseur refuse l'autorisation | Vérifiez que vous utilisez bien un compte de test, et pas un compte personnel avec des restrictions. |
| L'Agent ne trouve pas d'outil Notion/Linear après connexion | Reformulez en nommant le service explicitement : `Utilise le serveur MCP Notion pour…`. |
| Le fichier Finance n'arrive pas sur le Drive de test | `Vérifie les permissions accordées au compte Drive connecté, puis réessaie le dépôt.` |

</details>

---

➡️ **Lab suivant :** [LAB-11 · Planifier une routine](LAB-11-routines.md)
