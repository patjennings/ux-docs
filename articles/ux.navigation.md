---
title: Navigation
layout: page
page_weight: 0
category: "ux"
---
* table of contents
{:toc}

La navigation comporte 3 grands aspects : 
- la navigation principale
- la navigation interne aux objets
- les mécanismes qui permettent de lier les contenus les uns aux autres.

## Navigation principale (sidebar) ##

La navigation principale est l'endroit à partir duquel part toute action dans l'interface. Ce composant permet de naviguer entre les objets, d'effectuer une recherche globale dans le système, de paramétrer l'application de façon globale (pour tous les utilisateurs) ou seulement pour soi, et d'être notifié des changements intervenus entre deux connexions.

Ce composant est tout le temps présent à l'écran. 2 états (déplié, replié). Comportement pour chacun.

Recherche
accès
notifications (badges)
choix du périmètre
infos utilisateur (notifications + options)

#### Recherche globale ####

Voir [Recherche](link)


menu rétractable

rollover quand menu rétracté


## Navigation interne aux objets ##

Chaque objet est lié à plusieurs typologies de données (un dossier est lié à des demandes d'achat, des besoins). Ces données sont disponibles sous forme d'onglets.

{{ tabs }}

#### Navigation de troisième niveau ####

Il est parfois nécessaire d'avoir à subdiviser un contenu à ce niveau de profondeur. On utilisera alors pour cela des [*button groups* ](https://getbootstrap.com/docs/4.5/components/button-group/#basic-example).

{{ exemple }}

## Lier les élements de l'interface ##

Contexte de carte

Menus contextuels dans les tableaux

Clic sur une ligne de tableau
