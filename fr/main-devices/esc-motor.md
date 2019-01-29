# esc-motor

![ESC T-motor drotek](https://drotek.com/wp-content/uploads/2017/01/DSC02089-1-700x258.jpg)

Les **ESC** \(Electronic Speed Controller\) permettent la gestion en vitesse des moteurs selon les ordres du contrôleur de vol. Typiquement le signal de commande utilisé par les ESC est un PWM \(Pulse Width modulation ou Modulation de largeur d’impulsion\) mais certains modèles permettent l’utilisation de signaux **I2C** ou **CAN**.

La Pixhawk 3 Pro dispose de **8 sorties PWM** permettant le pilotage de 8 couples ESC / Moteur.

## HARDWARE

Veuillez connecter chacun de vos ESC PWM sur la sortie « **Main Out** » correspondante. Reportez-vous au diagramme ci-dessous pour l’ordre de vos couples ESC Moteur.

![esc tmotor drotek](https://drotek.com/wp-content/uploads/2017/01/DSC02091-1-700x380.jpg)

![Motors\_Wiring pixhawk by drotek](https://drotek.com/wp-content/uploads/2017/01/Motors_Wiring-700x744.jpg)

Tous les moteurs de couleur bleue doivent être utilisés uniquement avec une hélices CCW. Les moteurs de couleur verte avec les hélices CW.

Pour repérer à quoi ressemble une hélice CCW, veuillez regarder la photo précédente.

Vérifiez aussi le sens des moteurs. **Pour des raisons de sécurité, enlevez les hélices avant toute manipulation!**

Pour inverser le sens d’un moteur, il suffit d’inverser 2 des 3 câbles qui vont du moteur à l’ESC.

