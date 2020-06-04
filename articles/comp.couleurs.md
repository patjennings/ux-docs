---
title: Couleurs
layout: page
page_weight: -9
category: "composants"
---
* table of contents
{:toc}

Les couleurs de l'interface sont divisées en deux grandes catégories : **les couleurs de base**, qui seront *overridées* dans le fichier `_variables.scss` de Bootstrap, et les **couleurs supplémentaires**, que l'on destinera à l'habillage de certains badges (types d'ocurrence, pour les dossiers e.g.) ou aux [graphiques](ui.graphiques.html)


## Couleurs de base ##

<div class="container colour-wheel" style="padding:0;">
    <div class="row">
	<div class="col-sm-6">
	    <div class="card">
		<div class="colour-slot" style="background-color: #5AB445"></div>
		<div class="card-body">
		    <p class="card-title font-weight-bold mb-0">primary</p>
			<p class="card-text text-muted mb-1">#5AB445</p>
		    <p class="card-text">Couleur identitaire de Cobuy, utilisée pour la mise en valeur des actions et des items de navigation.</p>

		</div>
	    </div>
	</div>
	<div class="col-sm-6">
	    <div class="card">
		<div class="colour-slot" style="background-color: #5C6975"></div>
		<div class="card-body">
		    <p class="card-title font-weight-bold mb-0">secondary</p>
			<p class="card-text text-muted mb-1">#5C6975</p>
		    <p class="card-text"></p>
		</div>
	    </div>
	</div>
    </div>
   <div class="row">
	<div class="col-sm-6">
	    <div class="card">
		<div class="colour-slot" style="background-color: #5AB445"></div>
		<div class="card-body">
		    <p class="card-title font-weight-bold mb-0">success</p>
			<p class="card-text text-muted mb-1">#5AB445</p>
		    <p class="card-text">Cette couleur est la même que <code>--primary</code>, elle informe sur un déroulement correct, une action réussie.</p>
		</div>
	    </div>
	</div>
	<div class="col-sm-6">
	    <div class="card">
		<div class="colour-slot" style="background-color: #D8113B"></div>
		<div class="card-body">
		    <p class="card-title font-weight-bold mb-0">danger</p>
						<p class="card-text text-muted mb-1">#D8113B</p>
		    <p class="card-text">On utilisera cette teinter pour des informations critiques, qui demandent une réaction de l'utilisateur.</p>
		</div>
	    </div>
	</div>
    </div><div class="row">
	<div class="col-sm-6">
	    <div class="card">
		<div class="colour-slot" style="background-color: #F6D944"></div>
		<div class="card-body">
		    <p class="card-title font-weight-bold mb-0">warning</p>
		    <p class="card-text text-muted mb-1">#F6D944</p>
			<p class="card-text">Pour des informations sensibles mais non critiques, on préférera utiliser cette teinte.</p>
		</div>
	    </div>
	</div>
	<div class="col-sm-6">
	    <div class="card">
		<div class="colour-slot" style="background-color: #04AEAE"></div>
		<div class="card-body">
		    <p class="card-title font-weight-bold mb-0">info</p>
		    <p class="card-text text-muted mb-1">#04AEAE</p>
			<p class="card-text"></p>
		</div>
	    </div>
	</div>
    </div><div class="row">
	<div class="col-sm-6">
	    <div class="card">
		<div class="colour-slot" style="background-color: #17181A"></div>
		<div class="card-body">
		    <p class="card-title font-weight-bold mb-0">dark</p>
		    <p class="card-text text-muted mb-1">#17181A</p>
<p class="card-text"></p>
		</div>
	    </div>
	</div>
	<div class="col-sm-6">
	    <div class="card">
		<div class="colour-slot" style="background-color: #F8F9FA"></div>
		<div class="card-body">
		    <p class="card-title font-weight-bold mb-0">light</p>
		    <p class="card-text text-muted mb-1">#F8F9FA</p>
<p class="card-text"></p>
		</div>
	    </div>
	</div>
    </div><div class="row">
	<div class="col-sm-6">
	    <div class="card">
		<div class="colour-slot" style="background-color: #B2B5B8"></div>
		<div class="card-body">
		    <p class="card-title font-weight-bold mb-0">light-grey</p>
		    <p class="card-text text-muted mb-1">#B2B5B8</p>
