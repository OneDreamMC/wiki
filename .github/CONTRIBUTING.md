# Contribuer au wiki One Dream

Merci de vouloir améliorer le wiki ! Ce guide explique comment proposer une modification, comment une page est
construite et quelles règles suivre pour qu'elle soit acceptée.

Sommaire :

1. [Comment proposer une modification](#1-comment-proposer-une-modification)
2. [Organisation des fichiers](#2-organisation-des-fichiers)
3. [Le front matter](#3-le-front-matter)
4. [Mise en forme](#4-mise-en-forme)
5. [Images](#5-images)
6. [Liens](#6-liens)
7. [Règles de rédaction](#7-règles-de-rédaction)
8. [Ce qui est refusé](#8-ce-qui-est-refusé)
9. [Avant d'ouvrir la pull request](#9-avant-douvrir-la-pull-request)
10. [Erreurs qui bloquent la publication](#10-erreurs-qui-bloquent-la-publication)

---

## 1. Comment proposer une modification

Le wiki se modifie uniquement par pull request (PR) : personne ne pousse directement sur `main`.

### Petite correction

Une faute, un chiffre faux, une phrase à reformuler : ouvrez la page sur GitHub, cliquez sur le crayon (*Edit this
file*), corrigez, puis cliquez sur *Propose changes*. GitHub forke le repo et prépare la PR pour vous.

### Nouvelle page ou grosse modification

1. **Annoncez-la d'abord** en ouvrant une issue « Proposer une page », pour vérifier que personne n'écrit déjà le même
   sujet et que le staff valide le contenu.
2. **Forkez** le repo, puis créez une branche au nom explicite : `ajout-page-metiers`, `correction-livraison`.
3. **Partez d'un modèle** du dossier [`exemples`](exemples) et respectez les règles de ce guide.
4. **Ouvrez la PR** vers `main` du repo `OneDreamMC/wiki` et cochez la liste de vérification.

Une PR = un sujet. Ne mélangez pas une nouvelle page et la correction d'une autre page sans rapport.

### Licence

En proposant une modification, vous acceptez qu'elle soit publiée sous la licence du wiki,
[CC BY-SA 4.0](../LICENSE). N'ajoutez que du texte et des images que vous avez écrits ou le droit de partager.

### Relecture et publication

Un membre du staff relit chaque PR : exactitude des informations, respect des règles, orthographe. Il peut demander
des changements ; répondez directement dans la PR. Une fois la PR fusionnée, le site se redéploie et la page est en
ligne en quelques minutes.

Si le wiki ne peut pas être construit (lien cassé, image manquante…), rien n'est publié et le site garde la version
précédente : le staff vous le signalera dans la PR.

---

## 2. Organisation des fichiers

### Pages et sections

- **Un fichier `.md` = une page.** Son adresse vient de son chemin : `iles/livraison.md` devient `/wiki/iles/livraison`.
- **Un dossier = une section** de la sidebar. Les sections peuvent s'imbriquer (`iles/avance/`), mais au-delà de deux
  niveaux la navigation devient pénible : évitez.
- **`index.md`** à la racine est l'accueil du wiki (`/wiki`). Il n'est autorisé qu'à la racine.
- **`_section.md`** dans un dossier donne le titre, la description et l'ordre de la section (voir
  [le front matter des sections](#front-matter-dune-section)). Sans lui, la section prend le nom du dossier.
- Une page **à la racine** (`faq.md`) s'affiche en haut de la sidebar, avec une icône.

Ne sont jamais publiés : `README.md` à la racine, tout fichier ou dossier dont le nom commence par un point
(`.github/`…), les dossiers qui ne contiennent aucun fichier `.md` et les brouillons.

### Noms de fichiers et de dossiers

En **kebab-case ASCII** : lettres minuscules sans accent, chiffres et tirets.

| Correct | Refusé |
| --- | --- |
| `creer-son-ile.md` | `Créer son île.md`, `creer_son_ile.md`, `CreerSonIle.md` |
| `economie/` | `Économie/`, `eco nomie/` |

Choisissez un nom court et stable : **renommer ou déplacer un fichier change son adresse** et casse les liens partagés
sur Discord ou ailleurs. Si c'est indispensable, signalez-le dans la PR.

### Ordre d'affichage

Dans la sidebar, les pages et sections sont triées par `order` (du plus petit au plus grand), puis par titre. Les
éléments sans `order` passent après ceux qui en ont un. Le même ordre donne les liens « Précédent » et « Suivant » en
bas des pages.

---

## 3. Le front matter

Chaque page commence par un bloc YAML entre deux lignes `---` : le **front matter**. Il n'apparaît pas dans la page,
il la décrit.

```yaml
---
title: Utiliser la livraison sur les îles
description: Envoyer des objets à un autre joueur sans quitter votre île, avec le système de livraison et ses frais.
order: 2
keywords:
  - colis
  - envoi
---
```

### Front matter d'une page

| Champ | Obligatoire | Rôle |
| --- | --- | --- |
| `title` | Oui | Titre de la page, affiché en haut, dans la sidebar et dans les résultats de recherche. |
| `description` | Oui | Une phrase qui résume la page. Affichée sous le titre et utilisée par Google et la recherche. |
| `order` | Non | Position dans la section (un nombre). |
| `keywords` | Non | Synonymes pour la recherche : des mots que les joueurs tapent mais que la page ne contient pas. |
| `icon` | Non | Icône d'une page à la racine (voir la liste ci-dessous). |
| `draft` | Non | `true` pour garder la page en brouillon : elle n'est pas publiée. |

Conseils :

- **`title`** : court et précis, sans point final, avec une majuscule au premier mot seulement
  (« Créer son île », pas « Créer Son Île »).
- **`description`** : une phrase complète de 80 à 160 caractères, avec un point final. Mettez-la entre guillemets si
  elle contient `:` ou `#` (`description: "Biomes, météo : le guide complet."`).
- **`keywords`** : 2 à 6 mots, au singulier, sans répéter le titre. Pour la page « Livraison » : `colis`, `envoi`,
  `boîte aux lettres`. La recherche tolère déjà les fautes de frappe, les accents et les pluriels.
- **`draft: true`** : pratique pour préparer une page en plusieurs fois. Aucune autre page ne peut faire de lien vers
  un brouillon.

### Icônes disponibles

Uniquement pour les pages à la racine. Sans `icon`, la page prend `file-text`.

`file-text`, `circle-help`, `message-circle`, `life-buoy`, `info`, `megaphone`, `scale`, `shield`, `users`, `map`,
`gift`, `star`, `coins`

Une icône hors de cette liste bloque la publication. Pour en ajouter une, demandez-le au staff.

### Front matter d'une section

Dans le fichier `_section.md` du dossier :

```yaml
---
title: Les îles
description: "Créer, gérer et faire grandir votre île : membres, livraisons et réglages."
order: 2
---
```

`title` est obligatoire, `description` et `order` sont facultatifs. La description s'affiche sur la carte de la section,
sur l'accueil du wiki. Le reste du fichier est ignoré.

---

## 4. Mise en forme

Le wiki utilise le Markdown de GitHub. La page [`exemples/page-complete.md`](exemples/page-complete.md) montre chaque
élément ci-dessous en situation.

### Intertitres

Commencez à `##`. Le titre de la page vient du front matter : n'écrivez pas de `#`.

```markdown
## Préparer un colis        ← apparaît dans « Sur cette page »
### Choisir le destinataire ← apparaît aussi, en retrait
#### Cas particulier        ← n'apparaît pas dans le sommaire
```

Chaque intertitre reçoit une ancre pour faire un lien direct (`/wiki/iles/livraison#preparer-un-colis`). Changer un
intertitre change son ancre : vérifiez qu'aucune page n'y fait de lien.

### Texte

| Markdown | Résultat |
| --- | --- |
| `**gras**` | **gras**, pour les noms de boutons, de menus et les mots importants |
| `*italique*` | *italique*, pour les termes étrangers et les titres d'œuvres |
| `` `code` `` | `code`, pour les commandes, les valeurs et les noms techniques |
| `~~barré~~` | ~~barré~~ |

### Listes

Listes à puces (`-`), numérotées (`1.`) pour les étapes à suivre dans l'ordre, et listes de cases (`- [ ]`, `- [x]`)
pour les checklists.

### Encadrés

Cinq types, à utiliser avec parcimonie (un ou deux par page) :

```markdown
> [!NOTE]
> Une information utile en complément.

> [!TIP]
> Une astuce pour aller plus vite.

> [!IMPORTANT]
> Une information à ne pas manquer.

> [!WARNING]
> Un risque de perdre du temps, des objets ou des SkyCoins.

> [!CAUTION]
> Une action irréversible ou sanctionnée.
```

Ils s'affichent avec les titres « Note », « Astuce », « Important », « Attention » et « Danger ».

### Tableaux

Pour comparer des valeurs (prix, limites, versions). Les tableaux trop larges défilent horizontalement sur mobile ;
au-delà de cinq colonnes, préférez une liste.

### Blocs de code

Toujours avec un langage. Pour les **commandes Minecraft**, utilisez `text` :

````markdown
```text
/is create
/is invite <joueur>
```
````

Autres langages courants : `yaml`, `json`, `properties`. Un langage inconnu s'affiche sans coloration.

### Éléments repliables et touches

Le HTML simple est accepté pour deux usages :

```html
<details>
<summary>Le message « Outdated client » s'affiche</summary>

Votre version de Minecraft est trop ancienne. Passez en 1.21.

</details>

Appuyez sur <kbd>F3</kbd> + <kbd>H</kbd>.
```

Laissez une ligne vide après `<summary>` pour que le Markdown à l'intérieur soit interprété.

### Notes de bas de page

`Le prix est fixe[^1].` puis, en bas de la page, `[^1]: Hors événements spéciaux.` À réserver aux précisions
secondaires.

---

## 5. Images

### Où les ranger

Dans un dossier `images/` à côté de la page, et lien en chemin relatif :

```markdown
![Le menu de livraison avec ses quatre boutons](images/menu-livraison.png "Le menu de livraison, ouvert avec /livraison")
```

- Le texte entre crochets est le **texte alternatif** : obligatoire. Il décrit l'image pour les lecteurs d'écran et
  s'affiche si l'image ne charge pas.
- Le texte entre guillemets, facultatif, devient la **légende** sous l'image. Il ne fonctionne que si l'image est seule
  dans son paragraphe.
- Les joueurs peuvent cliquer sur une image pour l'agrandir et zoomer : une capture lisible en grand suffit.

### Règles

- **Format** : PNG pour les captures d'interface, WebP ou JPEG pour les paysages et les constructions.
- **Taille** : 1600 px de large au maximum et 500 Ko au maximum. Recadrez sur ce qui compte.
- **Nom** : en kebab-case, comme les pages (`menu-livraison.png`).
- **Pas d'images externes** (liens vers Imgur, Discord…) : elles finissent par disparaître. Ajoutez le fichier au repo.
- **Captures propres** : interface en français, pas d'informations personnelles (pseudos d'autres joueurs sans leur
  accord, coordonnées de bases, conversations privées).
- **Droits** : uniquement vos propres captures, ou des images que vous avez le droit de partager.

---

## 6. Liens

### Vers une autre page du wiki

Avec le **chemin relatif du fichier `.md`**, depuis la page où vous écrivez :

```markdown
Consultez [la livraison](livraison.md).                    ← même dossier
Consultez [les règles](../communaute/regles-du-serveur.md). ← autre section
Consultez [la FAQ](../faq.md#mot-de-passe).                  ← avec une ancre
```

N'écrivez jamais d'adresse en dur (`/wiki/iles/livraison` ou `https://…/wiki/…`) : le chemin relatif est vérifié à
chaque publication, une adresse en dur non. Un lien vers une page ou une ancre qui n'existe pas bloque la publication.

### Vers un autre site

En adresse complète : `[le Discord](https://discord.gg/RjYBUUKYFg)`. Ces liens s'ouvrent dans un nouvel onglet. Limitez-les
aux sites officiels (Minecraft, Discord One Dream, outils reconnus).

---

## 7. Règles de rédaction

### Le ton

- **Vouvoiement** partout : « Ouvrez le menu », « vous recevez ».
- **Phrases courtes**, une idée par phrase. Un joueur doit trouver sa réponse en survolant la page.
- **Impératif pour les étapes** : « Cliquez sur **Envoyer** », pas « Il faut cliquer » ni « On clique ».
- **Neutre et factuel** : pas d'humour qui vieillit mal, pas de « super », « génial », pas d'emojis.

### La structure d'une page

1. Un premier paragraphe qui dit **à quoi sert la page** et à qui elle s'adresse.
2. Des sections `##` dans l'ordre où le joueur en a besoin : d'abord comprendre, puis faire, puis les cas particuliers.
3. Si utile, une section « En cas de problème » à la fin.

Une page traite **un seul sujet**. Au-delà d'environ 1500 mots, découpez-la en plusieurs pages.

### Les termes du jeu

- Écrivez les commandes en code avec leur barre oblique : `/is create`. Indiquez les paramètres entre chevrons :
  `/livraison <joueur>`.
- Écrivez les noms de boutons et de menus en gras, avec la majuscule du jeu : **Colis simple**.
- La monnaie principale du serveur s'appelle les **SkyCoins** (« 50 SkyCoins »). Les autres monnaies gardent
  leur nom du jeu : **Tokens**, **IslandPoints**, **AfkPoints**…
- Gardez le nom exact des objets Minecraft en français (« table d'enchantement », pas « enchanting table »).

### Typographie

- Espace avant `:`, `;`, `!` et `?`, comme en français courant.
- Guillemets français « » pour citer un message du jeu : le message « Boîte aux lettres pleine ».
- Nombres : `1 000`, `2,5`. Unités et heures : `4 h`, `14 jours`, `10 minutes`.
- Pas de majuscules pour insister, utilisez le **gras**.

### L'exactitude

- **Vérifiez en jeu** chaque commande, prix et limite avant de les écrire.
- **N'inventez rien** : si vous n'êtes pas sûr d'un chiffre, dites-le dans la PR, le staff complétera.
- **Pas de date précise** pour une fonctionnalité à venir : ce n'est pas au wiki de l'annoncer.

---

## 8. Ce qui est refusé

- Les **exploits, duplications et contournements** de règles, même pour les « signaler » : envoyez-les au staff sur
  Discord, en privé.
- Les **informations non publiques** : fonctionnalités pas encore annoncées, chiffres internes, contenu du staff.
- Les **données personnelles** : pseudos de joueurs ciblés, captures de conversations, coordonnées.
- La **publicité** : autres serveurs, boutiques, chaînes ou serveurs Discord personnels.
- Le **contenu copié** d'un autre wiki ou site sans autorisation.
- Les **pages d'opinion** (« les meilleures îles », « les pires métiers ») : le wiki explique, il ne classe pas.
- Le **HTML** en dehors de `<details>`, `<summary>` et `<kbd>` : pas de scripts, de styles, d'iframes ni de vidéos
  intégrées.

---

## 9. Avant d'ouvrir la pull request

Relisez votre page avec l'aperçu de GitHub (onglet *Preview* de l'éditeur, ou la page du fichier sur votre branche) :
les encadrés, tableaux et images s'y affichent presque comme sur le wiki.

- [ ] Les noms de fichiers et de dossiers sont en kebab-case ASCII.
- [ ] Le front matter contient `title` et `description`.
- [ ] La page commence par `##`, pas de `#`.
- [ ] Les liens internes pointent vers des fichiers `.md` qui existent, en chemin relatif.
- [ ] Chaque image est dans le repo, fait moins de 500 Ko et a un texte alternatif.
- [ ] Les commandes, prix et limites ont été vérifiés en jeu.
- [ ] Le texte est relu : vouvoiement, orthographe, phrases courtes.

---

## 10. Erreurs qui bloquent la publication

À chaque fusion, le wiki est construit. Si une de ces erreurs est détectée, **rien n'est publié** et le site garde la
version précédente, jusqu'à la correction.

| Message | Cause | Correction |
| --- | --- | --- |
| `front matter manquant` | Le fichier ne commence pas par un bloc `---`. | Ajoutez le front matter en toute première ligne. |
| `front matter invalide` | YAML mal formé, ou champ du mauvais type. | Vérifiez l'indentation ; mettez la description entre guillemets si elle contient `:`. |
| `titre manquant` | Pas de `title`. | Ajoutez-le. |
| `description manquante` | Pas de `description` sur une page. | Ajoutez une phrase de résumé. |
| `icône "…" inconnue` | `icon` hors de la liste. | Choisissez une icône de la [liste](#icônes-disponibles). |
| `nom de fichier invalide` | Majuscule, accent, espace ou `_` dans le nom. | Renommez en kebab-case. |
| `nom de dossier invalide` | Idem pour un dossier. | Renommez en kebab-case. |
| `"index.md" n'est autorisé qu'à la racine` | Un `index.md` dans un dossier. | Renommez-le, la section utilise `_section.md`. |
| `URL en double` | Un fichier `iles.md` à côté d'un dossier `iles/`, par exemple. | Renommez l'un des deux. |
| `lien cassé` | Lien vers un fichier, un brouillon ou une ancre qui n'existe pas. | Corrigez le chemin ou l'ancre. |
| `lien relatif … seuls les liens vers un fichier .md` | Lien relatif vers autre chose qu'une page. | Liez le fichier `.md`, ou utilisez une adresse complète. |
| `image manquante` | Le fichier image n'est pas au chemin indiqué. | Ajoutez l'image ou corrigez le chemin (attention aux majuscules). |
