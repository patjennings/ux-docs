---
title: Sprint 1
layout: page
page_weight: 6
category: "sprints"
---
* table of contents
{:toc}

## Informations ##
On peut consulter les informations via deux types d'affichage :
- une vue *liste*, affichée seulement dans une modale
- une vue *expand*, associée à une ligne de tableau

Les informations, qui retracent l'historique des actions effectuées sur un objet, est disponible au niveau du menu "points", sous l'entrée *Informations*. Dans une modale, on affiche alors :
- un rappel du nom principal de l'objet, du propriétaire et du site
- une liste, **triée par ordre antéchronologique**. chaque item comprend une icone _pen_. 
  - Le nom de l'utilisateur ayant effecté l'action est en gras. 
  - Les informations de temps sont en `small` et `text-muted`

La première entrée est matérialisée par un fond jaune `#FFFBE8`

--- 

Les informations peuvent également être consultées pour une ligne de tableau. Ainsi, au niveau du menu "points" d'une ligne, un accès *Informations* est également disponible. Ici, un conteneur sur fond gris `#F8F9FA` affiche l'historique des interventions sur un élémente de tableau. Chaque ligne est stylé avec une classe `text-muted`, et précédée d'un icone _pen_. Sur la première entrée, les caractères et l'icone sont de couleur `5AB445`.

--- 
Sur les écrans suivants, on voit également la façon dont une ligne peut embarquer d'autres lignes de tableau. On retrouve ce cas de figure dans un chiffrage, ou un article peut comprendre plusieurs offres. Les sous-éléments sont prévus pour être masqués par défaut. Au clic sur l'icone _plus_, à gauche, on dévoile les sous-éléments, affichés sur une ligne de fond `#F8F9FA`. Si l'utilisateur choisit d'afficher les informations sur ce type d'élément complexe, le conteneur s'affichera sous les deux lignes de sous-éléments. Si les sous-éléments sont masqués, le comportement est identique à une ligne de tableau simple, comme vu plus haut.

## Révisions ##
La création d'une révision s'effectue par un clic sur l'icone _pen_ située à côté de la donnée de révision, dans l'en-tête. 

On affiche alors une modale : celle-ci contient un seul champ, qui permet d'ajouter une précision à la révision en cours de création. La lettre de la révision, l'utilisateur, la date et l'heure de la création de la révision sont des données en lecture, et ne s'affichent donc pas dans un champ. Elles introduisent la modale, séparées du champ _description_ par un séparateur.

--- 

Pour des éléments qui possèdent une information de révision, la modale d'information propose deux types de données : les informations de mise à jour, et les révisions (qui sont des mises à jour, mais assez spécifiques pour qu'on les affiche à part). Un [button-group](https://getbootstrap.com/docs/5.0/components/button-group/) permet de passer de passer de l'un à l'autre. Les données affichées par défaut sont les mises à jour.

## Pièces-jointes ##
Les pièces-jointes auront un comportement légèrement différent du comportement actuel. Plutôt que d'avoir des pièces-jointes qui embarquent plusieurs liens ou fichiers, on privilégiera l'approche suivante

> 1 fichier (ou 1 lien) = 1 ligne de pièce-jointe

On naviguera ainsi plus facilement dans les pièces-jointes, et la suppression et la mise à jour seront simplifiées.

Au niveau de la modale d'ajout, l'utilisateur doit d'avbord choisir quel type de pièce-jointe il souhaite ajouter (lien ou fichier). Les champs sous le séparateur qui suit ce menu dépliant seront alors rafraichis en fonction de son choix.

Dans le cas où l'utilisateur uploade plusieurs fichiers dans le module de téléversement ― par exemple deux, comme sur les écrans ― deux lignes de pièces-jointes seront créées, qui partageront la description donnée au moment de l'ajout.

Les lignes de pièce seront ensuite les mêmes, à l'exception du bouton d'action : Une pièce-jointe de type *fichier* aura un bouton gris (_light_), avec une icone `arrowdown`, qui permet de télécharger le fichier en local. Une pièce-jointe de type _lien_ aura elle une bouton vert (_primary_),  avec une icone `arrowright`, qui permet d'accéder à la page web liée.

## Homologations ##
Le cycle des validations reprend le schéma synthétisé ici, et repris de la version existante. Chaque état bénéficie d'une pastille spécifique, affichée sur la ligne : 
- de couleur _light_, avec une icone `clock` pour le statut _en attente_
- de couleur _warning_, `check` pour le statut_validé R&D_ (ou toute autre étape de **validation intermédiaire**)
- de couleur _primary_, `check-double` pour le statut _validé qualité_ (ou toute étape de **validation finale**)
- de couleur _danger_, `close` pour le statu *rejeté*

L'affichage du suivi des validations reprend l'affichage *expand* des informations, comme vu plus haut, et reprend, pour chaque statut,  les icones vues ci-avant.

## En-têtes ##

#### Métadonnées ####
L'ajout principal de cet élément est l'apparition des informations d'utilisateur propriétaire, de site et de provenance ERP. 
Ces informations s'affichent de façon discrète, mais sont saillantes dans le parcours visuel.
- L'information de provenance ERP est colorée avec *info*, et est précédée d'une icone `arrow_exchange`
- Les informations utilisateur utilisent une classe text-muted. L'icone est `user_admin`
- Les informations de site utilisent une classe text-muted. L'icone est `buildings`

Tous les caractères sont affichés à une taille de `12px`

#### Mises à jour ####

En ce qui concerne le nom principal, affiché en gras : Certains objet ont un nom dédié, renseigné par l'utilisateur. C'est le cas des dossiers, sociétés, contrats. Pour les autres éléments, on affichera le nom de l'article (non conformité, demande d'achat) ou de la société (consultation, offre e.g.) associés.

