## Configuration de l'affichage de Matplotlib
Pour un affichage des graphiques dans le notebook de Jupyter qui fonctionne en export PDF si latex est installé dans le système, 
il faut ajouter la ligne suivante avant tout affichage :

    %matplotlib inline

Pour avoir des graphiques interactifs :

    %matplotlib nbagg
ou

    %matplotlib notebook
Mais dans ce cas, l'export PDF ne comportera plus les graphiques (mode non supporté par Latex).
