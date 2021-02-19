---
title: Sprint 2
layout: page
page_weight: 6
category: "sprints"
---
* table of contents
{:toc}

## Fiche société ##

### Amélioration de l'onglet *Qualité* ###

#### Évaluations ####

Cet onglet est présenté en deux colonnes : 
- à gauche, les valeurs, renseignées régulièrement par l'utilisateur à cet endroit-même
- à droite, les graphes remontant un historique de certaines valeurs, réunies par le système à partir d'endroits divers

L'idée est de pouvoir effetuer la modification des "questions" (sur la gauche), en disposant, en regard, de données permettant d'effectuer cette modification

> la perspective d'offrir un sroll indépendant à chaque colonne peut être envisagée, afin de disposer de la bonne donnée en face de la question modifiée

Pour éditer une question, l'utilisateur clique sur l'icone `pen`, à côté de la valeur. Ensuite, on a deux options

###### Édition _inline_ (privilégiée) ######
La valeur en lecture est remplacée par un tryptique
  * champ avec valeur actuelle
  * bouton valider
  * bouton annuler
  
> Cette option permet de garder les graphes en lecture pendant l'édition de la note

###### Modale ######
L'autre option est d'afficher une modale à l'utilisateur, contenant le champ et la valeur à renseigner

#### Non-conformité ####
Les non conformités s'affichent sous forme de liste

Nouveauté : les archives fermées sont affichées avec un icone `archive`, et sont positionnées en bas de la liste.
Ainsi, les non-conformités ouvertes sont distinctes des non-conformités fermées. Le filtre de recherche permettra d'afficher seulement les NC fermées, si l'utilisateur le souhaite.

> Pour fermer un NC, on intégrera plutôt un bouton "Fermer" dans la modale d'édition, plutôt qu'une case à cocher.

Pour rouvrir une non conformités, on cliquera sur les points d'édition de celle-ci, puis sur `Ré-ouvrir`

--- 

L'icone et le texte sont colorées avec `secondary`, et les fonds avec `light`.

#### Conformité documentaire ####

Ici, rien à signaler : on affiche simplement une liste de conformités documentaires

#### Répercussion dans les paramètres généraux ####
un nouvel onglet apparait : Évaluation qualité des sociétés

Deux sous-onglets permettent d'jaouter ou de modifier :
- les raphiques : permet de contrôler les indicateurs, qui génèrent les graphiques (colonne de droite dans la fiche société, onglet Qualité)
- les notes (ou "questions") : contrôle les indicateurs (les notes) renseignés régulièrement par l'utilisateur (colonne de gauche dans la fiche société, onglet Qualité)

Dans chaque onglet, l'élément que l'on ajoute ou modifie sera appelé *indicateur*

> à la suppression, alerter l'utilsateur que des données sont présentes, et qu'elles seront effacés avec l'indicateur

### Amélioration de l'onglet *Achats* ###
synthèse;

L'onglet Achats affiche par défaut une synthèse. On affiche une carte, contenant chacune :
  * un titre
  * un sous-titre, si nécessaire, explicitant la donnée
  * un bloc étiquette/valeur, avec indice d'évolution (flèche montante ou descendante + couleur `primary` ou `danger`). La valeur set affichée avec `h4`
  * un bloc étiquette/valeur indiquant la valeur précédente. La valeur est affichée avec `h5`

> Une cersion alternative de ces cartes est également proposée, avec l'affichage d'un graphe d'évolution de la valeur


#### Offres et contrats ####

Ici, rien à signaler : on affiche simplement une liste d'offres et de contrats

#### Répercussion dans les paramètres généraux ####
un nouvel onglet apparait : Synthèse achat des sociétés
On peut ajouter ou modifier un indicateur

Dans chaque onglet, l'élément que l'on ajoute ou modifie sera appelé *indicateur*

> à la suppression, alerter l'utilsateur que des données sont présentes, et qu'elles seront effacés avec l'indicateur

## Données ERP ##

