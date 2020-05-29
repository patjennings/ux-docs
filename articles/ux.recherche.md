---
title: Recherche
layout: page
page_weight: 0
category: "ux"
---
* table of contents
{:toc}

ne devrait pas être case-sensitive. Une recherche effectuée avec des minuscules uniquement devrait remonter les résultats comportant la même chaîne en majuscules ou mélangeant majuscules et minuscules.
La recherche devrait aussi remonter les résultats qui correspondent à une recherche effectuée sans accents (e.g. "energie" renvoie les résultats correspondants à "énergie").

## Recherche globale ##

Pour les paramètres
utilisateurs et autres objet n'ayant pas de page dédiée vers laquelle renvoyer, on surlignera la ligne dans le contexte de liste par un jaune {définir}

Voir composants recherche globale

## Recherche contextuelle ##

La recherche contextuelle se trouve dans les listes (voir gabarit) et chaque sous-section de la page détails d'un objet (voir gabarit)

On peut retrouver, par le champ, tous les attributs de l'objet, même si celui-ci n'est pas affiché (e.g. id d'un dossier)

les options de filtre permettent d'affiner la recherche (ou la liste brute). La liste de filtre propose plusieurs options, qui sont des _toggles_ par défaut désactivés. Si on active l'un d'entre eux, celui-ci s'affiche sous forme de carte dans le champ de recherche pour indiquer qu'un filtre est appliqué sur la liste. Ce filtre petu s'ajouter ou non à une recherche par chaîne de caractères dans ce même champ de recherche.

[exemple illustré de recherche + filtres]

On peut finalement opérer un tri avec les colonnes. Cette fonctionnalité est développée dans le composant [tableau](comp.tableaux.html).

aucun filtre activé équivaut à une liste par défaut (tous les résultats). Elle se filtre dès qu'on sélectionne un ou plusieurs filtres. Aucun filtre activé ne donnne donc pas une liste vide mais une liste complète (non filtrée).


où la retrouve-t-on ?