> On s'affranchit ainsi de la lourdeur de la *description courte* sur une non-conformité. Ici, on affichera **l'article** en tant que nom principal

---

Le principe de mise en page évolue vers quelque chose de plus simple pour ce composant. Au lieu de répartir le contenu des données sur une grille, on les affichera les unes à côté des autres, horizontalement (en `flex-direction : row`, par exemple). Les colonnes s'aditionnant ainsi, chacune ayant une largeur relative à son contenu.

---

Exit, également, les KPIs saillantsn, avec label au dessus et valeur en dessous, en gras. Tous les KPIs s'affichent désormais *en ligne* ; on veillera à ne pas en afficher plus de trois en hauteur, et pas plus de cinq en tout.

#### Rétractation/déploiement ####

L'en-tête a une capacité de rétractation, qui permet de gagner de la place en hauteur. Replié, l'en-tête à une hauteur fixe de `104px`. Seules les informations principales sont affichées :
- le nom principal
- référence
- type
- utilisateur et site (on retire la donnée de provenance ERP)
- un ou deux KPIs, en fonction de la place disponible

On peut rétracter ou déployer l'en-tête en cliquant sur la barre grise à bouts arrondies, affichée à 4px sous la ligne d'onglets, et centrée avec l'en-tête. La barre grise a les caractéristiques suivantes :

``` css
width: 36px;
height: 4px;
background: #B2B5B8;
```

Il est essentiel, pour que l'usage de cet interacteur soit compris, que le curseur affiché au survol soit adapté :

``` css
cursor: n-resize;
```

## Modales ##

<div class="alert alert-warning" role="alert">
  Ces informations ne sont plus à jour. Elles sont reprises et modifiées dans le sprit suivant (sprint 2)
</div>

Toutes les fenêtres modales ont été revues. Certains champs ont été redisposés pour grouper l'information de façon logique, et faciliter la compréhension de l'utilisateur. Les mises à jour importantes sont les suivantes :

