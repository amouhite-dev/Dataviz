*************************** PROJET DE VISUALISATION *************************

*************************** BUT DU PROGRAMME *************************
Le projet consiste a fait une visualisation afin de vérifier les cdps ayant dépasserla limite de temps requis pour la réalisation d'un projet.

*************************** LANCEMENT DU PROGRAMME *************************
/*** Sur JupyterNoteBook ***/
Vérifier que les bibliothèque dans le fichier requirements.txt sont bien installer
Lancer tous simplement le programme depuis l'option Kernel > Restart & Run All

*************************** EXPLICATION DU PROGRAMME ***********************
Le programme au lancement créé un repectoire appelé ALL_HISTOGRAM (le nom peut être changé dans
le fichier excel ConfigExtraction.xlsx), ensuite initialise les variables neccessaire pour le
traitement et la visualisation des données du fichier excel donnée.

Après cette étape appel la fonction ***initialization_of_treatment*** afin de vérifier si avec les
paramètre fourni dans le fichier ***ConfigExtraction*** l'on peut fait le traitement et visualisé les données. Dans le cas échéant il affiche un message(voir code ou lors de l'éxécution avec comme paramètre 
de l'offre 9 office ims), sinon il appele la fonction ***evaluation_date_replace_nan*** qui va créé un nouveau dictionnaire sans valeur nulle, pour etre passé en paramètre à la fonction ***create_dict_cdp_time_do*** qui permettra de créé un dictionnaire(le nom est ***dict_all_cdp_time_do***) lié a chaque cdp(clé) qui auront pour valeur une liste de dictionnaire(contiendra tout les projet lié a eux).

Avec ce dictionnaire l'ont pourra ainsi créé les histogrammes lié a notre étude a savoir:
- liste des cdp avec leur nombre de projet a chacun
- temps emis sur chaque phase d'un projet pour un cdp
- temps totale mis pour la réalisation de chacun de tout ses projets pour un cdp
- temps moyen mis pour la réalisation de tout ses projets
- en terme de pourcentage le nombre de projets hors délai limite ou non ou égale au delai limite


***************************************** FIN *******************************************