---
layout: article
titles: Partiel 02
permalink: /pages/Partiel02



---

_____


# OrcSword

Réaliser cette épée en s'approchant au plus prêt de son aspect:


![OrcSword]({{"/assets/images/OrcSword.jpg" | absolute_url}})

* L'objet doit être subdivisable (contrairement à l'objet présent sur l'image).
* Le projet se nomme OrcSword
* Dans un premier temps ,modeliser le cuir et le metal en objets séparés.
* Faire les UVs

S'assurer que:
*le module unfold est bien loadé (windows/preferences/plug-in)
*Les préférences du layout : 
*Shell Pre-Scaling -> Preserve 3D Ratios
{:.info}

* Fusionner les objets (combine)
* ReFaire un layout des UVs (pas de superpositions)
* Assigner un materiau (blinn) aux polygones correspondants au cuir 
* Nommer le Shading group "leather"
* Assigner un materiau (blinn) aux polygones correspondants au metal
* Nommer le Shading group "Metal"
* Dupliquer le model de l'épée
* Lui appliquer une subdivision ( Mesh/Smooth)
* Nommer Le duplicata OrcSword_HD
* Le selectionner et l'exporter en obj ( OrcSword_HD.obj)
* Ouvrir Substance Painter
* Importer son objet (file/new) + Document resolution 4096
* Enregistrer votre projet.
* Réaliser les textures et matériaux dans substance painter et photoshop (zbrush non admis)
* Faire un Rendu en 1920*1080 dans substance painter  (Mode/Rendering)
* Sauvegarder l'image rendue
* Livrer votre dossier de travail sur la clé usb du surveillant


Une tolerance zero s'appliquera à la nomenclature. (mauvaise nomenclature-> je ne corrige même pas -> 0 )
{:.error}

Nomenclature:
~~~~~~
VotreNom_OrcSword\
		OrcSword.mb
		OrcSword.spp
		OrcSword.jpg
		WIP\	
			OrcSword_001.mb
			OrcSword_00?.mb
			....
			OrcSword_HD.obj
			OrcSword_UV.png
			OrcSword_Metal_Mask.jpg
			....
			OrcSword_Leather_???.jpg
~~~~~~