Ici, c'est une simple reprise de listes. On signale seulement la provenance de la donnée, par un flag `ERP` (icon `sync` de couleur `couleur`)

> On évitera de signaler plus que cela la provenance des données : la donnée s'insère dans la structure de Cobuy, son statut de donnée ERP signifiant simplement que la donnée est créée ailleurs.
> Notamment, éviter de créer des entrées comme "Données ERP" ou "import ERP" dans la navigation

## Catégories ##

La hiérarchie des catégories est plus marquée. Cet affichage passe par deux modifications
  * Augmentation de l'identation des items, en fonction de leur position dans la hiérarchie. On ajoute `20px` à chaque nouveau niveau
  * Un style par niveau
	* niveau 1 : font-weight: 700, couleur `dark`
	* niveau 2 : font-weight: 400, couleur `dark`
	* niveau 3 : font-weight: 400, couleur `#6c757d`
	* niveau 4 : font-weight: 400, font-style; italic, couleur `#6c757d`
	* niveau 5 : font-weight: 400, font-style; italic, couleur `light-grey`

## Informations fournisseur ##

La page des informations fournisseur se compose de la sorte :
  * les données générales (SIRET, type de société, etc.) sont présentées sous forme d'un tableau, qui affiche label/valeur (label en gras)
  * Ensuite, chaque partie suivante est introduite par un titre `h5`, et affiche des [cartes](https://getbootstrap.com/docs/5.0/components/card/#titles-text-and-links)
	* Les informations financières : chaque carte affiche le résultat de l'année et de l'année -1 résultat année avec évolution et couleur tendance :
		* Pour le résultat année : un bloc étiquette/valeur, avec indice d'évolution (flèche montante ou descendante + couleur `primary` ou `danger`). La valeur set affichée avec `h4`
		* Pour le résultat année-1 : un bloc étiquette/valeur indiquant la valeur précédente. La valeur est affichée avec `h5` (couleur par défaut `dark`)
	Les données de l'organigramme et les références sont affichées dans une carte simple (titre + description)

### Informations de mise à jour ###
Au début de la liste, on affiche les informations de mise à jour de la fiche.
  * Si la mise à jour est ok, on affiche simplement la date de la mise à jour (avec `text-muted`)
  * Si la mise à jour est trop ancienne, on affiche également la date de la mise à jour (avec `text-muted`). Mais, avant, on aura affiché un bandeau ― couleur `danger`― qui avertit de l'obsolescence des données actuellement affichées

### Modification ###

La modification des informations se fait au niveaiu de la fiche société. Les données de cet onglet `Informations` seront donc édités **avec** les données générales de la société (visibles dans l'en-tête).

#### Informations financières ####
La nouvelle année affiche un nouveau champ dans fenêtre modification

> déterminées par paramètres applis. On change valeur



> Voir modales pour principes édition interne modale

#### Organigramme ####

peut contenir personne seulement org, ou contact
un contact apparait auto dans org. On ne peut pas le supprimer d'ici (d'ou `trash` muted)
si on clique sur personne : affichage des champs personne
si on clique sur  contact : rappel du formulaire contact

Pour les références, le même principe sera appliqué (icone `pen` pour éditer, puis affichage par formulaire d'édition interne à la modale)

> Voir modales pour principes édition interne modale

## Modales ##

Toutes les fenêtres modales ont été revues. Certains champs ont été redisposés pour grouper l'information de façon logique, et faciliter la compréhension de l'utilisateur. Les mises à jour importantes sont les suivantes

- **Des séparateurs** (couleur `#DFDFDF`) sont utilisés pour répartir les groupes de champs de façon logique
- La `largeur de la modale` a été revue. Elle est désormais égale à la largeur du viewport, moins `64px` à gauche et `64px` à droite, et est disposée à `64px` du bord haut du `viewport`
  - À l'intérieur de cet espace, les éléments de formulaire sont établis sur une largeur de 680px.
  - Cela permet deux choses :
	- à gauche, la place est disponible pour un menu de navigation interne au formulaire (voir plus bas)
	- à droite, on laisse la place pour un formulaire *subsidiaire*, présenté dans un cadre _slidant_ (venant) de la droite (cf. prototype)
- **Les champs ont trois tailles** : *small* (`80px`), *medium* (`192px`) et *large* (`510px`), et correspondent à la taille de la valeur attendue
- **Les champs déroulants** sont [ceux de Bootstrap](https://getbootstrap.com/docs/5.0/components/dropdowns/#single-button)
- **Une navigation interne** est présente sur certains formulaires. Les liens sont des ancres, qui positionnent le contenu à la bonne position. Chaque item ne renvoie pas forcément à un groupe de champ surmonté d'un titre. On s'en servira pour les formulaires longs, comme :
  - Société
  - Ligne de contrat
  - Paramètres utilisateur
  
> Pour les messages : un utilisateur interne ou externe doit pouvoir être ajouté dans le même champ. Ainsi, on ajoutera un utilisateur interne en utilisant la recherche contextuelle. Si l'utilisateur entre une adresse mail inconnue du système et appuie sur `RET`, cette adresse est alors ajoutée en tant que destinataire. La différence entre destinataire interne et externe est matérialisée par la couleur du badge (_primary_ ou _light_).

Le comportement général, ainsi que l'affichage, est celui-ci proposé dans la section *Modales I*. La section *Modales II* reprend toutes les mises à jour de formulaires de création d'objets. La section *Modales III* évoque quant à elle le cas des formulaires longs.

## Ajout d'un objet hors de son contexte originel ##
Le formulaire secondaire, qu'on peut appeler au sein d'une modale, est affichée par dessus les éléments de formulaire courant. Il permet, notamment, d'éditer un objet autre que celui que l'on est en train d'éditer. Cela est particulièrement utile lorsqu'une action nécessite que l'utilisateur fasse référence à un autre objet du système, mais pas encore créé.

> L'objectif est double 
>  * pouvoir créer le lien avec cet autre objet
>  * favoriser l'action courante de l'utilisateur. Cela signifie qu'on proposera un minimum de champ à l'utilisateur lors de la création du nouvel objet. 

> Exemple : si l'utilisateur doit créer une société pendant la création d'un dossier, on ne proposera à l'utilisateur que les champs _Raison sociale_ et _type_ (fournisseur, client, etc.). Ainsi, le *flow* originel, de création de dossier, est favorisé. L'utilisateur pourra ensuite, éditer la société créée au cours de la création du dossier : mais cette action ne l'a pas détourné de son action première.

> On peut visualiser le comportement de cette fenêtre dans le prototype

## Cas particulier : l'ajout d'une demande d'achat ##
Dans le cas de l'ajout d'une demande d'achat, une requête, et une réponse, sont attendues par le système. C'est un cas particulier, qui a été résolu de la sort
Au bas de la première étape du formulaire, le bouton pour poursuivre l'action , n'est pas de fond `primary`, mais possède juste un contour (`class="outline"`).
Au clic sur ce bouton, un chargemetn s'effectue. La requête est lancée, et attend la réponse du serveur.
La réponse est arrivée, le formulaire est de nouveau affichée avec les nouveaux champs liés à cette réponse. L'utilisateur est positionné au niveau de ces nouveaux champs, un nouvel élément de menu est apparu dans la navigation interne. Au bas de la modale, la bouton `Continuer` est remplacé par le bouton `Valider`, de fond vert.


> La solution proposée rend aussi peu visible que possible cette contrainte pour l'utilisateur. Ici, elle n'est visible que par le bouton `Continuer` qui se substitue au bouton `Valider`, en bas à droite de la modale.

## Liens ##
- Prototype : <https://www.figma.com/proto/i5jtbAaIPN3Xq4u5Cg7qvv/%C3%89volutions-2021?node-id=183%3A30991&scaling=min-zoom>
