# Configuration de Python et Jupyter

1. Téléchargement de Python
2. Installation des modules numpy, scipy, matplotlib et pyserie
3. Installation de Jupyter
4. Quelques vérifications
5. Ouverture notebook jupyter
6. Premier notebook python

## 1. Téléchargement de Python
En suivant ce [lien,](https://www.python.org/ftp/python/3.6.4/python-3.6.4-amd64.exe) téléchargez la distribution Python 3.6.4 pour Windows. Ce [lien,](https://www.python.org/ftp/python/3.6.4/python-3.6.4-macosx10.6.pkg) vous permet de télécharger la version pour Mac OS X. Si nécessaire, visitez le site [suivant](https://www.python.org/downloads/release/python-364/) pour une autre version. Une fois l'exécutable téléchargé, lancez-le puis spécifiez une installation pour un seul utilisateur, sélectionnez l'option qui permet d'ajoutez le chemin Python au Path windows avant de cliquer sur "Installer maintenant". En fin d'installation, cliquez sur "Fermer".

## 2. Installation des modules numpy, scipy, matplotlib et pyserial
Pour installer ces modules, il suffit de taper la commande suivante dans une console windows :

    pip3 install numpy scipy matplotlib pyserial
    
## 3. Installation de Jupyter
De la même manière, installez jupyter en tapant cette commande, toujours dans une console windows :

    pip3 install jupyter
    
## 4. Quelques vérifications
Pour vérifier que le noyau Python pour Jupiter a été correctement installé, tapez la commande suivante :

    jupyter kernelspec list
Pour vérifier que les modules numpy, scipy, matplotlib et pyserial sont également installés, tapez :

    pip3 list 

## 5. Ouverture notebook jupyter
Toujours dans cette console tapez, à partir d'un répertoir ou vous avez les droits d'écriture :

    jupyter notebook

**Si vous n'avez pas les droits d'écriture dans le répertoire à partir duquel vous lancez le notebook Jupyter, vous ne pourrez pas contiuner...**

Cette commande ouvre, après quelques secondes, le notebook dans le navigateur par défaut. Pour quitter correctement Jupyter, il faut taper Ctrl+C dans la console à partir de laquelle il a été lancé. 

## 6. Premier notebook python
Dans le navigateur, cliquer sur le bouton new puis Python 3 :

![Python Notebook](newPythonNoteBook.PNG)
