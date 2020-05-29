---
title: Listes
layout: page
page_weight: 0
category: "gabarits"
---
* table of contents
{:toc}

Ce gabarit d'écran est celui qui sera utilisé pour l'affichage des listes d'objets.

## Zoning ##

[ zoning, nommage des zones ]

## Barre de recherche et d'actions ##

Toute liste est chapeauté par une barre permettant de rechercher dans les données de la liste, de filtrer celle-ci, de contrôler son affichage et d'y ajouter un nouvele élément.

#### Recherche et filtrage ####

Sur la gauche de cette zone vient se placer la recherche contextuelle à la liste affichée. Elle se compose d'un champ de recherche et d'un dropdown qui permet de filtrer les contenus. Ce dropdown contient des options de filtrage qui sont adaptées à la section affichée. On veillera à garder organisé ce menu déroulant en séparant les options par type.

Si aucune des options du menu déroulant n'est cochée, la liste remonte tous les résultats. Dès qu'une option est activé (icone `check`), la liste n'affiche que les résultats correspondants à ce critère. On peut additionner les options en activant plusieurs d'entre elles. Le dropdown ne se referme pas entre deux sélections d'option. C'est un clic à l'extérieur du menu déroulant qui vient fermer celui-ci.

> Par exemple, cette configuration filtre les résultats en ne remontant que les dossiers en retard de type *Affaire* et *Appel d'offres*.
> <div class="dropdown-menu" style="position: static;display: block; float: none; margin-bottom: 1rem;">
>   <a class="dropdown-item" href="#"><i class="ico ico-medium" style="color: #5AB445;">check</i>&nbsp;&nbsp;Affaire</a>
>   <a class="dropdown-item" href="#"><i class="ico ico-medium" style="color: #5AB445;">check</i>&nbsp;&nbsp;Appel d'offres</a>
>   <a class="dropdown-item" href="#">Devis</a>
>   <a class="dropdown-item" href="#">Projet</a>
>   <div class="dropdown-divider"></div>
>   <a class="dropdown-item" href="#"><i class="ico ico-medium" style="color: #5AB445;">check</i>&nbsp;&nbsp;Dossiers en retard</a>
>     <div class="dropdown-divider"></div>
>   <a class="dropdown-item" href="#">Mes dossiers</a>
> </div>

#### Gestion de l'affichage ####

Immédiatement à sa droite, vient se placer un toggle, qui permet de basculer entre une vision *liste* et une vision *carte* (icones `bullet_list` et `grid`).

[ illustration (mise en valeur du composant )]

Plus de détails, voir [recherche](ux.recherche.html)

#### Ajout d'un élément ####
Dans cette ligne, on ajoutera, aligné sur la droite, [les boutons](https://getbootstrap.com/docs/4.5/components/buttons/) d'ajout de contenu. Dès qu'une section offre la possibilité d'ajouter un élément, c'est ici que l'on placera le ou les boutons. Chaque bouton sera accompagné, sur sa gauche, d'une icone `plus`.

C'est une action importante, aussi ce bouton est il coloré avec `--primary`, pour favoriser sa visibilité.

[ exemple ]

## Alerte ##

Lorsqu'une alerte est remontée à l'utilisateur, [un composant alert](https://getbootstrap.com/docs/4.5/components/alerts/#link-color)e est utilisé. Il contient le motif de l'alerte, et propose une action qui permet de filtrer la liste et de ne remonter que les résultats correspondant au message. On choisira entre les couleurs `--warning` (jaune, criticité moyenne et faible) et `--alert` (rouge, information critique) pour déterminer la criticité de l'alerte.

## Liste ##

La liste de résultats peut s'afficher de deux façons : par l'intermédiaire d'une vue *tableau* ou par l'intermédiaire d'une vue *grille*

#### Vue tableau ####

[ illustration (mise en valeur du composant )]

C'est la vue par défaut. Elle est basée sur les principes de la section

Les tableaux s'affichent sur un fond blanc `--white`

Il n'est pas nécessaire de nommer chaque colonne : on ne garde que les en-têtes qui créeraient trop de confusion s'ils étaient retirés. Typiquement, l'en-tête de la colonne "identifiants" n'apporte pas de réelle information, mais n'empêche pas de comprendre que la donnée affichée est un identifiant.

Plus de détails sur la vue [tableaux](comp.tableaux.html), et notamment sur le comportement de tri au clic sur les en-têtes de colonnes.

> le critère de tri par défaut de la liste est la date de création de l'élément (descendant, du plus récent au plus ancien).

#### Vue grille ####

[ capture  ]

La vue *grille* est constituée [de cartes avec titre et sous-titre](https://getbootstrap.com/docs/4.5/components/card/#titles-text-and-links). Chaque carte est établie sur 4 colonnes de largeur (à ajuster en fonction des informations à remonter dans chacune).

[ capture élément seul ]

Cette vue offre la possibilité de hiérarchiser les données de chaque élément. Dans le cas d'un dossier, on peut notamment ajouter, dans le corps de la carte, un budget ou une quantité d'offres reçues de la sorte :
- le libellé `<p class="text-muted">`
- le valeur `<h5>`

On peut également afficher, en bas de carte, une information lié à l'échéance du dossier `<p class="text-muted">`, accompagnée d'une icone `clock`

#### Zone d'état (nombre de résultats, actualisé par le filtrage) ####

Cette zone permet d'afficher le nombre de résultats remontés pour la configuration actuelle de la liste. Par défaut, il comptabilise l'ensemble des résultats, qu'ils soient ou pas dans le *viewport*.
À partir du moment où la liste est filtrée (application d'un filtre à partir du menu déroulant ou entrée d'une chaine de caractères dans le champ de recherche), ce chiffre est actualisé.

Cette zone occupe une hauteur de `48px`, de fond `--white` et surmonté d'un filet de 1px de couleur `#DFDFDF`. Le nombre de résultat est affiché via `<p class="small text-muted">`.

## Défilement ##

La liste remonte en premier lieu la quantité de résultats affichable dans le viewport. Les résultats suivants de la liste sont appelés et affichés au scroll de l'utilisateur. La conjonction des informations de la barre d'état et de la taille de la scrollbar permettent à l'utilisateur de se repérer et d'avoir une idée du volume et de sa position dans la masse de résultats.
> La mise en place d'un système de pagination classique génère un nombre de clics trop importants. Sur des listes où le volume de données est peu important (-100 résultats), un scroll est plus efficace. Sur des listes où le volume de données est plus important (500+ résultats), le passage par la recherche est plus efficace pour l'utilisateur.

## Reprise des listes ##

Les listes peuvent être reprises dans certains onglets d'autres types d'objets. 
Qu'y retrouve-t-on ?
Où amène le clic ?
