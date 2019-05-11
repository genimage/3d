---
layout: article
titles: RoomProject
permalink: /pages/RoomProject

aside:
  toc: true

sidebar:
  nav: docs-en

---

_____


# RoomProject

## Sujet

Par groupe de 2 personnes, votre projet est de designer,modéliser,texturer et éclairer un décor intérieur.
Vous choisirez parmis les univers suivants:
* Steampunk
* Pirate
* Hightech
* Horreur

Le style doit être semi réaliste.

La modelisation devra être subdivisable.

Vous devrez réaliser le sol + deux pans de murs consécutifs + tous les props comme dans les exemples ci-dessous :

![DesignExample]({{"/assets/images/design-exemple_01.jpg" | absolute_url}})
![DesignExample]({{"/assets/images/design-exemple_02.jpg" | absolute_url}})
![DesignExample]({{"/assets/images/design-exemple_03.jpg" | absolute_url}})

## Notes Techniques

Tous le décors est assemblé dans une scene maya nommée RoomProject.mb

Chaque objet doit être "combine": 1 objet = 1 Mesh

Les objets sont nommez en anglais sans caratère spécial ( pas de "-", pas de "_",pas d'accents).

Si l'objet a un nom composé par exemple "machine gun" les mots seront collés avec une majuscule au début de chaque mot:

MachineGun.

Tous les objets ont des UVs valides,réguliers et sans superpositions , Les UVs peuvent êtres décomposés en plusieurs UDIMs.

Chaque objet est texturé dans Substance Painter.

<div>{%- include extensions/vimeo.html id='335608672' -%}</div>

Les textures sont exportées depuis substance dans un dossier du même nom au format Tif 8bits selon cette nommenclature:
~~~~~~
RoomProject\
		RoomProject.mb
		Textures\
				ObjectName\
					ObjectName_1001_BaseColor.tif
					ObjectName_1001_Metallic.tif
					ObjectName_1001_Normal.tif
					ObjectName_1001_Roughness.tif
					ObjectName.spp
						
		WIP\	
			...
~~~~~~

Si plusieurs objets doivent avoir le même matériau comme par exemple des pièces de monnaies dupliquées x fois.
Dans la scene Maya vous devrez ajouter le séparateur "_" + son numero:

~~~~~~
Coin_01
Coin_02
Coin_03
~~~~~~

Le dossier unique contenant les textures sera:

~~~~~~
		Textures\
				Coin\
					Coin_1001_BaseColor.tif
					Coin_1001_Metallic.tif
					Coin_1001_Normal.tif
					Coin_1001_Roughness.tif

~~~~~~

**Cas particulier:**

Si par exemple pour un coffre vous avez la necessité de faire 2 mesh vous les nommerez ainsi dans Maya:

~~~~~~
ChestIron
ChestWood
~~~~~~

Leurs textures correspondantes seront alors nommées ainsi:

~~~~~~
		Textures\
				ChestIron\
					ChestIron_1001_BaseColor.tif
					ChestIron_1001_Metallic.tif
					ChestIron_1001_Normal.tif
					ChestIron_1001_Roughness.tif
					....
				
				ChestWood\
					ChestWood_1001_BaseColor.tif
					ChestWood_1001_Metallic.tif
					ChestWood_1001_Normal.tif
					ChestWood_1001_Roughness.tif
					....		

~~~~~~

Dans le cas d'un objet ayant une partie devant avoir un matériau transparent vous devrez obligatoirement en faire un mesh séparé.
{:.error}

Par exemple une bouteille en verre avec un bouchon en liège, dans Maya il y aura 2 meshs nommés ainsi:

~~~~~~
BottleGlass
BottleCork
~~~~~~

Leurs textures correspondantes seront alors nommées ainsi:

~~~~~~
		Textures\
				BottleGlass\
					BottleGlass_1001_BaseColor.tif
					BottleGlass_1001_Metallic.tif
					BottleGlass_1001_Normal.tif
					BottleGlass_1001_Roughness.tif
					....
				
				BottleCork\
					BottleCork_1001_BaseColor.tif
					BottleCork_1001_Metallic.tif
					BottleCork_1001_Normal.tif
					BottleCork_1001_Roughness.tif
					....		

~~~~~~




