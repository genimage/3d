---
layout: article
titles: Modeling
permalink: /pages/modeling

aside:
  toc: true

sidebar:
  nav: docs-en

---

_____


# Modeling

Le modeling est la tâche qui consiste a créer les objets en volume.
{:.info}

Les objets 3D sont composés de points (ou vertex, vertices au pluriel), d'edges (ou arêtes, cotés) et de faces ( ou polygones).\\
On les appelle composants (components).

![PointEdgeFace]({{"/assets/images/PointEdgeFace.jpg" | absolute_url}})

La position d'un point est definie par 3 valeurs X,Y et Z, ce sont ses coordonnées

![PointCoordinates]({{"/assets/images/PointCoordinates.png" | absolute_url}})

Dans cet exemple le point a pour coordonnées (2,3,4)

![Cube]({{"/assets/images/Cube.jpg" | absolute_url}})

Pour décrire ce cube de manière textuelle (fichier obj):

~~~~~~
v 0.5 -0.5 0.5
v -0.5 -0.5 0.5
v 0.5 0.5 0.5
v -0.5 0.5 0.5
v -0.5 -0.5 -0.5
v 0.5 -0.5 -0.5
v -0.5 0.5 -0.5
v 0.5 0.5 -0.5

f 1 3 4 2
f 5 7 8 6
f 7 4 3 8
f 6 1 2 5
f 6 8 3 1
f 2 4 7 5
~~~~~~

* Chaque ligne commençant par un "v" est un point et les valeurs sont ses coordonnées X Y Z
* Chaque ligne commençant par un "f" est une faces et les valeurs sont les points qui la compose

on peut noter que chaque face est composée de 4 points, l'objet est composé de 6 polygones à 4 côtés.

L'ensemble point,edges et polygones est appelé maillage ou mesh
{:.info}

## Subdivision de surface

De part sa nature polygonale la surface d'un objet en 3D est anguleuse.

![Subdiv]({{"/assets/images/Subdiv.jpg" | absolute_url}})

La subdivision de surface est une technique permettant de subdiviser/lisser les objets 3D
{:.info}

Sur un film d'animation on travaille avec des objets non subdivisés cela permet d'avoir des objets léger (moins de points a gérer, scenes plus légères, rapidité d'affichage,..)\\
Ce n'est qu'au moment du calcul de l'image finale (rendering) que la subdivision de surface est appliquée.

## Topologie

La topologie est l'organisation du maillage
{:.info}

![Topology1]({{"/assets/images/Topology1.jpg" | absolute_url}})

Ici nous avons 4 spheres ayant la même forme, le même volume mais leurs topologies sont différentes.


### Pourquoi la topologie est importante ?

![TopologySubdiv]({{"/assets/images/TopologySubdiv.jpg" | absolute_url}})

* Avec une mauvaise topologie la Subdivision de surface n'est pas propre.


![TopologySkin]({{"/assets/images/TopologySkin.gif" | absolute_url}})


* Avec une mauvaise topologie les déformations de l'animation ne sont pas correctes.

* Il existe de nombreuses autres raisons que nous verrons dans la suite des cours qui démontreront  l'importance d'une bonne topologie.




Une bonne topologie n'est pas une option c'est une nécéssité fondamentale.
{:.error}

### Comment fait-on une bonne topologie ?

Il n'existe pas **encore** de programme faisant automatiquement des topologies aussi bonnes que les modeleurs professionnels.\\
Il n'existe pas à ma connaissance de recette miracle... l'expérience est primordiale.

Il existe néamoins des régularités et avec de la pratique on y arrive assez intuitivement.

Quelques règles vers lesquelles tendre (attention il est impossible de modeliser en les appliquant toutes strictement):

![TopologyRule01.jpg]({{"/assets/images/TopologyRule01.jpg" | absolute_url}})

* Utiliser uniquement des polygones à 4 cotés (quad)

![TopologyRule03.jpg]({{"/assets/images/TopologyRule03.jpg" | absolute_url}})

* Un quad doit avoir ses angles proches de 90° (shearing)

![TopologyRule04.jpg]({{"/assets/images/TopologyRule04.jpg" | absolute_url}})

* Un quad doit être coplanaire (ses points situés dans un même plan)

![TopologyRule02.jpg]({{"/assets/images/TopologyRule02.jpg" | absolute_url}})

* Les lignes doivent être réparties progressivement
* Pour marquer un angle il faut plusieurs lignes rapprochées
* Un quad ne doit pas avoir un côté très petit et un autre très long (mais plutôt se rapprocher d'un carré)

![TopologyRule05.jpg]({{"/assets/images/TopologyRule05.jpg" | absolute_url}})

* Dans le cas d'un animal ou d'un humain les lignes suivent les formes des muscles

**Il faut étudier attentivement des maillages de qualité professionnelle et s'en servir comme référence:**

[Gallerie d'exemples de topologies]({{"/pages/GalleryTopo.html" | absolute_url}}){:.button.button--success.button--pill}





## Direct modeling

Le direct modeling est une manière de modéliser en démarrant d'une simple primitive (cube,sphere,cylinder,grid,...) ou de rien \\
L'artiste modifie la primitive de départ grâce à des opérations de modélisation.

Voici les opérations les plus courrantes (les noms varient d'un logiciel à l'autre):

![ModelingTools01.gif]({{"/assets/images/ModelingTools01.gif" | absolute_url}})

Move/Rotate/Scale sur les components (ici sur les points)

![ModelingTools02.gif]({{"/assets/images/ModelingTools02.gif" | absolute_url}})

Split Edge loops

![ModelingTools03.gif]({{"/assets/images/ModelingTools03.gif" | absolute_url}})

Extrude

![ModelingTools04.gif]({{"/assets/images/ModelingTools04.gif" | absolute_url}})

Cut

![ModelingTools05.gif]({{"/assets/images/ModelingTools05.gif" | absolute_url}})

Edge collapse

![ModelingTools06.gif]({{"/assets/images/ModelingTools06.gif" | absolute_url}})

Weld (points)

![ModelingTools07.gif]({{"/assets/images/ModelingTools07.gif" | absolute_url}})

Bridge (faces)

![ModelingTools08.gif]({{"/assets/images/ModelingTools08.gif" | absolute_url}})

Curve revolution

![ModelingTools09.gif]({{"/assets/images/ModelingTools09.gif" | absolute_url}})

Extrude along curve


Le TP relatif à ce cours:

[TP Direct Modeling 1]({{"/pages/directModeling01.html" | absolute_url}}){:.button.button--success.button--pill}


## Sculpt et re-topologie

Une autre méthode de modélisation consiste à séparer volume et topologie en deux étapes.

![Modeling_Pixar_Sculpt]({{"/assets/images/Modeling_Pixar_Sculpt.jpg" | absolute_url}})

Sur cette image on peut voir une sculpture réelle en argile du visage de Woody  (à droite) et le résultat en 3D avec sa topologie (à gauche)

Un artiste a sculpté le visage puis le model a été scanné en 3D.
Une re-topologie a été effectuée

![Modeling_Retopology]({{"/assets/images/Modeling_Retopology.jpg" | absolute_url}})

Voici un autre exemple d'un début de re-topologie

Les polygones sont créés par dessus un sculpt 3D très détaillé ayant une topologie anarchique, l'artiste s'en sert comme guide.
