---
title: Introduction
layout: page
page_weight: -11
category: "ui"
---
* table of contents
{:toc}

Le système graphique présenté ici a été basé sur l'utilisation du framework [Bootstrap <i class="ico">external_link</i>](https://getbootstrap.com/docs/4.5/getting-started/introduction/). L'utilisation de ce framework permet d'atteindre rapidement un résultat satisfaisant pour l'utilisateur. La personnalisation de certaines variables comme les couleurs et les polices de caractère permet d'adapter visuellement le jeu de règles d'affichage au produit Cobuy.

[ capture 100% de l'ui ]

## Points d'attention ##
Même si le framework, personnalisé, répond à la plupart des besoins, il y a néanmoins certains composants qui vont nécessiter une attention particulière, et peut-être bénéficier de règles d'affichage _ad hoc_ :
- la navigation principale, qui est le point de départ de l'interface, doit bénéficier d'une grande attention, car elle va concentrer une partie non négligeable des *clics* qui vont être effectués sur l'interface.
- Dans l'objet *dossier*, les parties [*besoins*](ui.dossiers.html#besoins) et [*chiffrage*](ui.dossiers.html#chiffrage) embarquent des composants aux fonctionnalités poussées. Des interactions particulières 

## Gabarits ##

Les gabarits sont des modèles d'écran dont la structure, les mécanismes et les interactions sont partagés par plusieurs objets. Deux gabarits sont utilisés pour une grande partie des écrans de l'interface :
- [le gabarit de liste](gabarits.listes.html), qui habille les écrans qui accueillent l'utilisateur dans chaque section. Ces éléments sont en outre repris à l'intérieur de certaines occurences d'objets, comme les dossiers
- [le gabarit de détail](gabarits.details.html), qui s'occupe de présenter les informations d'une occurrence d'un objet. Il dispose d'un système de navigation interne.

L'écran de [catégorie](ui.categories.html) bénéficie, lui, d'une structure particulière. [Les paramètres](ui.parametres.html), quant à eux, sont des écrans plus basiques, et réutilisent des composants comme les [*list groups* <i class="ico">external_link</i>](https://getbootstrap.com/docs/4.5/components/list-group/#links-and-buttons) les [tableaux](comp.tableaux.html) ou les [fenêtres modales](comp.modales.html).
