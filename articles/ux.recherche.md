---
title: Recherche
layout: page
page_weight: 0
category: "ux"
---
* table of contents
{:toc}

## Règles générales ##

La recherche ne devrait pas être case-sensitive, *i.e.* une recherche effectuée avec des minuscules uniquement devrait remonter les résultats comportant la même chaîne en majuscules ou mélangeant majuscules et minuscules.
La recherche devrait aussi remonter les résultats qui correspondent à une recherche effectuée sans accents.

> "energie" renvoie les résultats correspondants à "Énergie".

> "cable rj45" renvoie les résultats correspondants à "Câble RJ45"

On doit pouvoir également remonter des résultats en rentrant des informations qui ne sont pas visibles au premier abord. Exemple :

>Une liste de dossiers est affichée, mais leurs identifiants `DOS-00000` ne sont pas visibles. Si l'utilisateur une recherche avec un identifiant correspondant à un dossier, celui-ci est remonté comme résultat, malgré l'absence à l'écran de cet identifiant.

## Recherche globale ##

Pour les paramètres
utilisateurs et autres objet n'ayant pas de page dédiée vers laquelle renvoyer, on surlignera la ligne dans le contexte de liste par un jaune `--warning`.

Voir la [recherche globale](comp.recherche.html)

## Recherche contextuelle ##

La recherche contextuelle se trouve dans les listes (voir [gabarit listes](gabarit.listes.html)) et chaque sous-section de la page détails d'un objet (voir [gabarit détails](gabarit.details.html))

On peut retrouver, par le champ, tous les attributs de l'objet, même si celui-ci n'est pas affiché (e.g. id d'un dossier, cf. règles générales).

les options de filtre permettent d'affiner la recherche effectuée (via le champ recherche), ou la liste brute (par défaut, sans recherche effectuée). La liste de filtres propose plusieurs options, qui sont des _toggles_ par défaut désactivés. 

Si l'utilisateur active l'un d'entre eux, celui-ci s'affiche sous forme de carte dans le champ de recherche pour indiquer qu'un filtre est appliqué sur la liste. Ce filtre peut s'ajouter ou non à une recherche par chaîne de caractères dans ce même champ de recherche.

![recherche](assets/images/ux.recherche-1.png)

On peut finalement opérer un tri avec les colonnes. Cette fonctionnalité est développée dans le composant [tableau](comp.tableaux.html).

#### Filtres ####

Lorsqu'aucun filtre n'est activé, cela équivaut à une liste par défaut (tous les résultats). Elle se filtre dès qu'on sélectionne un ou plusieurs filtres. Aucun filtre activé ne donnne donc pas une liste vide mais une liste complète (non filtrée).
