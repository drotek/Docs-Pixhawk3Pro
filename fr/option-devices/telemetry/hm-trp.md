![](https://drotek.com/wp-content/uploads/2017/01/radio-telemetry-kit-433-915-mhz.jpg "telemetry hm-trp pixhawk by drotek")

Ce système de télémétrie**Drotek** est conçu comme une radio open source remplaçant les modules Xbee à un prix inférieur, de plus longue portée \(environ**1km**\) avec des performances supérieures. Il est disponible en 433 MHz ou 915 MHz.

Le système fournit un lien**full-duplex**à l'aide des modules HM-TRP de chez HopeRF s'exécutant avec un firmware open source.

Vous trouverez plus d'informations sur cette[page](https://drotek.com/shop/fr/drotek-parts/795-kit-radio-telemetrie-433-915-mhz.html).

  


### HARDWARE

Veuillez connecter une des 2 télémétries sur le port série "**Telem 1**" de la Pixhawk \(voir photo\).

![](https://drotek.com/wp-content/uploads/2017/01/DSC02048.jpg "HM-TRP telemetry pixhawk drotek")

Ensuite il vous reste à connecter l'autre télémétrie à votre**PC** via un câble**USB micro**ou à une**tablette**via un câble** USB OTG. **

![](https://drotek.com/wp-content/uploads/2017/01/Planner-APM-Android-700x382.jpg "telemetrie tablette hm-trp")

  


![](https://drotek.com/wp-content/uploads/2017/01/groundstation-with-MP-700x383.png "hm-trp telemetry 433mhz dropix")

**IMPORTANT**: N'oubliez pas de visser les antennes sur chaque module télémétrie avant de les alimenter sous peine de griller les puces HM-TRP.

  


  


### SOFTWARE \(PX4 / QGC\)

Par défaut, QgroundControl sous le firmware PX4 reconnait automatiquement les modules télémétries car elles ont déjà été configurés en usine par Drotek.

Si notre configuration ne vous convient pas, vous pouvez configurer vos modules de télémétrie à votre guise en utilisant[cette utilitaire.](http://vps.oborne.me/3drradioconfig.zip)

Il suffit de connecter le module au PC via le câble USB et ouvrir le logiciel de configuration.

![](https://drotek.com/wp-content/uploads/2017/01/3DR_Radio_Config-700x536.png "3DR\_Radio\_Config hmtrp drotek")

Vous pouvez modifier les valeurs afin d’augmenter votre portée ou bien de communiquer plus vite.

_**Net ID**: C’est le canal sur lequel va communiquer la radio, les 2 doivent avoir la même valeur._

_**Tx Power**: La puissance décuplée par la radio pour l’émission de données. Peut être augmenté pour augmenter la portée._

_**Air Speed**: la vitesse de croisière des données dans l’air. Peut être réduite pour augmenter la portée._

_**Baud**: Vitesse de communication des télémétries. Peut être diminué pour augmenter la portée._

  


Vous trouverez plus d'informations sur ce[site](http://ardupilot.org/copter/docs/common-configuring-a-telemetry-radio-using-mission-planner.html).

  


  


  


