# Python and Jupyter configuration

1. Download Python
2. Install numpy, scipy, matplotlib and pyserial modules
3. Install Jupyter
4. Some checking
5. Open Jupyter Notebook
6. First Python Notebook

## 1. Download Python
En suivant ce [lien,](https://www.python.org/ftp/python/3.6.4/python-3.6.4-amd64.exe) téléchargez la distribution Python 3.6.4 pour Windows. Ce [lien,](https://www.python.org/ftp/python/3.6.4/python-3.6.4-macosx10.6.pkg) vous permet de télécharger la version pour Mac OS X. Si nécessaire, visitez le site [suivant](https://www.python.org/downloads/release/python-364/) pour une autre version. Une fois l'exécutable téléchargé, lancez-le puis spécifiez une installation pour un seul utilisateur, sélectionnez l'option qui permet d'ajouter le chemin Python au Path windows avant de cliquer sur "Installer maintenant". En fin d'installation, cliquez sur "Fermer". Il peut être nécessaire de redémarrer pour que les chemins d'accès aux différentes commandes de Python soient pris en compte.

## 2. Install numpy, scipy, matplotlib and pyserial modules
Pour installer ces modules, il suffit de taper la commande suivante dans un terminal Windows, MacOSX ou Linux :

    pip3 install numpy scipy matplotlib pyserial
    
## 3. Install Jupyter
De la même manière, installez Jupyter en tapant cette commande, toujours dans un terminal :

    pip3 install jupyter
    
## 4. Some checking
Pour vérifier que le noyau Python pour Jupiter a été correctement installé, tapez la commande suivante :

    jupyter kernelspec list
Pour vérifier que les modules numpy, scipy, matplotlib, pyserial et jupyter sont également installés, tapez :

    pip3 list 

## 5. Open Jupyter Notebook
Toujours dans ce terminal tapez, à partir d'un répertoir où vous avez les droits d'écriture :

    jupyter notebook

**Si vous n'avez pas les droits d'écriture dans le répertoire à partir duquel vous lancez le notebook Jupyter, vous ne pourrez pas contiuner...**

Cette commande ouvre le notebook dans le navigateur par défaut. Pour quitter correctement Jupyter, il faut taper Ctrl+C dans la console à partir de laquelle il a été lancé. 

## 6. First Python Notebook
Dans le navigateur, cliquer sur le bouton new puis Python 3 :

![Python Notebook](newPythonNoteBook.PNG)
