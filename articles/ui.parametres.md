---
title: Paramètres
layout: page
page_weight: 11
category: "ui"
---
Cette section regroupe les paramètres du système. Les utilisateurs peuvent y avoir plus ou moins accès, en fonction de leur rôle et de leurs *privilèges*.

## Sous-navigation ##

Composant list-group, sur 3 colonnes

<div class="list-group" style="width: 14rem;">
  <button type="button" class="list-group-item list-group-item-action active">
    Sites
  </button>
  <button type="button" class="list-group-item list-group-item-action">Unités</button>
  <button type="button" class="list-group-item list-group-item-action">Devises</button>
  <button type="button" class="list-group-item list-group-item-action">Utilisateurs</button>
  <button type="button" class="list-group-item list-group-item-action">Incoterms</button>
  <button type="button" class="list-group-item list-group-item-action">Importation</button>
  <button type="button" class="list-group-item list-group-item-action">Portail</button>
  <button type="button" class="list-group-item list-group-item-action">ERP</button>
</div>

<hr/>

``` html
<div class="list-group">
  <button type="button" class="list-group-item list-group-item-action active">Sites</button>
  <button type="button" class="list-group-item list-group-item-action">Unités</button>
  <button type="button" class="list-group-item list-group-item-action">Devises</button>
  <button type="button" class="list-group-item list-group-item-action">Utilisateurs</button>
  <button type="button" class="list-group-item list-group-item-action">Incoterms</button>
  <button type="button" class="list-group-item list-group-item-action">Importation</button>
  <button type="button" class="list-group-item list-group-item-action">Portail</button>
  <button type="button" class="list-group-item list-group-item-action">ERP</button>
</div>
```

## Contenu ##
Contrôlé par la sous-navigation, l'affichage du contenu est affiché sur 13 colonnes, dans un tableau qui liste chacune des entrées de la sous-section de paramètres

[ capture ]

Chaque sous-section est introduite par un titre `<h3>` et un texte qui explique le rôle de cette section de paramètres `<p class="text-muted"></p>`

Ensuite, on aligne à droite un bouton de création, qui permet d'ajouter un élément dans la sous-section. L'affichage s'effetue donc via un tableau ; chaque ligne se voit doté d'un menu (icone `dots_v`), qui permet, *a minima*, d'éditer ou de supprimer l'occurence. 

<div class="dropdown-menu" style="position: static;display: block; float: none; margin-bottom: 1rem; width: 8rem;">
  <a class="dropdown-item" href="#">Modifier</a>
  <a class="dropdown-item" href="#">Supprimer</a>
</div>

## Configuration d'un utilisateur ##

La configuration d'un utilisateur intègre des paramètres particuliers. La fenêtre modale est divisée en deux :
- une partie de gauche qui permet d'intervenir sur les informations principales de l'utilisateur. 
  - ses noms, prénoms, adresse mail
  - le site de l'utilisateur. Cela influera sur les données de site que l'utilisateur pourra consulter (voir le menu *périmètre* de la barre de gauche)
  - les catégories sur lesquels il intervient (ces paramètres auront un rôle à jouer lors de lancement automatique de consultations *e.g.*)
- une partie de droite qui permet de gérer les privilèges de l'utilisateur. Le fonctionnement de cette partie [est développé dans la partie UX](ux.multi.html)

![ecran](assets/images/13.3-parametres.png)
