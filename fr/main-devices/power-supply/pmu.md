#Power Management Unit module

<p align="center">
  <img src="./images/pmu3d.png?raw=true" alt="PMU 3D Model"/>
</p>


Drotek a créé une nouvelle unité de gestion de l'alimentation, conçue pour fournir une alimentation électrique solide et fiable et plug-and-play avec la Pixhawk 3 PRO.

Vous trouverez plus d'information sur cette [page](https://drotek.gitbooks.io/power-management-unit-user-guide/).


### SOFTWARE

Pour configurer votre module Tiny sous QgroundControl, accédez à la fenêtre de configuration « Power ».

![](https://drotek.com/wp-content/uploads/2017/01/Menu_Power_QGC.png "GGC PX4 pixhawk")![](https://drotek.com/wp-content/uploads/2017/01/Window_Power_QGC-700x592.png "GGC PX4 pixhawk")

* Number of Cells \(in Series\): indiquez ici le nombre de cellules de votre batterie lipo, ce paramètre est indiqué sur votre batterie par la mention 3S, 4S ...

* Full Voltage \(per cell\) : laissez le paramètre
  **4.05**
  par défaut

* Empty Voltage \(per cell\) : laissez le paramètre
  **3.40**
  par défaut
  
* Voltage divider: `15.9`

* Amps per volt: `37.51`





