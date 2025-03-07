
# DUSB Tester  : Fabrication
Dans cette vidéo, découvrez le testeur USB entièrement assemblé et programmé !  

[![Voir la démonstration](images/video-thumbnail.jpeg)](https://tube-sciences-technologies.apps.education.fr/w/i4Xqwx69rhGFDRBjq2J4fU)

Ce projet, basé sur une carte Arduino, intègre :
- **4 LEDs** et **4 boutons** pour reproduire la séquence du jeu,
- Un **buzzer** pour les signaux sonores,
- Un **boîtier imprimé en 3D** réalisé sur mesure,


# Dossier de conception du shield Arduino

Voici un guide étape par étape pour concevoir et assembler la carte électronique intégrant des composants CMS (résistances et LED montées en surface) ainsi que des composants traversants (comme le connecteur Arduino et le buzzer). Ce procédé  inclut l'application manuelle de pâte à braser et le passage en four à refusion sans utilisation de stencil.

## 1. Génération des Fichiers de Fabrication

- **Fichiers Gerber :**
- Télécharger [fichiers de fabrication gerber Simon3.zip](hardware/kicad/simon3/production/simon3.zip)
- **Fabrication du PCB :**
- Envoyez ces fichiers à un fabricant de PCB (JLCPCB)

## 2. Nomenclature

| Reference         | Value        |  Qty |
|-------------------|--------------|----- |
| BZ1               | Buzzer       |  1   |
| D1                | LED RED      |  1   |
| D2                | LED Green    |  1   |
| D3                | LED Blue     |  1   |
| D4                | LED Yellow   |  1   |
| J1                | Power        |  1   |
| J2,J4             | Digital/PWM  |  2   |
| J3                | Analog       |  1   |
| R1,R2             | 160          |  2   |
| R3                | 100          |  1   |
| R4                | 150          |  1   |
| R5,R6,R7,R8       | 10k          |  4   |
| SW1,SW2,SW3,SW4   | SW_Push      |  4   |

[Nomenclature](hardware/kicad/simon3/simon3.csv)

## 4. Préparation à l’Assemblage

- **Nettoyage du PCB :**
  - Assurez-vous que la carte est propre et exempte de poussière ou d’empreintes.
- **Mise en place du poste de travail :**
  - Organisez votre matériel : pâte à braser (en seringue), fer à souder pour les composants traversants, four à refusion.
- **Documentation :**
  - Imprimez le schéma et/ou un plan de positionnement (layout) pour guider le placement des composants.
![Implantation ](hardware/kicad/simon3/implantation.pdf)


# Brasage des composants

![carte à braser](images/etape1.jpg) 

## 1. Application de la Pâte à Braser (Sans Stencil)

![Appliquer la pâte](images/etape2.jpg) 

- **Utilisation d’une seringue :**
  - À l’aide d’une seringue, déposez manuellement la pâte à braser sur chaque zone de montage des composants CMS.
  - Veillez à appliquer la quantité appropriée pour chaque pad afin d’éviter les ponts de soudure ou les soudures insuffisantes.
- **Précision :**
  - Pour les zones très fines, utilisez une seringue à embout fin et, si besoin, une loupe pour vérifier l’exactitude de l’application.

## 6. Placement des Composants CMS

![Peupler les CMS](images/etape3.jpg)

- **Positionnement :**
  - Placez délicatement les composants CMS (résistances, LED, etc.) sur les pads recouverts de pâte.
  - Vérifiez l’alignement et l’orientation (notamment pour les composants polarisés comme certaines LED).
- **Ajustement :**
  - Corrigez la position des composants si nécessaire avant le passage en four.

## 7. Passage en Four à Refusion

![Mettrer au four](images/etape4.jpg)

- **Programmation de la courbe de chauffe :**

  - Programmez le four à refusion selon une courbe de température adaptée (phase de préchauffage, pic de température, et refroidissement contrôlé).

- **Refusion :**
  - Placez la carte dans le four et lancez le cycle.
  - Surveillez le processus pour vous assurer que la pâte à braser fond correctement et forme des joints solides.
- **Refroidissement :**
  - Laissez la carte refroidir progressivement pour éviter les contraintes thermiques.

![Sortir du four](images/etape5.jpg)

## 8. Soudure des Composants Traversants

- **Placement manuel :**
  - Après la refusion des composants CMS, positionnez les composants traversants (connecteur Arduino, buzzer, etc.) sur la carte.
- **Soudure :**
  - Utilisez un fer à souder pour souder manuellement ces composants.
  - Assurez-vous de réaliser des soudures nettes et sans ponts.
- Utilisation d'une carte Arduino HS pour pour maintenir le shield et les connecteurs 
![Arduino HS](images/etape6.jpg)
- Placer la carte par dessus 
![Shield maintenu sur l'Arduino UNO](images/etape7.jpg)
![Soudure du connecteur](images/etape8.jpg)
![Soudure du buzzer](images/etape9.jpg)

## 9. Inspection et Tests

![Brasures Terminéee](images/etape10.jpg)

- **Contrôle visuel :**

  - Inspectez la carte à l’aide d’une loupe ou d’un microscope pour vérifier la qualité des soudures (absence de ponts, bonne homogénéité des joints).
- **Retouches éventuelles :**
  - Réalisez des retouches manuelles si vous constatez des défauts.
- **Tests fonctionnels :**
  - Alimentez la carte et vérifiez le bon fonctionnement de l’ensemble du circuit (LED, buzzer, connecteur Arduino).
  - Mesurez les tensions et vérifiez la continuité des pistes si nécessaire.
