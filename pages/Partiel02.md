---
layout: article
titles: Partiel 02
permalink: /pages/Partiel02



---

_____


# OrcSword

**Réaliser cette épée en s'approchant au plus prêt de son aspect:**


![OrcSword]({{"/assets/images/OrcSword.jpg" | absolute_url}})
![OrcSword]({{"/assets/images/OrcSword02.jpg" | absolute_url}})
![OrcSword]({{"/assets/images/OrcSword03.jpg" | absolute_url}})
![OrcSword]({{"/assets/images/OrcSwordTurn.gif" | absolute_url}})


* L'objet doit être subdivisable (contrairement à l'objet présent sur l'image).
* Le projet se nomme **OrcSword**
* Dans un premier temps ,modeliser le cuir et le metal en objets séparés.
* Faire les UVs

S'assurer que le module unfold soit bien loadé (windows/preferences/plug-in)
{:.info}

S'assurer que la valeur de l'option de l'outil layout "Shell Pre-Scaling" soit sur "Preserve 3D Ratios"
{:.info}

* Fusionner les objets (mesh/combine)
* Re-faire un layout des UVs (pas de superpositions)
* Assigner un materiau (blinn) aux polygones correspondants au cuir 
* Nommer le **Shading group** "Leather"
* Assigner un materiau (blinn) aux polygones correspondants au metal
* Nommer le **Shading group** "Metal"
* Dupliquer le model de l'épée
* Lui appliquer une subdivision ( Mesh/Smooth)
* Nommer Le duplicata OrcSword_HD
* Le selectionner et l'exporter en obj ( OrcSword_HD.obj)
* Ouvrir Substance Painter
* Importer son objet (file/new) + Document resolution 4096
* Enregistrer son projet (.spp)
* Réaliser les textures et matériaux dans substance painter et photoshop,  **pas d'utilisation de Zbrush**

Vous pouvez télécharger des textures sur internet
{:.info}

* Faire un Rendu en 1920*1080 depuis substance painter  (Mode/Rendering)
* Sauvegarder l'image rendue

Ne pas exporter pas les textures de substance painter. Je corrigerais en ouvrant le fichier .spp
{:.info}

* Livrer son dossier de travail sur la clé usb du surveillant


**Une tolerance zero s'appliquera à la nomenclature. (mauvaise nomenclature-> je ne corrige même pas -> 0 )**
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
			OrcSword_001.spp
			OrcSword_00?.spp
			....
			OrcSword_HD.obj
			OrcSword_UV.png
			OrcSword_Metal_Mask.psd
			OrcSword_Metal_Mask.jpg
			....
			OrcSword_Leather_??????.jpg
~~~~~~