<p class="card-text"></p>
		</div>
	    </div>
	</div>
	<div class="col-sm-6">
	    <div class="card">
		<div class="colour-slot" style="background-color: #FFFFFF"></div>
		<div class="card-body">
		    <p class="card-title font-weight-bold mb-0">white</p>
		    <p class="card-text text-muted mb-1">#FFFFFF</p>
<p class="card-text"></p>
		</div>
	    </div>
	</div>
    </div>
</div>

``` css
--primary : #5AB445;
--secondary : #5C6975;
--success : #5AB445;
--danger : #D8113B;
--warning : #F6D944;
--info : #04AEAE;
--dark : #17181A;
--light : #F8F9FA;
--light-grey : #B2B5B8;
--white : #FFFFFF;
```


## Couleurs supplémentaires ##

<div class="container colour-wheel" style="padding:0;">
    <div class="row">
	<div class="col-sm-6">
	    <div class="card">
		<div class="colour-slot" style="background-color: #5AB696"></div>
		<div class="card-body">
		    <p class="card-title font-weight-bold mb-0">cobuy-1</p>
		    <p class="card-text text-muted mb-1">#5AB696</p>
<p class="card-text"></p>
		</div>
	    </div>
	</div>
	<div class="col-sm-6">
	    <div class="card">
		<div class="colour-slot" style="background-color: #FF9F40"></div>
		<div class="card-body">
		    <p class="card-title font-weight-bold mb-0">cobuy-2</p>
		    <p class="card-text text-muted mb-1">#FF9F40</p>
<p class="card-text"></p>
		</div>
	    </div>
	</div>
    </div>
   <div class="row">
	<div class="col-sm-6">
	    <div class="card">
		<div class="colour-slot" style="background-color: #36A2EB"></div>
		<div class="card-body">
		    <p class="card-title font-weight-bold mb-0">cobuy-3</p>
		    <p class="card-text text-muted mb-1">#36A2EB</p>
<p class="card-text"></p>
		</div>
	    </div>
	</div>
	<div class="col-sm-6">
	    <div class="card">
		<div class="colour-slot" style="background-color: #26999B"></div>
		<div class="card-body">
		    <p class="card-title font-weight-bold mb-0">cobuy-4</p>
		    <p class="card-text text-muted mb-1">#26999B</p>
<p class="card-text"></p>
		</div>
	    </div>
	</div>
    </div><div class="row">
	<div class="col-sm-6">
	    <div class="card">
		<div class="colour-slot" style="background-color: #FFCD56"></div>
		<div class="card-body">
		    <p class="card-title font-weight-bold mb-0">cobuy-5</p>
		    <p class="card-text text-muted mb-1">#FFCD56</p>
<p class="card-text"></p>
		</div>
	    </div>
	</div>
	<div class="col-sm-6">
	    <div class="card">
		<div class="colour-slot" style="background-color: #E1627D"></div>
		<div class="card-body">
		    <p class="card-title font-weight-bold mb-0">cobuy-6</p>
		    <p class="card-text text-muted mb-1">#E1627D</p>
<p class="card-text"></p>
		</div>
	    </div>
	</div>
    </div><div class="row">
	<div class="col-sm-6">
	    <div class="card">
		<div class="colour-slot" style="background-color: #212126"></div>
		<div class="card-body">
		    <p class="card-title font-weight-bold mb-0">cobuy-7</p>
		    <p class="card-text text-muted mb-1">#212126</p>
<p class="card-text"></p>
		</div>
	    </div>
	</div>
	<div class="col-sm-6">
	    <div class="card">
		<div class="colour-slot" style="background-color: #8D5F86"></div>
		<div class="card-body">
		    <p class="card-title font-weight-bold mb-0">cobuy-8</p>
		    <p class="card-text text-muted mb-1">#8D5F86</p>
<p class="card-text"></p>
		</div>
	    </div>
	</div>
	</div>
</div>

``` css
--cobuy-1 : #5AB696;
--cobuy-2 : #FF9F40;
--cobuy-3 : #36A2EB;
--cobuy-4 : #26999B;
--cobuy-5 : #FFCD56;
--cobuy-6 : #E1627D;
--cobuy-7 : #212126;
--cobuy-8 : #8D5F86;
```
