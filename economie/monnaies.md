---
title: Les monnaies
description: Les monnaies de One Dream, à quoi elles servent, comment les gagner et consulter vos soldes.
order: 1
keywords:
  - argent
  - solde
  - skycoins
  - tokens
  - balance
---

Sur One Dream, plusieurs monnaies coexistent : chaque système du serveur utilise la sienne. Cette page
présente chaque monnaie, son rôle et la façon de l'obtenir. Les valeurs affichées en jeu évoluent avec
les mises à jour : c'est le menu en jeu qui fait foi, pas le wiki.

## Les monnaies du serveur

### SkyCoins

Les **SkyCoins** (symbole `SC`) sont la monnaie principale du serveur. Vous les gagnez en vendant vos
ressources avec [/sell](vendre.md), au [SG Weekly](../progression/skygrades.md) et dans diverses
récompenses. Elles servent à acheter aux [boutiques du spawn](boutiques-et-livraisons.md), aux
[shops entre joueurs](shops-joueurs.md), à débloquer les [SkyGrades](../progression/skygrades.md) et à
agrandir votre [sac](sac.md). C'est aussi la seule monnaie que vous pouvez envoyer à un autre joueur
avec `/pay`.

### Tokens

Les **Tokens** s'achètent sur la [boutique du site](https://one-dream.fr). Ils servent en jeu à
acquérir les grades premium et à payer certains
[rerolls](../progression/quetes-journalieres.md). Ils ne s'échangent pas entre joueurs.

### ReRolls

Les **ReRolls** sont des jetons de relance : ils permettent de reroller une
[quête journalière](../progression/quetes-journalieres.md), un contrat de
[chasse](../chasse/ile-de-chasse.md) ou le [SG Weekly](../progression/skygrades.md). Vous partez avec
un premier ReRoll et certains [SkyGrades](../progression/skygrades.md) en offrent. Un reroll se paie au
choix en ReRolls ou en Tokens : si vous payez en ReRolls, le coût en ReRolls augmente à chaque reroll
payé de cette façon au cours du mois (le compteur repart à zéro le 1er du mois) ; si vous payez en
Tokens, le coût est fixe.

### IslandPoints

Les **IslandPoints** appartiennent à votre île, pas à votre inventaire. Vous en gagnez en accomplissant
des missions d'île, et vous les dépensez dans les **améliorations de l'île**, accessibles depuis le
panneau de contrôle. Un classement compare les îles entre elles.

### AfkPoints

Les **AfkPoints** se gagnent en restant dans les zones AFK, que vous rejoignez avec
`/afk`. Vous les dépensez dans la boutique AFK, ouverte avec `/afk shop`.

### Clés de caisse et fragments de clé

Les **caisses** du spawn s'ouvrent avec des clés : Clé Niveau 1 à Clé Niveau 5, plus des clés plus
rares. Vous obtenez des clés notamment avec les
[quêtes journalières](../progression/quetes-journalieres.md), le vote, les récompenses de temps de jeu réclamées dans
`/playtime` et certaines récompenses de [SkyGrades](../progression/skygrades.md).

Vous pouvez aussi **recycler** des clés en **fragments de clé**, puis **fabriquer** de nouvelles clés
avec ces fragments. Ces deux fonctions se débloquent avec un SkyGrade, via le menu des caisses
`/crates`.

## Consulter vos soldes

```text
/money
/balances
/baltop <devise>
```

- `/money` affiche votre solde de SkyCoins.
- `/balances` affiche tous vos soldes d'un coup.
- `/baltop` affiche le classement d'une devise, à indiquer dans la commande.

## Envoyer de l'argent à un joueur

Pour envoyer des SkyCoins à un autre joueur, utilisez :

```text
/pay <joueur> <montant>
```

> [!CAUTION]
> Un envoi est immédiat et irréversible : vérifiez bien le pseudo et le montant avant de valider.

Les autres monnaies ne sont pas transférables : les IslandPoints appartiennent à l'île, et les Tokens,
ReRolls, clés et fragments restent attachés à leur détenteur. Pour échanger des objets avec un joueur,
passez par les [shops entre joueurs](shops-joueurs.md).
