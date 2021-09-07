---
title: Graphiques
layout: page
page_weight: 3
category: "composants"
---
* table of contents
{:toc}

Les graphiques sont affichés avec [ChartJS<i class="ico">external_link</i>](https://www.chartjs.org/). Les couleurs utilisées dans les graphiques seront exclusivement celles détaillées dans la partie *couleurs supplémentaires* de la section [Couleurs](ui.couleurs.html), cela afin de ne pas générer de bruit avec le nuancier de l'interface, qui a une valeur d'information ― action primaire, alerte, avertissement, etc.

Il est recommandé de n'afficher que les éléments nécessaires. Ainsi, on évitera toute légende qui surcharge inutilement un graphique.

<div class="chart-container" style="position: relative; width:640px; margin: 3rem 0;">
    <canvas id="example-doughnut"></canvas>
</div>

<script>
	 var ctx = document.getElementById('example-doughnut').getContext('2d');
	 var myChart = new Chart(ctx, {
	     type: 'doughnut',
	     data: {
		 labels: ['data 1', 'data 2', 'data 3', 'data 4', 'data 5', 'data 6'],
		 datasets: [{
		     label: '# of Votes',
		     data: [14, 18, 10, 14, 28, 16],
		     backgroundColor: [
			 '#5AB696',
			 '#FF9F40',
			 '#36A2EB',
			 '#26999B',
			 '#FFCD56',
			 '#E1627D'
		     ],
		     borderWidth: 0
		 }]
	     },
	     options: {
			 responsive: true,
			 maintainAspectRatio: true,
			 legend: {
				 position: 'right'
			 }
	     }
	 });
</script>

> Un [plugin pour ChartJS <i class="ico">external_link</i><i class="ico">external_link</i>](https://emn178.github.io/chartjs-plugin-labels/samples/demo/) permet d'afficher les données **sur** le graphique ― en plus du tooltip

## Exemples d'utilisation ##


#### Pie menu ####

C'est le graphique idéal pour représenter une répartition de quantités.

<div class="chart-container" style="position: relative; width:640px; margin: 3rem 0;">
    <canvas id="example-pie"></canvas>
</div>

<script>
	 var ctx = document.getElementById('example-pie').getContext('2d');
	 var myChart = new Chart(ctx, {
	     type: 'pie',
	     data: {
		 labels: ['data 1', 'data 2'],
		 datasets: [{
		     label: '# of Votes',
		     data: [36, 64],
		     backgroundColor: [
			 '#36A2EB',
			 '#E1627D'
		     ],
		     borderWidth: 0
		 }]
	     },
	     options: {
			 responsive: true,
			 maintainAspectRatio: true,
			 legend: {
				 position: 'right'
			 }
	     }
	 });
</script>

``` js
var ctx = document.getElementById('example-pie').getContext('2d');
var myChart = new Chart(ctx, {
    type: 'pie',
    data: {
	labels: ['data 1', 'data 2'],
	datasets: [{
	    data: [36, 64],
	    backgroundColor: [
		'#36A2EB',
		'#E1627D'
	    ],
	    borderWidth: 0
	}]
    },
    options: {
	responsive: true,
	maintainAspectRatio: true,
	legend: {
	    position: 'right'
	}
    }
});
```


#### Pie menu, variante *doughnut* ####

La variante `doughnut` sera intéressante pour représenter une répartition entre plus de 7 éléments, qui augmente légèrement la lisibilité des parties les plus petites

<div class="chart-container" style="position: relative; width:640px; margin: 3rem 0;">
    <canvas id="example-doughnut-2"></canvas>
</div>

<script>
	 var ctx = document.getElementById('example-doughnut-2').getContext('2d');
	 var myChart = new Chart(ctx, {
	     type: 'doughnut',
	     data: {
		 labels: ['data 1', 'data 2', 'data 3', 'data 4', 'data 5', 'data 6', 'data 7', 'data 8', 'data 9', 'data 10', 'data 11', 'data 12'],
		 datasets: [{
		     label: '# of Votes',
		     data: [8,8,1,10,8,12,8,6,4,8,15,8],
		     backgroundColor: [
			 '#5AB696',
			 '#FF9F40',
			 '#36A2EB',
			 '#26999B',
			 '#FFCD56',
			 '#E1627D',
			 '#212126',
			 '#8D5F86',
			 '#5AB696',
			 '#FF9F40',
			 '#36A2EB',
			 '#26999B'
		     ],
		     borderWidth: 0,
			 
		 }]
	     },
	     options: {
			 responsive: true,
			 maintainAspectRatio: true,
			 legend: {
				 position: 'right'
			 }
	     }
	 });
</script>

``` js
var ctx = document.getElementById('example-doughnut').getContext('2d');
var myChart = new Chart(ctx, {
    type: 'doughnut',
    data: {
	labels: [
		'data 1', 
		'data 2', 
		'data 3', 
		'data 4', 
		'data 5', 
		'data 6', 
		'data 7', 
		'data 8', 
		'data 9', 
		'data 10', 
		'data 11', 
		'data 12'
	],
	datasets: [{
	    label: '# of Votes',
	    data: [8,8,1,10,8,12,8,6,4,8,15,8],
	    backgroundColor: [
		'#5AB696',
		'#FF9F40',
		'#36A2EB',
		'#26999B',
		'#FFCD56',
		'#E1627D',
		'#212126',
		'#8D5F86',
		'#5AB696',
		'#FF9F40',
		'#36A2EB',
		'#26999B'
	    ],
	    borderWidth: 0,
	    
	}]
    },
    options: {
	responsive: true,
	maintainAspectRatio: true,
	legend: {
	    position: 'right'
	}
    }
});
```

> Si les couleurs du nuancier viennent à manquer, on pourra reprendre deux fois la même couleur ; l'important étant bien sûr que les deux parts ne viennent pas à se toucher !

#### Barres horizontales ####
Pour évaluer des quantités en plusieurs dimensions, les barres horizontales sont intéressantes. Attention, toutefois, à garder l'information lisible. Une des dimensions ne pourra dépasser 3 éléments.

<div class="chart-container" style="position: relative; margin: 3rem 0;">
    <canvas id="example-bars"></canvas>
</div>

<script>
	 var ctx = document.getElementById('example-bars').getContext('2d');
	 var myChart = new Chart(ctx, {
	     type: 'horizontalBar',
	     data: {
		 labels: [
		     "bois",
		     "carte electronique",
		     "chimie",
		     "circuit imprime ",
		     "consommable",
		     "câblage filaire ",
		     "electromecanique",
		     "frais generaux",
		     "interim",
		     "matiere premiere",
		     "plasturgie",
		     "prestation",
		     "quincaillerie",
		     "tolerie",
		     "travaux",
		     "tuyauterie",
		     "usinage",
		     "verre"
		 ],
		 datasets: [{
		     label: 'Data 1',
		     data: [0,4,3,4,3,6,3,5,1,4,3,3,4,3,2,4,3,3],
		     backgroundColor: '#26999B',
		     borderWidth: 0
		 },
         {
        	label: 'Data 2',
        	data: [0,6,3,4,3,6,6,4,7,3,3,3,4,3,4,5,3,3],
        	backgroundColor: '#FFCD56',
        	borderWidth: 0
         }]
	     },
	     options: {
		 legend: {
		     display: true,
		     position: 'right'
		 },
		 scales: {
		     yAxes: [{
			 ticks: {
			     beginAtZero: true
			 }
		     }]
		 }
	     }

	 });

	</script>
	
	

``` js
var ctx = document.getElementById('example-bars').getContext('2d');
var myChart = new Chart(ctx, {
    type: 'horizontalBar',
    data: {
	labels: [
	    "bois",
	    "carte electronique",
	    "chimie",
	    "circuit imprime ",
	    "consommable",
	    "câblage filaire ",
	    "electromecanique",
	    "frais generaux",
	    "interim",
	    "matiere premiere",
	    "plasturgie",
	    "prestation",
	    "quincaillerie",
	    "tolerie",
	    "travaux",
	    "tuyauterie",
	    "usinage",
	    "verre"
	],
	datasets: [{
	    label: 'Data 1',
	    data: [0,4,3,4,3,6,3,5,1,4,3,3,4,3,2,4,3,3],
	    backgroundColor: '#26999B',
	    borderWidth: 0
	},
		   {
        	       label: 'Data 2',
        	       data: [0,6,3,4,3,6,6,4,7,3,3,3,4,3,4,5,3,3],
        	       backgroundColor: '#FFCD56',
        	       borderWidth: 0
		   }]
    },
    options: {
	legend: {
	    display: true,
	    position: 'right'
	},
	scales: {
	    yAxes: [{
		ticks: {
		    beginAtZero: true
		}
	    }]
	}
    }

});
```

#### Ligne ####
Une ligne est utile pour représenter une donnée qui évolue dans le temps. On pourra afficher plusieurs données dans un même graphique, mais on veillera à ne pas en mettre plus de 3.

Ici, l'échelle est importante pour donner un repère quantitatif, mais il n'est pas nécessaire pour visualiser l'évolution : on n'affiche donc, en ordonnées, que des *steps* de 5.

<div class="chart-container" style="position: relative; margin: 3rem 0;">
    <canvas id="example-line"></canvas>
</div>

<script>
	 var ctx = document.getElementById('example-line').getContext('2d');
	 var myChart = new Chart(ctx, {
	     type: 'line',
	     data: {
		 labels: [
		     "Jan.",
		     "Fev.",
		     "Mar.",
		     "Avr.",
		     "Mai",
		     "Jun.",
		     "Jui.",
		     "Aou.",
		     "Sep.",
		     "Oct.",
		     "Nov.",
		     "Déc."
		 ],
		 datasets: [{
		     label: 'Data 1',		     
		     data: [0,2,1,0,3,0,1,2,0,2,3,1],
		     backgroundColor: '#36A2EB33',
		     borderColor: '#36A2EB',
		     borderWidth: 2
		 }]
	     },
	     options: {
		 legend: {
		     display: true  
		 },
		 scales: {
		     yAxes: [{
			 ticks: {
			     min: 0,
			     max: 10,
			     stepSize: 5,
			     beginAtZero: true
			 }
		     }]
		 }
	     }

	 });

	</script>
	
``` js
var ctx = document.getElementById('example-line').getContext('2d');
var myChart = new Chart(ctx, {
    type: 'line',
    data: {
	labels: [
	    "Jan.",
	    "Fev.",
	    "Mar.",
	    "Avr.",
	    "Mai",
	    "Jun.",
	    "Jui.",
	    "Aou.",
	    "Sep.",
	    "Oct.",
	    "Nov.",
	    "Déc."
	],
	datasets: [{
	    label: 'Data 1',		     
	    data: [0,2,1,0,3,0,1,2,0,2,3,1],
	    backgroundColor: '#36A2EB33',
	    borderColor: '#36A2EB',
	    borderWidth: 2
	}]
    },
    options: {
	legend: {
	    display: true  
	},
	scales: {
	    yAxes: [{
		ticks: {
		    min: 0,
		    max: 10,
		    stepSize: 5,
		    beginAtZero: true
		}
	    }]
	}
    }
});
```

## Liens ##
- Documentation de ChartJS : <https://www.chartjs.org/docs/latest/charts/doughnut.html>
