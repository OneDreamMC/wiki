---
title: Créer son île
description: Créer votre île skyblock, choisir son type et découvrir les commandes de base pour la gérer au quotidien.
order: 2
keywords:
  - is
  - skyblock
  - création
  - île
  - commande
---

Sur One Dream, tout part de votre **île** : un petit territoire flottant, entouré de vide, que vous agrandissez et
aménagez à votre rythme. Cette page explique comment créer votre île, comment y revenir et où régler son
fonctionnement. La gestion des membres (invitations, rôles, permissions) est traitée dans une page dédiée.

## Créer votre île

1. Tapez la commande `/is create`.
2. Un menu s'ouvre avec les modèles d'île disponibles. Chaque modèle indique ses caractéristiques et son biome.
3. **Clic gauche** pour créer l'île, **clic droit** pour la prévisualiser avant de choisir.
4. L'île est générée en quelques secondes et vous y êtes téléporté automatiquement.

```text
/is create
```

> [!NOTE]
> Vous ne pouvez appartenir qu'à une seule île à la fois. Une île supprimée ne peut pas être récupérée :
> vérifiez votre choix avant de confirmer une suppression.

### Le menu d'île

La commande `/is menu` ouvre le **panneau de contrôle** de votre île. Vous y retrouvez, en un seul menu :

- **Réglages de l'Ile** : les paramètres de fonctionnement (drapeaux, réglages visibles par les visiteurs) ;
- **Permissions de l'Ile** : ce que chaque rôle peut faire sur l'île ;
- **Biome de l'Ile** : changer le biome ;
- **Banque de l'Ile** : déposer ou retirer de l'argent au coffre commun ;
- **Améliorations de l'Ile** : améliorer l'île avec vos IslandPoints ;
- **Classement de l'Ile** : voir votre position parmi les meilleures îles ;
- **Membres de l'Ile** : gérer les membres.

```text
/is menu
/is cp
```

## Les commandes de base

Toutes les commandes d'île commencent par `/is`. Les alias `/ile`, `/island` et `/islands` fonctionnent aussi.

```text
/is create        Créer une nouvelle île
/is               Se téléporter sur votre île
/is panel         Ouvrir le panneau de contrôle
/is top           Ouvrir le classement des îles
/is upgrades      Ouvrir le menu des améliorations
/is bank          Ouvrir la banque de l'île
/is biome         Changer le biome de l'île
/is nether        Changer le biome de l'île nether
/is permissions   Voir les permissions de chaque rôle
/is setteleport   Déplacer votre point de téléportation
```

> [!TIP]
> Retenez surtout `/is menu` : le panneau de contrôle donne accès aux menus les plus utilisés sans retenir les
> sous-commandes.

## Revenir sur votre île

La commande `/is` vous téléporte sur votre île, où que vous soyez sur le serveur.

Par défaut, vous arrivez au point de téléportation de l'île. Après avoir construit, vous pouvez le déplacer où vous
voulez avec `/is setteleport`, placé à l'endroit de votre choix.

```text
/is
/is setteleport
```

Pour aller sur l'île d'un autre joueur, utilisez `/is visit <joueur>` : vous arrivez dans sa zone visiteurs.
