---
title: Non conformités
layout: page
page_weight: 3
category: "ui"
---
* table of contents
{:toc}

Intro

## Liste ##

Au clic sur la section dans la navigation principale, on affiche la liste des offres en cours.

[capture liste]

Cet écran utilise les spécifications du [gabarit d'écran de liste](gabarits.listes.html)

Chaque ligne du tableau remonte, par défaut, ces informations
- un badge affichant le (…). Couleur du badge `--couleur`
- (…) `<p><strong/>`
- (…) `<p class="text-muted">`
- (…) `<p>`

Un badge doté d'un fond `--warning` et contenant un `!` sera affiché sur les dossiers présentant un retard qui doit être remonté à l'utilisateur.

> Comme stipulé dans la [section Listes](gabarits.listes.html), il n'est pas nécessaire de nommer chaque colonne.

#### Recherche contextuelle ####
La recherche contextuelle fonctionne sur le modèle défini dans les spécifications du [gabarit d'écran de liste](gabarits.listes.html#zone-de-recherchefiltrage-et-actions-principales)

Le menu déroulant du filtre pourra être composé des options suivantes (ces options pourront être revus ou affinés en fonction des besoins):

<div class="dropdown-menu" style="position: static;display: block; float: none; margin-bottom: 1rem;">
  <a class="dropdown-item" href="#">Affaire</a>
  <a class="dropdown-item" href="#">Appel d'offres</a>
  <a class="dropdown-item" href="#">Devis</a>
  <a class="dropdown-item" href="#">Projet</a>
  <div class="dropdown-divider"></div>
  <a class="dropdown-item" href="#">Dossiers en retard</a>
    <div class="dropdown-divider"></div>
  <a class="dropdown-item" href="#">Mes dossiers</a>
</div>

## Détail ##

[capture détail]

#### En-tête ####

Dans la zone de l'offre, les informations de **budget** et de **délai** sont mises en avant.

> Plus de détails dans les [spécifications de l'en-tête](gabarits.details#en-tête.html)


#### Onglets ####

###### Coûts de non qualité ######

Reprise de liste, vue tableau (liens vers coût de non qualité, section détail)

###### Messages ######

lien vers docs-messages-notes

###### Documents ######

lien vers docs-messages-notes
