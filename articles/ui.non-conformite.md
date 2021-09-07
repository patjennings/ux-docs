---
title: Non conformités
layout: page
page_weight: 9
category: "ui"
---
* table of contents
{:toc}

## Liste ##

Au clic sur la section dans la navigation principale, on affiche la liste des offres en cours.

![ecran](assets/images/10.1-non-conformites.png)

Cet écran utilise les spécifications du [gabarit d'écran de liste](gabarits.listes.html)

Chaque ligne du tableau remonte, par défaut, ces informations
- La description `<p><strong/>`, accompagnée d'un badge affichant le type de la non-conformité (qualité, logistique). Chaque type prendra une des couleurs personnalisés
- La société concernée `<p class="text-muted">`
- L'article concerné `<p>`
- La date de RMA `<p class="text-muted">`
- La date d'action curative`<p class="text-muted">`
- La date d'action préventive `<p class="text-muted">`
- La dérogation `<p>`

> Comme stipulé dans la [section Listes](gabarits.listes.html), il n'est pas nécessaire de nommer chaque colonne.

#### Recherche contextuelle ####
La recherche contextuelle fonctionne sur le modèle défini dans les spécifications du [gabarit d'écran de liste](gabarits.listes.html#zone-de-recherchefiltrage-et-actions-principales)

Le menu déroulant du filtre pourra être composé des options suivantes (ces options pourront être revues ou affinées en fonction des besoins):

<div class="dropdown-menu" style="position: static;display: block; float: none; margin-bottom: 1rem;width:18rem;">
  <a class="dropdown-item" href="#">Qualité</a>
  <a class="dropdown-item" href="#">Logistique</a>
  <div class="dropdown-divider"></div>
  <a class="dropdown-item" href="#">Retail Material Agreement renseigné</a>
    <a class="dropdown-item" href="#">Action curative renseignée</a>
	  <a class="dropdown-item" href="#">Action préventive renseignée</a>
    <div class="dropdown-divider"></div>
  <a class="dropdown-item" href="#">Dérogation</a>
  <div class="dropdown-divider"></div>
  <a class="dropdown-item" href="#">Voir les non-conformités fermées</a>
</div>

À noter qu'en sélectionnant *Voir les non conformités fermées*, on appelle des résultats absents de la liste par défaut, les non conformités fermées n'étant par défaut pas disponibles.

## Détail ##

![ecran](assets/images/10.2-non-conformite.png)

#### En-tête ####

Dans la zone de l'offre, les informations de **budget** et de **délai** sont mises en avant.

> Plus de détails dans les [spécifications de l'en-tête](gabarits.details.html#en-tête)


#### Onglets ####

###### Coûts de non qualité ######

Reprise de liste, vue [tableau](comp.tableaux.html) affichant les [coûts de non qualité](ui.cnq.html) liés à l'occurence de non-conformité.

###### Notes ######

Voir Notes dans [Documents, messages, notes](comp.docs-messages-notes.html)

###### Documents ######

Voir Documents dans [Documents, messages, notes](comp.docs-messages-notes.html)
