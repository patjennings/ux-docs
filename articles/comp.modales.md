---
title: Fenêtres modales
layout: page
page_weight: 1
category: "composants"
---
* table of contents
{:toc}

Dès qu'un utilisateur doit entrer ou modifier des informations, il le fait dans une fenêtre modale. Le changement visuel traduit le changement de position de l'utilisateur. De cette façon, les actions d'écriture manuelles sont séparées des actions de lecture, ou des actions opérées par le système. 

Il permet en outre de poser un cadre cohérent à ces actions de saisie, et de mutualiser des composants (côté développement) et des façons de faire (côté utilisateur). 

Il permet, dans certains cas particuliers, d'afficher des données en lecture (historique de l'évaluation d'une société *in* [Société](ui.societes.html), accès à une vue statistique dans le [chiffrage d'un dossier](ui.dossiers.html) )

Formulaires : appel d'un objet présent dans le système 

{ illustration }


laisser toujours un espace de 64px en haut et en bas. Si les informations dépassent, on doit pouvoir scroller dans la zone de contenu (le header qui contient le titre et le footer qui contient les boutons d'action sont fixes). 


Les modales sont centrées verticalement et horizontalement dans l'écran.

forms :

priorité > label aligné horizontalement avec le champ
Si plus de place nécessaire, on place le champ sous le label

<https://getbootstrap.com/docs/4.5/components/modal/#vertically-centered>

erreur dans formulaire (warning)
    
<div style="background: #B2B5B8; padding: 1rem; width:48rem;">
	<div id="modal-intro" tabindex="-1" role="dialog">
	    <div class="modal-dialog">
		<div class="modal-content">
		    <div class="modal-header">
			<h5 class="modal-title mt-0">Modal title</h5>
			<button type="button" class="close" data-dismiss="modal" aria-label="Close">
			    <span aria-hidden="true">&times;</span>
			</button>
		    </div>
		    <div class="modal-body">
		    <div class="container">
				<div class="row">
					<div class="col-2 text-center"><i class="ico ico-large">caution</i></div>
					<div class="col-10">Êtes-vous sûr ?</div>
				</div>
			</div>
		    </div>
		    <div class="modal-footer">
		<button type="button" class="btn btn-outline-dark">Annuler</button>
			<button type="button" class="btn btn-primary">Modifier</button>
		    </div>
		</div>
	    </div>
	</div>
</div>

<hr/>

<div style="background: #B2B5B8; padding: 1rem; width:48rem;">
    <div id="modal-intro" tabindex="-1" role="dialog">
	<div class="modal-dialog modal-xl">
	    <div class="modal-content">
		<div class="modal-header">
		    <h5 class="modal-title mt-0">Modifier le dossier</h5>
		    <button type="button" class="close" data-dismiss="modal" aria-label="Close">
			<span aria-hidden="true">&times;</span>
		    </button>
		</div>
		<div class="modal-body">
		    <div class="container">
			<div class="form-group row mb-3">
			    <div class="col-3"><label for="input1">Nom</label></div>
			    <div class="col-9"><input type="text" class="form-control" id="input1" aria-describedby="emailHelp" value="Super ordinateur"></div>
			</div>
			<div class="form-group row mb-3">
			    <div class="col-3"><label for="input2">Client</label></div>
			    <div class="col-9">
				<div class="dropdown">
				    <button class="btn btn-light dropdown-toggle" type="button" id="dropdownMenuButton" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
					Client name
				    </button>
				    <div class="dropdown-menu" aria-labelledby="dropdownMenuButton">
					<a class="dropdown-item disabled" href="#">Ce composant est détaillé ci-dessous</a>
				    </div>
				</div>
			    </div>
			</div>
			<div class="form-group row mb-3">
			    <div class="col-3"><label for="input3">Budget</label><p class="text-muted small">Ce texte d'aide indique que le budget est indiqué en {devise du système}</p></div>
			    <div class="col-9"><input type="text" class="form-control" id="input3" aria-describedby="emailHelp" value="50000" style="width: 96px;"></div>
			</div>
		    </div>
		</div>
		<div class="modal-footer">
		    <button type="button" class="btn btn-outline-dark">Annuler</button>
		    <button type="button" class="btn btn-primary">Modifier</button>
		</div>
	    </div>
	</div>
    </div>
</div>

## composants spéciaux ##

#### ajout de société ####
dans consultations
#### ajout/recherche dropdown ####

