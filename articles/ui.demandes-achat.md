---
title: Demandes d'achat
layout: page
page_weight: 4
category: "ui"
---
* table of contents
{:toc}

## Liste ##

Au clic sur la section dans la navigation principale, on affiche la liste des offres en cours.

![ecran](assets/images/6.1-demandes.png)

Cet écran utilise les spécifications du [gabarit d'écran de liste](gabarits.listes.html)

Chaque ligne du tableau remonte, par défaut, ces informations
- Le nom de l'article `<p><strong/>`
- Le dossier affilié `<p class="text-muted"><strong/>` et `<p class="text-muted">`
- Les quantités de l'offre `<p>`
- La date de création de l'offre `<p class="text-muted">`

> Comme stipulé dans la [section Listes](gabarits.listes.html), il n'est pas nécessaire de nommer chaque colonne.

#### Recherche contextuelle ####
La recherche contextuelle fonctionne sur le modèle défini dans les spécifications du [gabarit d'écran de liste](gabarits.listes.html#zone-de-recherchefiltrage-et-actions-principales)

Le menu déroulant du filtre pourra être composé des options suivantes (ces options pourront être revus ou affinés en fonction des besoins):

<div class="dropdown-menu" style="position: static;display: block; float: none; margin-bottom: 1rem;width:18rem;">
  <a class="dropdown-item" href="#">Contient une note</a>
</div>

## Détail ##

![ecran](assets/images/6.2-demande-offres.png)

#### En-tête ####

Un rappel du dossier parent est affiché en haut de l'en-tête.

> Plus de détails dans les [spécifications de l'en-tête](gabarits.details#en-tête.html)

#### Onglets ####

###### Lignes d'offres ######

Reprise de liste (Voir [listes](gabarits.listes.html)). Affichage des lignes liés à l'occurence de demande d'achat, sous forme de cartes (voir [cartes](comp.cartes-offres.html))

###### Consultations ######

Reprise de liste, vue [tableau](comp.tableaux.html) affichant les [consultations](ui.consultations.html) liés à l'occurence de demande d'achat.

###### Notes ######

Voir Notes dans [Documents, messages, notes](comp.docs-messages-notes.html)
