# xxl-gps

Le module **GNSS XXL** embarque une puce GNSS Ublox **Neo M8N** compatible **GPS, Galileo, GLONASS et BeiDou** ainsi qu’une puce magnétomètre **LIS3MDL** afin de donner à votre système la capacité de connaitre sa position et son orientation.

Ces modules offrent une meilleur réception satellite que le module GNSS « Mushroom » grâce à leur grande antenne et leur plan de masse plus important.

Vous trouverez plus d'informations sur cette [page](https://drotek.com/shop/fr/u-blox/875-module-gps-ublox-neo-m8n-magnetometre-lis3mdl-xxl.html?live_configurator_token=8746d605a9c04b1e35dffc6d98e0a9e5&id_shop=1&id_employee=1&theme=&theme_font=).

## HARDWARE

Connectez votre GPS sur le connecteur « GPS » de votre Pixhawk.

Le module doit être fixé solidement sur l’appareil, de préférence dans le même sens que votre Pixhawk 3 Pro et surélevé de quelques centimètres par rapport à vos moteurs.

Aucun élément ne doit être placé au-dessus du module afin de garantir à ce dernier une réception satellite optimale.

![xxl GNSS glonass galileo gps u-blox by drotek](https://drotek.com/wp-content/uploads/2017/02/DSC02066-700x312.jpg)

## SOFTWARE \(PX4 / QGC\)

Avant de procéder à la configuration, assurez-vous d’avoir bien placé votre module comme indiqué dans la section précédente.

Pour configurer votre module GPS mushroom avec QgroundControl, accédez à la fenêtre de configuration « **Sensors** » rubrique « **Compass** » :

![Menu\_Sensors\_QGC px4 pixhawk](https://drotek.com/wp-content/uploads/2017/01/Menu_Sensors_QGC.png)![Compass\_FcRotation\_QGC px4](https://drotek.com/wp-content/uploads/2017/01/Compass_FcRotation_QGC.png)

Dans la fenêtre ci-dessus, sélectionnez « Rotation\_None ».

Procédez ensuite à la calibration du compas en effectuant successivement avec votre appareil les rotations indiquées par les images.

![qgroundcontrol px4 pixhawk](https://drotek.com/wp-content/uploads/2017/01/Window_Compass_Calib_QGC-700x460.png)
