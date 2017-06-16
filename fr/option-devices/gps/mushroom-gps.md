![](https://drotek.com/wp-content/uploads/2017/01/ublox-neo-m8n-gps-hmc5983-compass.jpg "ublox m8n drotek")

Le module GPS « Mushroom » embarque une puce GNSS Ublox **Neo M8N** compatible **GPS, Galileo, GLONASS et BeiDou** ainsi qu’une puce magnétomètre **HMC5983** afin de donner à votre système la capacité de connaitre sa position et son orientation.

Le tout dans un boitier déportable afin d’éviter les interférences.

Vous trouverez plus d'informations sur cette [page](https://drotek.com/shop/fr/drotek-parts/820-module-gps-ublox-neo-m8n-magnetometre-hmc5983-pixhawk-pro.html?search_query=ublox&results=20).

  


### HARDWARE

Connectez votre GPS mushroom sur le connecteur « GPS » de votre Pixhawk.

Le module doit être fixé solidement sur l’appareil, de préférence dans le même sens que votre Pixhawk 3 Pro et surélevé de quelques centimètres par rapport à vos moteurs.

Aucun élément ne doit être placé au-dessus du module « Mushroom » afin de garantir à ce dernier une réception satellite optimale.

  


![](https://drotek.com/wp-content/uploads/2017/01/DSC02039-700x369.jpg "pixhawk ublox gps drotek")

  


### SOFTWARE \(PX4 / QGC\)

Avant de procéder à la configuration, assurez-vous d’avoir bien placé votre module Mushroom comme indiqué dans la section précédente.

Pour configurer votre module GPS mushroom avec QgroundControl, accédez à la fenêtre de configuration « **Sensors** » rubrique « **Compass** » :

![](https://drotek.com/wp-content/uploads/2017/01/Menu_Sensors_QGC.png "Menu\_Sensors\_QGC px4 pixhawk")![](https://drotek.com/wp-content/uploads/2017/01/Compass_FcRotation_QGC.png "Compass\_FcRotation\_QGC px4")

Dans la fenêtre ci-dessus, sélectionnez « Rotation\_None ».

Procédez ensuite à la calibration du compas en effectuant successivement avec votre appareil les rotations indiquées par les images.

![](https://drotek.com/wp-content/uploads/2017/01/Window_Compass_Calib_QGC-700x460.png "qgroundcontrol px4 pixhawk")

  


Pour le GPS « Mushroom » et uniquement pour ce modèle de GPS, une rotation est a paramétrer dans QgroundControl.

Pour cela, accédez à la fenêtre de configuration « **Sensors** » rubrique « **Set Orientation** ».

Dans la fenêtre qui apparait sur la droite, sélectionnez « **ROTATION\_NONE** » dans « Autopilot Orientation » et « **ROTATION\_ROLL\_180** » dans « External Compass Orientation »

Cliquez ensuite sur « OK »

![](https://drotek.com/wp-content/uploads/2017/01/External_Compass_SetOrientation_QGC-250x175.png "External\_Compass\_SetOrientation\_QGC")

  


