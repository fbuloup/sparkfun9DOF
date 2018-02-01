# Guide d'installation du Sparkfun 9DOF sous Mac OSX

C'est un peu plus simple sur OSX que sous Windows...

Les étapes sont les suivantes (pas besoin d'être admin [à vérifier]) :

1. Connection de l'IMU sur un port USB
2. Recherche du fichier tty associé à l'IMU
3. Utilisation de la commande screen

## 1. Connection de l'IMU sur un port USB
Connecter le module sur un port USB de l'ordinateur et attendre qu'il ait fini l'installation partielle.

## 2. Recherche du fichier tty associé à l'IMU
Dans un terminal, taper la commande suivante :

    ls /dev/tty.*
Vous devriez obtenir une réponse du type suivant :

    /dev/tty.Bluetooth-Incoming-Port	/dev/tty.usbmodem1411
L'IMU est attaché à /dev/tty.usbmodem1411

## 3. Utilisation de la commande screen
Lancer dans ce terminal la commande suivante :

    screen /dev/tty.usbmodem1411 115200
Si la petite led bleu du module clignote, vous devriez voir le flux de données. 

    (SPACE) – Pause/resume serial port printing
    a – Turn accelerometer readings on or off
    g – Turn gyroscope readings on or off
    m – Turn magnetometer readings on or off
    r – Adjust log rate in 10Hz increments between 1-100Hz (1, 10, 20, …, 100)
    A – Adjust accelerometer full-scale range. Cycles between ± 2, 4, 8, and 16g.
    G – Adjust gyroscope full-scale range. Cycles between ± 250, 500, 1000, 2000 dps.

