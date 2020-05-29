---
title: Typographie
layout: page
page_weight: -8
category: "ui"
---
* table of contents
{:toc}

La police de caractère utilisée dans l'interface est la [Lato](https://fonts.google.com/specimen/Lato), de Google. Elle est choisi pour son élégance et sa lisibilité, aussi bien en texte qu'en titrage.

[ Spécimen rapide ]

#### Exemples d'utilisation ####

Outre les titres, quelques styles à utiliser avec Bootstrap nous intéressent particulièrement. L'utilisation conjointe de ces 4 styles permet quasiment à elle seule de hiérarchiser un écran, et de proposer à l'utilisateur une déchiffrage progressif de l'information. 

> Cette technique assure un confort d'utilisation et une bonne compréhension des informations que l'utilisateur a sous les yeux.

<p>Voici le style par défaut.</p>

``` html
<p>Une information</p>
```


<hr/>

<p><strong>Si une information mérite d'être vue immédiatement, on la traitera avec la balise <code>&lt;strong&gt;</code>.</strong></p>

``` html
<p><strong>Une information importante</strong></p>
```


> **Attention à ne mettre en valeur que quelques informations par écran avec ce style**. Dans un tableau, par exemple, il n'y aura sûrement qu'une ou deux colonnes qui se verront habillées de ce style.

<hr/>

<p class="text-muted">La classe <code>text-muted</code> permet d'établir une hiérarchie claire. Cela ne signifie pas que ces informations n'ont pas d'importance, mais simplement qu'elles ne devraient sûrement pas être vues avant celles traitées avec les deux styles précédents.</p>

``` html
<p class="text-muted">Une information de second ordre</p>
```


<hr/>

<p class="small text-muted">On ajoutera une classe <code>small</code> à <code>text-muted</code> lorsqu'on habille une information périphérique, comme une aide ou une légende.</p>

``` html
<p class="small text-muted">Une légende ou une aide</p>
```



