# Guide d'installation du Sparkfun 9DOF sous Windows

[Lien vers le document qui a servi de base.](https://learn.sparkfun.com/tutorials/9dof-razor-imu-m0-hookup-guide?_ga=2.99420060.326620079.1517431239-364404356.1517431239)

Les étapes sous windows (pas besoin d'être admin [a vérifier]) :

1. Connection de l'IMU sur un port USB
2. Installation du driver
3. Téléchargement du Tera Term's et permiers tests

## 1. Connection de l'IMU sur un port USB
Connecter le module sur un port USB de l'ordinateur et attendre qu'il ait fini l'installation partielle.

## 2. Installation du driver
Terminer cette installation en suivant ce [lien vers le document qui a servi de base.](https://learn.sparkfun.com/tutorials/9dof-razor-imu-m0-hookup-guide?_ga=2.99420060.326620079.1517431239-364404356.1517431239) Localiser la portion du document qui présente l'installation du driver sous Windows, comme le montre l'image suivante :

![Windows driver](WindowsDriver.PNG)

Puis cliquer sur "DOWNLOAD THE SPARKFUN SAMD21 WINDOWS DRIVER" pour télécharger le driver. Toujours au même endroit, cliquer sur le lien "instructions in the SAMD21 Breakout hookup guide" pour suivre les instructions d'installation du driver.

## 3. Téléchargement du Tera Term's et permiers tests
Télécharger le logiciel en suivant ce [lien.](https://osdn.net/projects/ttssh2/downloads/68719/teraterm-4.97.exe/) Lancer Tera Term's et choisir le bouton radio Serial et cliquer sur OK. Les données dervraient s'afficher en temps réel dans le terminal. Un appui sur la barre d'espace permet de mettre en pause ou de reprendre l'acquisition des données. Utiliser, toujours dans ce terminal, les commandes suivantes pour modifier la configuration de l'acquisition :

    (SPACE) – Pause/resume serial port printing
    a – Turn accelerometer readings on or off
    g – Turn gyroscope readings on or off
    m – Turn magnetometer readings on or off
    r – Adjust log rate in 10Hz increments between 1-100Hz (1, 10, 20, …, 100)
    A – Adjust accelerometer full-scale range. Cycles between ± 2, 4, 8, and 16g.
    G – Adjust gyroscope full-scale range. Cycles between ± 250, 500, 1000, 2000 dps.

