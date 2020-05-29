---
title: Cartes (offres)
layout: page
page_weight: 0
category: "composants"
---
* table of contents
{:toc}

Le modèle de carte présenté ici sert à afficher des lignes offres. Les offres sont présentes dans des objets de type [Offres](ui.offres.html) ou [demandes d'achat](ui.demandes-achat.md).

[ capture contexte ]

## Carte par défaut ##

La carte par défaut permet d'afficher le nom du fournisseur et l'id de la ligne d'offre en en-tête. Le menu d'options de l'en-tête permet d'embarquer des possibilités d'accès à des objets associés (fiche fournisseur, consultations, *e.g.*). On ajoutera dans ce menu toutes les actions annexes nécessaires. 

Par défaut, toutes les lignes d'offres sont affichées dans cet état. Si une ligne est sélectionnée par un chiffrage automatique dans le dossier qui la contient, on la trouvera sélectionnée à l'arrivée sur cet écran. Une ligne d'offres est désélectionnée dès qu'une autre est choisie.

<div class="card" style="width: 20rem;">
    <div class="card-header">
	Ingelec<span class="small text-muted" style="margin-left:0.5rem;">LOF-00128</span><i class="ico ico-medium" style="position: absolute; right: 6px; color: #5C6975;">dots_v</i>
    </div>
    <ul class="list-group list-group-flush">
	<li class="list-group-item"><span class="text-muted w-75 d-inline-block">Qté consultations</span>10</li>
	<li class="list-group-item"><span class="text-muted w-75 d-inline-block">Qté commande min.</span>500</li>
	<li class="list-group-item"><span class="text-muted w-75 d-inline-block">Qté conditionnement</span>1500</li>
    </ul>
    <div class="card-body">
	<div class="container">
	    <div class="row">
		<div class="col-sm pl-0 pr-0">
		    <p class="card-text text-muted" style="margin-bottom: 0.25rem;">PU H.T.</p>
		    <!-- h4 -->
		    <h3 style="margin-top: 0;font-size: 1.25rem; font-weight: 700;">0,265 €</h3>
		</div>
		<div class="col-sm pl-0 pr-0">
		    <p class="card-text text-muted" style="margin-bottom: 0.25rem;">Prix total H.T.</p>
		    <!-- h3 -->
		    <h3 style="margin-top: 0;font-size: 1.5rem; font-weight: 700; color:#5AB445;">132,00 €</h3>
		</div>
	    </div>
	    <div class="row pt-2"><a href="#" class="btn btn-outline-dark w-100">Sélectionner cette offre</a></div>
	</div>
    </div>
</div>

<hr/>

``` html
<div class="card">
    <div class="card-header">
	Ingelec
	<span class="small text-muted ml-1">LOF-00128</span>
	<i class="ico ico-medium position-absolute" style="right: 6px; color: var(--secondary)">dots_v</i>
    </div>
    <ul class="list-group list-group-flush">
	<li class="list-group-item">
	    <span class="text-muted w-75 d-inline-block">
		Qté consultations
	    </span>10
	</li>
	<li class="list-group-item">
	    <span class="text-muted w-75 d-inline-block">
		Qté commande min.
	    </span>
	    500
	</li>
	<li class="list-group-item">
	    <span class="text-muted w-75 d-inline-block">
		Qté conditionnement
	    </span>
	    1500
	</li>
    </ul>
    <div class="card-body">
	<div class="container">
	    <div class="row">
		<div class="col-sm pl-0 pr-0">
		    <p class="card-text text-muted mb-1">PU H.T.</p>
		    <h4>0,265 €</h4>
		</div>
		<div class="col-sm pl-0 pr-0">
		    <p class="card-text text-muted mb-1">Prix total H.T.</p>
		    <h3 class="text-primary">132,00 €</h3>
		</div>
	    </div>
	    <div class="row pt-2">
		<a href="#" class="btn btn-outline-dark w-100">
		    Sélectionner cette offre
		</a>
	    </div>
	</div>
    </div>
</div>
```

## Carte active ##

Dès qu'une ligne d'offre est sélectionnée, sa carte devient active et change de couleur. Le bouton de sélection est remplacé par un message indiquant l'état de la ligne d'offre, accompagné d'une icone `check`.

<div class="card text-white" style="width: 20rem; background-color:#5AB445;">
    <div class="card-header">
	Ingelec<span class="small" style="margin-left:0.5rem; opacity:0.5;">LOF-00128</span><i class="ico ico-medium" style="position: absolute; right: 6px;">dots_v</i>
    </div>
    <ul class="list-group list-group-flush">
	<li class="list-group-item" style="background-color: #5AB445;"><span class="w-75 d-inline-block" style="opacity: 0.75;">Qté consultations</span>10</li>
	<li class="list-group-item" style="background-color: #5AB445;"><span class="w-75 d-inline-block" style="opacity: 0.75;">Qté commande min.</span>500</li>
	<li class="list-group-item" style="background-color: #5AB445;"><span class="w-75 d-inline-block" style="opacity: 0.75;">Qté conditionnement</span>1500</li>
    </ul>
    <div class="card-body">
	<div class="container">
	    <div class="row">
		<div class="col-sm pl-0 pr-0">
		    <p class="card-text" style="margin-bottom: 0.25rem;">PU H.T.</p>
		    <!-- h4 -->
		    <h3 style="margin-top: 0;font-size: 1.25rem; font-weight: 700;">0,265 €</h3>
		</div>
		<div class="col-sm pl-0 pr-0">
		    <p class="card-text" style="margin-bottom: 0.25rem;">Prix total H.T.</p>
		    <!-- h3 -->
		    <h3 style="margin-top: 0;font-size: 1.5rem; font-weight: 700;">132,00 €</h3>
		</div>
	    </div>
	    <div class="row pt-2">
		<div class="col-sm">
		<p class="text-center mt-2 mb-0"><i class="ico ico-medium mr-1" style="color: #FFFFFF;">check</i>Offre sélectionnée</p>
		</div>
		</div>
	</div>
    </div>
</div>

<hr/>

``` html
<div class="card text-white bg-success">
    <div class="card-header">
	Ingelec
	<span class="small ml-1">LOF-00128</span>
	<i class="ico ico-medium position-absolute" style="right: 6px;">dots_v</i>
    </div>
    <ul class="list-group list-group-flush">
	<li class="list-group-item">
	    <span class="w-75 d-inline-block">
		Qté consultations
	    </span>
	    10
	</li>
	<li class="list-group-item">
	    <span class="w-75 d-inline-block">
		Qté commande min.
	    </span>
	    500
	</li>
	<li class="list-group-item">
	    <span class="w-75 d-inline-block">
		Qté conditionnement
	    </span>
	    1500
	</li>
    </ul>
    <div class="card-body">
	<div class="container">
	    <div class="row">
		<div class="col-sm pl-0 pr-0">
		    <p class="card-text mb-1">PU H.T.</p>
		    <h4>0,265 €</h4>
		</div>
		<div class="col-sm pl-0 pr-0">
		    <p class="card-text mb-1">Prix total H.T.</p>
		    <h3>132,00 €</h3>
		</div>
	    </div>
	    <div class="row pt-2">
		<p class="text-center mt-2 mb-0">
		    <i class="ico ico-medium mr-1" style="color: #FFFFFF;">
			check
		    </i>
		    Offre sélectionnée
		</p>
	    </div>
	</div>
    </div>
</div>
```
