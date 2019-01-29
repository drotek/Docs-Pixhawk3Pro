# sirius

![Sirius M8N GPS](https://drotek.com/wp-content/uploads/2017/05/Sirius_rendu_oblique2.png)

Le module GPS Sirius comprend une puce u-blox **Neo M8N** pour une localisation précise et un magnétomètre **LIS3MDL** pour ajouter un capteur d'orientation à votre système. Ce modèle possède une antenne active qui lui permet de délivrer des performances de haut niveau et une compatibilité accrue avec la constellation de satellites Galileo.

Un lien vers la page produit sera présenté dés que le module GPS Sirius sera disponible au public!

## HARDWARE

Branchez le cable du module Sirius au port GPS de votre Pixhawk 3 PRO. Il est nécéssaire que le GPS soit bien fixé à votre véhicule, et de préférence dans dans la même direction que votre Pixhawk 3 PRO.

Veillez à n'avoir aucun autre élément électromagnétique placé plus haut que votre GPS dans votre installation, et à ce que le GPS Sirius soit situé quelques centimètres au-dessus des moteurs pour éviter au maximum les interférences.

## SOFTWARE \(PX4 / QGC\)

Avant de procéder à la configuration, veillez à ce que le GPS Sirius soit bien installé comme décrit plus haut.

Pour le configurer, ouvrez le logiciel, connectez vous à votre autopilote, puis rendez-vous dans la partie `Compass` dans le menu `Sensors`.

![Menu\_Sensors\_QGC px4 pixhawk](https://drotek.com/wp-content/uploads/2017/01/Menu_Sensors_QGC.png)![Compass\_FcRotation\_QGC px4](https://drotek.com/wp-content/uploads/2017/01/Compass_FcRotation_QGC.png)

Dans la fenêtre ci-dessus, sélectionnez `Rotation_None`. Ensuite, calibrez le magnétomètre en réalisant les opérations décrites par le logiciel, faisant faire les rotations requises à votre véhicule.

![qgroundcontrol px4 pixhawk](https://drotek.com/wp-content/uploads/2017/01/Window_Compass_Calib_QGC-700x460.png)

Le magnétomètre est à présent prêt à être utilisé.

