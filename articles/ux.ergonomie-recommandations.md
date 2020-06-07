---
title: Ergonomie
layout: page
page_weight: 0
category: "ux"
---
* table of contents
{:toc}

Cette page regroupe différentes recommandations ergonomiques, à appliquer sur l'ensemble des éléments de l'interface.

## Libellés ##

Les libellés tels que les titres, les en-têtes de tableaux et les libellés de champs sont des points d'informations très importants. Il convient de soigner leur présentation et leur sens.

Exemples

Au niveau de la présentation, **on tâchera d'utiliser exclusivement des bas-de-casse (minuscules) pour l'affichage des libellés et des textes de l'interface**. L'usage des capitales (majuscules) devrait être réservé à quelques cas exceptionnels, car leur lisibilité se réduit à mesure que la quantité de texte augmente à l'écran. 

> Dans une interface utilisateur, il n'y a en général aucune utilité à se servir de capitales, même pour surligner des informations importantes. On se servira plutôt des couleurs pour cet usage d'alerte.

On bannira également les tirets `-` et *underscores* `_` dans les libellés.

## Actions ##

Toutes les actions seront indiquées à l'infinitif : *Envoyer le message*, *lancer la consultation*

On tâche d'utiliser les articles pour les libellés d'action : l'interface utilisateur essaie de parler un langage humain, surtout dans les actions et les alertes. 
> On préféra utiliser le libellé "modifier l'évaluation" plutôt que "modifier évaluation"

Pour les actions *binaires* (checkboxes, principalement), on respectera le sens de l'action. Ainsi, une checkbox activé indiquera une possibilité supplémentaire pour l'utilisateur, et non une restriction.

> <div class="form-check"><input class="form-check-input" type="checkbox" value="" id="defaultCheck1" checked><label class="form-check-label" for="defaultCheck1">   Ne peut pas lancer de consultations</label></div>

Cette forme est contre-indiquée, dans la mesure où **l'activation de la checkbox induit une restriction** pour l'utilisateur (inversion des sens d'action). On préférera donc utiliser cette forme-ci :

> <div class="form-check"><input class="form-check-input" type="checkbox" value="" id="defaultCheck1"><label class="form-check-label" for="defaultCheck1">   Lancer des consultations</label></div>

Encore une fois, cette logique traversant l'interface, il sera plus facile pour un utilisateur de prendre rapidement la décision qui convient.

## Champs de formulaires ##

Les champs d'un formulaire de création ou de modification doivent être regroupés par 

On pourra aussi les séparer par des titres, et ainsi clarifier le découpage du formulaire pour l'utilisateur.

<hr/>

Il est important que les formulaires aient une taille qui correspondent à la donnée. C'une indication pour l'utilisateur, et cela facilitera son utilisation.

Ainsi, un champ trop large pour une donnée qui ne fera que 3 caractères max. est contre-indiqué. Exemple :
> <input class="form-control" type="text" value="500">

On préférera ainsi établir sa largeur de façon à l'adapter à la donnée accueillie
> <input class="form-control" type="text" value="500" style="width: 4rem;">




## Tableaux ##

###### Alignement ######

Dans les tableaux, les données chiffrées sont alignées sur leur droite. Voici un contre-exemple :

<div class="pt-2 pb-2 mb-3" style="text-align:left; border-top: 1px solid #e8e8e8; border-bottom: 1px solid #e8e8e8; width: 8rem;">
	<p>14 800 €</p>
	<p>7 500 €</p>
	<p>645 €</p>
	<p>101 425 €</p>
</div>

En alignant ces prix sur la droite, on constate que les devises, ainsi que les dizaines, centaines et milliers sont l'un au dessus de l'autre. La lecture en est facilitée.

<div class="pt-2 pb-2 mb-3" style="text-align:right; border-top: 1px solid #e8e8e8; border-bottom: 1px solid #e8e8e8; width: 8rem;">
	<p>14 800 €</p>
	<p>7 500 €</p>
	<p>645 €</p>
	<p>101 425 €</p>
</div>

###### Réduction de texte ######

Certains contextes d'affichage obligent des libellés à être réduits.

Pour les en-têtes de tableaux, on pourra appliquer ces règles de réduction de titre, pour gagner de l'espace :
  - *Tx* pour taux
  - *Qté* pour quantité
  
Ailleurs, si une donnée textuelle n'est pas adaptée à la place qui lui est laissée, on la tronquera. On affichera `…` à l'endroit de la troncature, et le reste de la donnée sera disponible au survol, comme illustré ici :

> <p data-toggle="tooltip" data-placement="top" title="Cette donnée est tronquée car elle est trop longue" style="width: 9rem;">Cette donnée est…</p>

<script>$(function () {
  $('[data-toggle="tooltip"]').tooltip()
})</script>

## Hiérarchie de l'information ##

Parfois, la quantité d'information présente à l'écran exige que l'on fasse un choix sur celle qui doit ressortir. Il n'est pas question ici de supprimer une information, mais d'échelonner la prise d'information de l'utilisateur.

Pour cela, nous avons plusieurs outils : **la graisse du caractère (gras, normal) et sa luminosité (noir ou gris clair).**

<hr/>
<span class="text-muted">Texte</span> `>` <span class="font-weight-bold text-muted">Texte</span> `>` <span>Texte</span> `>` <span class="font-weight-bold">Texte</span>
<p class="small text-muted">Styles disponibles pour hiérarchiser l'information.</p>
<hr/>


> La combinaison de ces éléments permet de nuancer un écran et de rendre digeste son appréhension par l'utilisateur.
> Pour cela, il est important, sur chaque écran, de hiérarchiser les informations (donnée cruciale, donnée principale, donnée secondaire, donnée contextuelle, méta-donnée).



## Dates ##
La plupart des dates sont indiquées au format `jj/mm/aaaa`. 
Lorsque cela est possible, une durée relative peut être employée : pour la durée jusqu'à expiration de la date d'échéance d'un dossier, par exemple.

De cette façon, la donnée est plus significative pour l'utilisateur ; la date au format `jj/mm/aaaa` pourra éventuellement être rappelée, au dessous, pour référence.

> <h5>Dans 24 jours</h5>
> <p class="small text-muted">Le 15/08/2020</p>
