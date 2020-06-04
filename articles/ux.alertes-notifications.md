---
title: Alerter, notifier
layout: page
page_weight: 0
category: "ux"
---
* table of contents
{:toc}

La notion de notification, ou d'alerte (selon la criticité de l'information) est présente à plusieurs niveaux de l'interface, et intervient selon des temporalités diverses. Il est également important de noter que l'utilisateur devrait être averti des actions négatives (erreur, non conformité d'une action) comme des actions positives (action ayant aboutie). Il conviendra pour cela de jauger finement la quantité d'informations à remonter à l'utilisateur : trop de messages, et il aurait tendance à ignorer et à manquer une notification importante dans un futur plus ou moins proche. Pas assez de messages, et l'utilisateur n'est pas capable de pondérer l'information ou de résoudre des problèmes dans l'interface.

> Le dévoilement progressif d'une information permet à un utilisateur d'avoir, selon son besoin, plus ou moins de détails (d'abord un message dans une notification, puis une vision plus détaillée dans une modale, puis une page retracant la totalité d'une anomalie *ou* une page de documentation pouvant aider l'utilisateur *e.g.*) 

<p class="small text-muted">Schéma de principe du dévoilement progressif d'une information</p>
![dévoilement progressif](assets/images/progressif.png)

#### À la connexion ####
On avertit l'utilisateur de changements qui auraient eu lieu depuis sa dernière connexion. Seul l'utilisateur voit ces notifications

#### Notifications système ####
Certains objets de l'interface ont 

Il y a plusieurs moyens d'afficher ces informations : par des [cartes d'alertes](gabarits.details.html#alerte), ou [par des badges ](comp.navigation.html#notifications)à côté des entrées qui remontent des avertissements.

#### Après une action ####
Après une action directe de l'utilisateur, plusieurs types de notifications sont possibles : 
- l'action a abouti
- l'action n'a pas abouti
  - cela est lié à une action non conforme, ou non autorisée, de l'utilisateur
  - cela provient du système (erreur de configuration, éléments *down*, comme l'accès à une base de données *e.g.*)

Ces messages sont affichés sous forme de [toaster](comp.notifications.html). Conformément au principe évoqué en introduction de cette section, le message initial sera court, synthétique, et un bouton pourra diriger l'utilisateur vers une version plus détaillée de celui-ci, si nécessaire.

#### particulier ####

chiffrage, avertir l'utilisateur que l'information sous nos yeux n'est pas complète/erronnée

#### À propos de l'automatisation ####

Si le système effectue certaines tâches seules , l'utilisateur doit en être averti d'une façon ou d'une autre, et il doit savoir comment désengager cette automatisation. Il est perturbant pour l'utilisateur d'avoir sous les yeux une donnée dont il ignore la provenance, un paramètre modifié sans qu'il en ait la connaissance.

> L'automatisation est une bonne chose, mais l'utilisateur reste le maître à bord.