- **Des séparateurs** (couleur `#DFDFDF`) sont utilisés pour répartir les groupes de champs de façon logique
- La `largeur de la modale` a été revue. Elle fait désormais `720px`, et est disposée à `64px` du bord haut du `viewport`
- **Les champs ont trois tailles** : *small* (`80px`), *medium* (`192px`) et *large* (`510px`), et correspondent à la taille de la valeur attendue
- **Les champs déroulants** sont [ceux de Bootstrap](https://getbootstrap.com/docs/5.0/components/dropdowns/#single-button)

> Pour les messages : un utilisateur interne ou externe doit pouvoir être ajouté dans le même champ. Ainsi, on ajoutera un utilisateur interne en utilisant la recherche contextuelle. Si l'utilisateur entre une adresse mail inconnue du système et appuie sur `RET`, cette adresse est alors ajoutée en tant que destinataire. La différence entre destinataire interne et externe est matérialisée par la couleur du badge (_primary_ ou _light_).

Le comportement général, ainsi que l'affichage, est celui-ci proposé dans la section *Modales I*. La section *Modales II* reprend toutes les mises à jour de formulaires de création d'objets. La section *Modales III* évoque quant à elle le cas des formulaires longs.

> Une [ligne de fold](https://logoscreative.com/the-fold-in-web-design-explained-simply/?share=google-plus-1) est matérialisée en pointillés rouge, et permet de voir à partir de quel moment le contenu sera masqué

#### Formulaires longs ####
Trois formulaires d'ajout ont été identifiés comme particulièrement longs, et devront potentiellement pouvoir bénéficier d'un traitement _ad hoc_. Ce sont les formulaires d'ajout de :
- Société
- Ligne de contrat
- Paramètres utilisateur

À chaque fois, deux options sont proposées : une tentative de gain d'espace, et une réorganisation en colonnes

###### Gain d'espace ######
C'est la piste privilégiée pour rendre ces formulaires plus digestes. Certaines sections, contenant des informations non obligatoires, peuvent être masqués (voir *paramètres supplémentaires* sur *Ligne de contrat* e.g.) et être déployés au besoin. 

De même, on peut regrouper sur une même ligne plusieurs champs *small* (voir *quantités* sur *ligne de contrat* e.g.) ou *médium* (voir code postal, ville, etc. dans *société* e.g.). Les labels seront alors au dessus de ces champs alignés horizontalement.

###### Colonnes ######
Les champs du formulaire peuvent être répartis en plusieurs colonnes : la modale prend alors toute la place disponible à l'écran (moyennant `16px` de marge minimum avec le bord du *viewport*), et tous les champs sont directement affichés.

Cette solution peut sembler intéressante, mais elle comporte les problèmes suivants :
- si du contenu disparait à nouveau sous le fold, un scroll devra être mis en place, mais il le sera alors sur deux colonnes, ce qui est à bannir en terme de lecture et d'ergonomie
- les références visuelles (alignement des champs sur leur gauche) sont diluées dans la nouvelle configuration

> Pour conclure : **la recommandation UX pour ce sujet** et que le scroll, en plus de ne pas poser de problème ergonomique rédhibitoire, permet un développement progressif de l'information, facilité par la présence des séparateurs. On garde l'alignement des champs du formulaire, ce qui permet de garder l'information bien ordonnée. La nouvelle largeur des formulaires donne plus d'aise à l'utilisateur, ce qui tend à atténuer la lourdeur perçue dans la proposition UX précédente.

## Chargement des données ##
Plusieurs solutions pour l'attente pendant les temps d'attente du système.

> À chaque fois, l'animation d'attente est essentielle pour ne pas induire un blocage de l'application

#### Premier chargement d'un tableau ####
La [technique du skeleton](https://css-tricks.com/building-skeleton-screens-css-custom-properties/) est utilisée pour faire patienter l'utilisateur pendant le chargement d'un gros jeu de données. Ici, on matéralise les données du tableau par des rectangles gris `#DFDFDF`

#### Chargement des données au scroll sur un tableau ####
Un spinner (icone `spin`), colorée en `#6C757D`, tourne dans un espace blanc de `80px` de hauteur pour faire patienter pendant le chargement des données à afficher au scroll

#### Actualisation d'un jeu de données ####
Lorsqu'un changement engage des calculs significatifs au système, comme lors de l'actualisation d'un chiffrage, l'interface est momentanément indisponible. On affiche un overlay noir (opac. `65%`), sur lequel une modale sans titre ni action vient accueillir un spinner (voir § précédent) en rotation, et une phrase indiquant la nature du travail en cours. La modale est masquée dès que le résulat du nouveau calcul est disponible.

## Données consultées ##
Lorsqu'un site est sélectionné, les données globales correspondent alors à celui-ci. Un bandeau de couleur _warning_ (bordure en bas, d'1 pixel couleur `#ECCC25`) est affiché sur **toute la largeur** de l'application. Un icone _eye_ précède la phrase indiquant la nouvelle configuration de l'affichage.

## Liaison entre objets ##
Règle générale à appliquer partout : toute référence faite, dans un tableau, à un objet qui s'appuie sur une vue *show*, doit posséder un accès vers celle-ci. On affichera un bouton doté d'une simple icone `arrowright` (couleur _primary_ au rollover) à droite de la référence ou, à défaut, à droite du titre.


## Recommandations générales ##
Sauf contre-indication d'usage, il faudra veiller à passer en minuscules toutes les chaînes de caractères affichées en capitales, en utilisant l'une ou l'autre de ces propriétés CSS

``` css
text-transform : lowercase | capitalize
```

Ou en utilisant une fonction, côté client, qui modifie l'affichage des données extraites de la base avant de les montrer à l'utilisateur.
