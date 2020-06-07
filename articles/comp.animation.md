---
title: Animations
layout: page
page_weight: 4
category: "composants"
---
* table of contents
{:toc}

L'animation des éléments permet d'apporter à l'utilisateur une sensation de fluidité. Mais, plus important, il permet d'attirer son regard sur certaines zones de l'interface.

#### Survol des éléments ####

Cette règle devrait, *a minima*, être appliquée à **tout** élément interactif de l'interface.

```scss
item{ 
    // règles de l'élément
}
item:hover{
    transition : 0.15s all ease-in-out;
}
```

#### *Toast* de notification ####

L'animation de cet élément est géré [ par Bootstrap<i class="ico">external_link</i>](https://getbootstrap.com/docs/4.5/components/toasts/#placement)

#### Horloge de notifications de l'utilisateur ####
Lors de sa connexion, une [notification apparait à l'utilisateur](comp.notifications.html#zone-utilisateur), près de son nom, et l'avertit d'événements survenus depuis sa dernière connexion (rechargez peut-être la page pour voir l'animation, ici).

<style type="text/css">
.bell-container{
	padding: 1rem;
	background: #17181A;
	margin-bottom: 1rem;
	border-radius: 4px;
}
	.bell{
		animation-name: bellNotification;
		animation-duration: 2s;
		animation-iteration-count: 2;
		animation-timing-function: ease-in-out;
		color: white;
}
.badge-bell{
	position: relative;
	left: -15px;
	top: -11px;
	animation-name: badgeNotification;
	animation-duration: 1s;
	animation-timing-function: ease-in-out;
}
	@keyframes bellNotification{
		0% { transform : rotate(0deg); }
		5% { transform : rotate(25deg); }
		15% { transform : rotate(-25deg); }
		25% { transform : rotate(25deg); }
		35% { transform : rotate(-25deg); }
		45% { transform : rotate(25deg); }
		55% { transform : rotate(-25deg); }
		70% { transform : rotate(0deg); }
		100% { transform: rotate(0deg); }
	}
	@keyframes badgeNotification{
		0% { transform : scale(0); }
		50% { transform : scale(0); }
		90% { transform : scale(1.5); }
		100% { transform : scale(1); }
	}
</style>

<div class="bell-container">
	<i class="ico ico-large bell">bell</i>
	<span class="badge badge-pill badge-info badge-bell">3</span>
</div>



```scss
.bell{
    animation-name: bell-animation;
    animation-duration: 2s;
    animation-iteration-count: 2;
    animation-timing-function: ease-in-out;
}
.badge{
    animation-name: badge-animation;
    animation-duration: 1s;
    animation-timing-function: ease-in-out;
}

@keyframes bell-animation{
    0% { transform : rotate(0deg); }
    5% { transform : rotate(25deg); }
    15% { transform : rotate(-25deg); }
    25% { transform : rotate(25deg); }
    35% { transform : rotate(-25deg); }
    45% { transform : rotate(25deg); }
    55% { transform : rotate(-25deg); }
    70% { transform : rotate(0deg); }
    100% { transform: rotate(0deg); }
}
@keyframes badge-animation{
    0% { transform : scale(0); }
    50% { transform : scale(0); }
    90% { transform : scale(1.333); }
    100% { transform : scale(1); }
}
```

#### Animations de l'icone *statistiques* dans chiffrage ####

Dans un dossier, lorsque l'utilisateur vient [d'effectuer un chiffrage](ui.dossiers.html), les statistiques liées à celui-ci sont disponibles

<style type="text/css">
.graph-container{
	padding: 1rem;
	background: #17181A;
	margin-bottom: 1rem;
	border-radius: 4px;
	color: white;
}
	.graph{
		animation-name: graphAvailable;
		animation-duration: 1s;
		animation-iteration-count: 4;
}
	@keyframes graphAvailable{
		0% { transform : scale(1); opacity: 1; }
		25% {opacity: 0.25;}
		50% { transform : scale(1.5); opacity: 1; }
		75% {opacity: 0.25;}
		100% { transform : scale(1); opacity: 1; }
	}
</style>

<div class="graph-container">
	<i class="ico ico-large graph">graph</i>
</div>

```scss
.element{
    animation-name: graph-available;
    animation-duration: 1s;
    animation-iteration-count: 4;
}
@keyframes graph-available{
    0% { transform : scale(1); opacity: 1; }
    25% {opacity: 0.25;}
    50% { transform : scale(1.5); opacity: 1; }
    75% {opacity: 0.25;}
    100% { transform : scale(1); opacity: 1; }
}
```

> Cette animation nécessitera peut-être de petites modifications en contexte, pour trouver le bon équilibre visuel.
