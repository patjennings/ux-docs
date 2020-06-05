---
title: Documents, messages, notes
layout: page
page_weight: 10
category: "composants"
---
* table of contents
{:toc}

On applique à ces composants un traitement quasiment similaire. Ils seront disposés les uns au dessus des autres, dans les sous-section correspondantes des éléments auxquels ils appartiennent

## Documents ##
Les documents sont accessibles, dans chaque élément, via un onglet *Documents* <i class="ico ico-medium">file_o</i> disponible à droite de la barre de navigation interne aux objets.

La carte remonte les titres, identifiant, date d'ajout du document. Un badge mentionnera si ce document est acessible publiquement. L'utilisateur peut télécharger ce document sur sa machine et être informé du poids du document en question.
<div style="background: #F8F9FA; padding: 2rem; width:48rem;" class="mb-3">
<div class="card mb-2">
    <div class="card-body">
	<button type="button" class="close" style="position: absolute; right: 6px;">
		<i class="ico ico-medium">dots_v</i>
	</button>
	<h5 class="card-title mt-0 font-weight-bold">doc_addl_20200515.pdf <span class="small text-muted ml-2">DOC-256789</span><span class="badge badge-primary ml-3 small">Accès fournisseur</span></h5>
	<h6 class="card-subtitle mb-2 text-muted">Ajouté le 18 nov. 2019</h6>
	<div class="container">
	    <div class="row">
		<div class="col-7 pl-0">
		    <p class="card-text">Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam.</p>
		</div>
		<div class="col-5">
		    <button type="button" class="btn btn-light btn-sm"><i class="ico ico-medium mr-2 ">arrowdown</i>Télécharger le document</button><span class="small text-muted ml-2">28 Kb</span>
		</div>
	    </div>
	</div>
    </div>
</div>
</div>

Le menu (icone `dots_v`) affiche les options suivantes, qui permettent de modifier le document, ou bien de le supprimer :

<div class="dropdown-menu" style="position: static;display: block; float: none; margin-bottom: 1rem; width: 15rem;">
    <a class="dropdown-item" href="#">Modifier</a>
    <a class="dropdown-item" href="#">Supprimer</a>
</div>

## Messages ##
Les messages sont disponibles dans les consultations *e.g.* Les messages affichés sont ceux envoyés par des utilisateurs du système à des intervenants externes.
<div style="background: #F8F9FA; padding: 2rem; width:48rem;" class="mb-3">
<div class="card">
    <div class="card-body">
	<h5 class="card-title mt-0 font-weight-bold">Jean Lepetit</h5>
	<h6 class="card-subtitle mb-2 text-muted">Le 15 mai 2019</h6>
	<p class="card-text">Bonjour Jean. Pourriez-vous me fournir les plans de la pièce, car il me semble que…</p>
    </div>
</div></div>

## Notes ##
Les notes sont accessibles, dans chaque élément, via un onglet *Notes* <i class="ico ico-medium">notes</i> disponible à droite de la barre de navigation interne aux objets.

<div style="background: #F8F9FA; padding: 2rem; width:48rem;" class="mb-3">
<div class="card">
    <div class="card-body">
	<button type="button" class="close" style="position: absolute; right: 6px;">
		<i class="ico ico-medium">dots_v</i>
	</button>
	<h6 class="card-title mt-0 font-weight-bold">Information générale</h6>
	<p class="card-subtitle mb-2 text-muted">Par <strong>Jeanne Balafon</strong>, le 15 mai 2019</p>
	<p class="card-text">At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque corrupti quos dolores et quas molestias excepturi sint occaecati cupiditate non provident</p>
	<ul>
		<li>Et harum quidem rerum facilis est</li>
		<li>Et expedita distinctio. Nam libero tempore</li>
		<li>Cum soluta nobis est eligendi optio cumque nihil impedit quo minus id</li>
	</ul>
	<p>	<img src="assets/images/img-note.png" width="260" style="width: 260px;"/></p>

    </div>
</div>
</div>
Le menu (icone `dots_v`) affiche les options suivantes. La note peut-être envoyée à un intervenant extérieur.

<div class="dropdown-menu" style="position: static;display: block; float: none; margin-bottom: 1rem; width: 12rem;">
	<a class="dropdown-item" href="#">Envoyer la note</a>
<div class="dropdown-divider"></div>
    <a class="dropdown-item" href="#">Modifier</a>
    <a class="dropdown-item" href="#">Supprimer</a>
</div>
