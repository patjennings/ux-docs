---
layout: home
title: Bienvenue
---

Ce site documente les principes visuels, d'ergonomie et d'interactions de l'application Cobuy v2. 

Il donne des recommandations sur la meilleure façon d'utiliser le design dans la construction du produit, afin de bénéficier du travail préparatoire de conception et d'obtenir un résultat qui satisfait les utilisateurs et leur permet d'être efficaces. 

#### Comment utiliser cette documentation ? ####

Cette documentation est à l'usage de plusieurs intervenants : l'équipe produit et l'équipe de développement. C'est pourquoi elle traite autant de problématiques *haut-niveau* (mécanismes généraux, place de l'utilisateur) que de problématiques *bas-niveau* (détail de la construction des composants et des interactions).

**La partie *UX*** traite de la ligne directrice et des mécanismes généraux qui régissent l'interface utilisateur. Cette partie traite de l'état d'esprit dans lequel le produit est envisagé, et propose un socle sur lequel celui-ci pourra se développer

**La partie *Gabarits*** traite des modèles d’écran dont la structure, les mécanismes et les interactions sont partagés par plusieurs objets (dossiers, sociétés, articles, etc.).

**La partie *Composants*** détaille l'utilisation d'éléments utilisés à plusieurs endroits de l'interface, comme les couleurs ou la typographie, mais aussi de composants mutualisés comme les tableaux, les fenêtres modales, etc.

**La partie *UI*** donne les spécifications pour chaque grande section de l'interface. Ces dernières ré-utilisent pour partie des composants détaillés dans la partie précédente, mais elles ont également des besoins propres : ils sont détaillés ici.

Enfin, **la partie *Ressources*** regroupe les liens et fichiers rencontrés tout au long de cette documentation.

#### Terminologie ####
Il sera souvent évoqué dans cette documentation la notion *d'objet* ou *d'occurence*. Ces deux éléments sont liés, en voici l'explication :
- **l'objet** est un élément type de l'interface : un dossier, une consultation, une offre, un article, une non-conformité. Il correspond aux sections de navigation de la barre de gauche
- **l'occurence** est un élément issu de cet objet : le *dossier DOS-02568* et le *dossier DOS-84459* sont des occurences de l'objet *dossier*

#### Et après ? ####

Cette documentation est conçue pour évoluer. Il conviendra d’étudier les besoins des utilisateurs et leurs usages dans la nouvelle version de Cobuy, pour ensuite amender et faire évoluer les principes de conception.

La pahse de construction de l'interface peut être envisagée ainsi :
> - On construira l'interface utilisateur à partir des éléments fournis, en respectant la cohérence du système de conception.
> - Si quelque chose ne fonctionne pas comme prévu, il peut y avoir un écart avec la recommandation. Le bon sens prévaut, mais il important de tester les deux versions pour vérifier que le gain est véritable.
> - les nouvelles décisions sont documentées, et on s'appuiera sur elles pour les évolutions futures.


