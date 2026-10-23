---
title: Quêtes journalières
description: "Les quêtes renouvelées chaque jour : comment les consulter avec /dailyquests, les compléter et récupérer leurs récompenses."
order: 4
keywords:
  - quête
  - daily
  - journalière
  - reroll
---

Chaque jour, le serveur vous propose un lot de **quêtes journalières** : des petits objectifs à accomplir en jouant
normalement, récompensés par des clés de caisse. Cette page explique comment consulter votre lot, compléter chaque
quête et ce que rapportent le lot et son bonus de complétion.

## Consulter vos quêtes

Ouvrez le menu avec la commande `/dailyquests` ou son raccourci `/dq` :

```text
/dailyquests
/dq
```

La fenêtre qui s'ouvre liste vos quêtes du jour, avec pour chacune l'objectif et votre progression actuelle. Les
quêtes sont générées à la première connexion du jour : si vous vous déconnectez puis revenez, vous retrouvez les
mêmes quêtes avec la même progression.

> [!NOTE]
> La journée de quêtes change à minuit : un nouveau lot est alors tiré.

## Compléter une quête

Chaque quête demande de fournir une quantité précise d'un élément, tirée au hasard dans une plage de valeurs. Trois
types d'objectifs existent :

- **Vendre des items** : la quête progresse quand vous vendez les objets demandés avec `/sell`.
- **Casser des blocs** : casser les blocs demandés, dans une famille comme la pierre ou le bois.
- **Récolter des cultures** : ramasser des récoltes mûres à la main.

Les quantités varient d'un jour à l'autre : quelques dizaines pour une vente ou une récolte, de 50 à 500 blocs pour
casser, selon le tirage. À chaque quête terminée, un message « Quête complétée » s'affiche et la récompense est versée
immédiatement. Quand **toutes** les quêtes du jour sont terminées, le bonus de complétion est versé à son tour.

### Le lien avec les SkyGrades

Le contenu de votre lot dépend de votre **SkyGrade**. Sans grade, aucune quête n'est disponible : chaque emplacement
du menu affiche « Quête verrouillée » et renvoie vers la commande `/sg` pour progresser ou acheter un grade. Plus
votre grade s'élève, plus votre lot du jour s'étoffe : si vous achetez un grade en cours de journée, les nouveaux
types de quêtes s'ajoutent immédiatement à votre lot, en conservant la progression de celles déjà commencées.

## Les récompenses

Le tirage dépend de votre grade du moment : un joueur plus gradé reçoit un lot plus riche le même jour. Chaque quête
complétée rapporte **1 clé de caisse de Niveau 1**. Quand toutes les quêtes du jour sont complétées, vous recevez en
plus un bonus de complétion, versé une seule fois par jour : **1 clé de caisse de Niveau 3**.

## Changer une quête : le reroll

Vous pouvez retirer une quête qui ne vous convient pas, contre paiement au choix :

- en **ReRolls** : le premier coûte 1 ReRoll, puis le prix augmente à chaque reroll payé ainsi dans le mois.
  Ce compteur est partagé avec les autres systèmes qui acceptent les ReRolls, et il repart à zéro le 1er de chaque
  mois ;
- en **Tokens** : un coût fixe de **20 Tokens**, qui n'augmente pas le compteur.

Consultez [la page SkyGrades](skygrades.md) pour savoir comment progresser de grade et débloquer plus de quêtes, et
[les premiers pas](../debuter/premiers-pas.md) si vous débutez sur le serveur.
