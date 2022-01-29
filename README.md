# RECONNAISSANCE DE L'ACTIVITE AVEC L'ACCELERATION
Tout au long du projet on va utiliser les bibiotheques suivant:

Pandas:pour importer les tables exels

Numpy:Pour manipuler le data set (fonct sur les matrices)

sklearn:pour les fonctions du machine Learning 


1-praitraitement: dans cette phase on utilise souvent le module preprocessing de sklearn "Sklearn.preprocessing" qui contient des classes appelées "transformateurs" et des fonctions mathématiques
nous traitons l'ensemble de nos données de façon cohérente,en transformant toute donnée future de la meme manière qu'on été transformé les données qu'on est servit à l'entrainement de la machine( grace aux transformateur et estimateur).

   •nettoyage et encodage:avant de démarer il fallait netoyer les données et encoder la colonne de classe (qui est qualitatif), mais le data set que j'ai trouvé est encodé et j'ai analysé les valeurs manquantes et rien trouver donc je croix qu'elle est netoyé aussi.
   
   •la normalisation:on choisit la technique de standarisation mentionné dans le résumé en utilisant le transformateurs Standarscaler() 
   
   •dataset Split :on séparé le data set en 80% train_set et 20% test_set
   
 NB: j'ai fait le traitement sur un seul fichier du data set (parmi les 14 fich exels) pour vous donner un exemple et manipuler les autres après avoir vos remarques  

questions à poser :

1.quand  les valeurs abérrantes (outliers) peuvent poser des problème durant l'apprentissage? car j'ai pas trouver une réponse exacte pour avoir la decision de les supprimer ou non? 

2.est-ce obligatoire d'équilibrer les données dans mon cas ? --voir derniere ligne de code qui visualise les données que j'ai pensé qu'ils son déquilibrées


