# Wiki One Dream

Les sources du wiki de [One Dream](https://one-dream.fr/wiki), le serveur Minecraft skyblock francophone : guides,
mécaniques de jeu et commandes, écrits par le staff et la communauté.

Chaque fichier Markdown de ce repo devient une page du wiki. Une modification fusionnée sur `main` est en ligne quelques
minutes plus tard, sans autre manipulation.

> [!IMPORTANT]
> Avant de proposer votre première modification, lisez le [guide de contribution](.github/CONTRIBUTING.md) : il
> détaille le format des pages et les règles de rédaction.

## Contribuer en 5 minutes

**Corriger une faute ou une information** : ouvrez la page concernée sur GitHub, cliquez sur le crayon (*Edit this
file*), faites votre correction puis *Propose changes*. GitHub crée la proposition (pull request) pour vous.

**Écrire une nouvelle page** :

1. Forkez le repo, puis créez une branche (`ajout-page-metiers`, `correction-livraison`…).
2. Copiez le [modèle de page](.github/exemples/modele-page.md) dans le bon dossier et renommez-le (`mon-sujet.md`).
3. Remplissez le front matter (titre, description) et rédigez la page.
4. Ouvrez une pull request vers `main` et remplissez la liste de vérification.

Un membre du staff relit chaque proposition avant publication.

**Signaler un problème sans modifier le wiki** : ouvrez une [issue](../../issues/new/choose).

## Organisation du repo

Les pages et dossiers ci-dessous sont un exemple d'organisation :

```text
index.md                 Accueil du wiki (/wiki)
faq.md                   Une page à la racine (/wiki/faq)
iles/                    Une section de la sidebar
  _section.md            Titre, description et ordre de la section
  creer-son-ile.md       Une page de la section (/wiki/iles/creer-son-ile)
  images/                Les images des pages de la section
  avance/                Une sous-section
    _section.md
    configuration.md     (/wiki/iles/avance/configuration)
.github/
  CONTRIBUTING.md        Le guide de contribution complet
  exemples/              Modèles et page d'exemple (jamais publiés)
```

L'adresse d'une page vient de son chemin dans le repo : `iles/creer-son-ile.md` est publiée sur
`/wiki/iles/creer-son-ile`. Ce `README.md` et tout ce qui se trouve dans `.github/` ne sont jamais publiés.

## Exemples

Le dossier [`.github/exemples`](.github/exemples) contient des modèles prêts à copier et une page qui montre toutes les
mises en forme disponibles.

## Questions

Une question sur le wiki ou sur une contribution : posez-la sur le [Discord One Dream](https://discord.gg/RjYBUUKYFg).

## Licence

Le contenu du wiki est publié sous licence [Creative Commons Attribution - Partage dans les mêmes conditions 4.0
(CC BY-SA 4.0)](LICENSE) : vous pouvez le réutiliser et le modifier, à condition de citer le wiki One Dream et de
partager vos modifications sous la même licence. Les noms, logos et visuels One Dream restent la propriété du serveur.
