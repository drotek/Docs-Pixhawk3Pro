# tiny-module

![alimentation pixhawk drotek](https://drotek.com/wp-content/uploads/2017/01/module-d-alimentation-53v-capteur-couranttension.jpg)

Cette carte permet d'alimenter avec une tension stabilisée l'autopilote **Pixhawk 3 Pro**.

Ce module est aussi capable de mesurer la consommation globale de votre système à l'aide de son capteur à effet Hall. Il est capable d'encaisser jusqu'à 200A en continu en toute sécurité \(selon version\).

La carte est équipée d'une **LED** témoin pour vous avertir en cas de problème d'alimentation.

Vous trouverez plus d'information sur cette [page](https://drotek.com/shop/fr/drotek-parts/806-module-d-alimentation-53v-capteur-couranttension.html).

## HARDWARE

Veuillez connecter le module d'alimentation sur le port "**Power 1**" de la Pixhawk.

![tiny power module PX4 ardupilot](https://drotek.com/wp-content/uploads/2017/01/DSC02053-700x393.jpg)

Pour une redondance, il est possible d'utiliser un deuxième module avec une autre batterie, le tout connecté sur le port "**Power 2**" de la Pixhawk.

Dans ce cas de figure, l'autopilote utilise seulement le premier module pour sa propre alimentation. Par contre, si le premier module venait à griller, l'autopilote switch directement sur le deuxième.

## SOFTWARE \(PX4 with QGC\)

Pour configurer votre module Tiny sous QgroundControl, accédez à la fenêtre de configuration « Power ».

![GGC PX4 pixhawk](https://drotek.com/wp-content/uploads/2017/01/Menu_Power_QGC.png)![GGC PX4 pixhawk](https://drotek.com/wp-content/uploads/2017/01/Window_Power_QGC-700x592.png)

* Number of Cells \(in Series\) : indiquez ici le nombre de cellules de votre batterie lipo, ce paramètre est indiqué sur votre batterie par la mention 3S, 4S ...
* Full Voltage \(per cell\) : laissez le paramètre **4.05** par défaut
* Empty Voltage \(per cell\) : laissez le paramètre **3.40** par défaut
* Voltage divider : **7.65**
* Amps per volt : **37.4**

