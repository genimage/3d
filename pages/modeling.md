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

Le modeling est la tâche qui consiste a créer les objets en volume.\\
Les objets 3D sont composés de points (appelés parfois vertex), d'edges (les cotés) et de faces.

![PointEdgeFace]({{"/assets/images/PointEdgeFace.jpg" | absolute_url}})

La position d'un point est definie par 3 valeurs X,Y et Z, ce sont ses coordonnées

![PointCoordinates]({{"/assets/images/PointCoordinates.png" | absolute_url}})

Dans cet exemple  Le point a pour coordonnées (2,3,4)

![Cube]({{"/assets/images/Cube.png" | absolute_url}})

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

on peut noter que chaque faces est composée de 4 points, l'objet est composé de polygones à 4 côtés.



# Direct modeling


blah,blah,blah

# Sculpt et re-topologie

## Intro

Une autre méthode de modélisation consiste à séparer volume et topologie en deux étapes.

![Modeling_Pixar_Sculpt]({{"/assets/images/Modeling_Pixar_Sculpt.png" | absolute_url}})

Sur cette image on peut voir une sculpture réelle en argile du visage de Woody  (à droite) et le résultat en 3D avec sa topologie (à gauche)

Un artiste a sculpté le visage puis le model a été scanné en 3D.
Une re-topologie a été effectuée

![Modeling_Retopology]({{"/assets/images/Modeling_Retopology.jpg" | absolute_url}})

Voici un autre exemple d'un début de re-topologie

Les polygones sont créés par dessus un sculpt 3D très détaillé ayant une topologie anarchique, l'artiste s'en sert comme guide.
