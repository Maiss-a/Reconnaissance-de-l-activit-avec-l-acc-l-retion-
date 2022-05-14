# RECONNAISSANCE DE L'ACTIVITE AVEC L'ACCELERATION
Tout au long du projet on va utiliser les bibiotheques suivant:

Pandas:pour importer les tables exels

Numpy:Pour manipuler le data set (fonct sur les matrices)

sklearn:pour les fonctions du machine Learning 

## 1- collect des données 
on utilise le data set suivant :https://archive.ics.uci.edu/ml/datasets/Activity+Recognition+from+Single+Chest-Mounted+Accelerometer
avec 15 individus chaqu'un performe 7 activitées toutes ces activitées dans un fichiers excel 
pour faciliter le travail d'extraction on a met chaque activitée dans un fichier avec 10 feuilles (en suprimmant 5 indiv qui ont des courbes insignificatifs)
après l'observation des courbes on a annuler l'activitée (standing walking and going up-down stair car elle n'a pas des caractéristique commun dans ces courbes 
## 2-praitraitement:
après le netoyage de données on a les équilibré en prenat pour chaque individu 988 instance car la fréquence est 52 donc elles représente 19 secondes pour chaque activitée et en les mettant dans un seul fichier 
https://github.com/Maiss-a/Reconnaissance-de-l-activit-avec-l-acc-l-retion-/blob/main/balance%20and%20concat%20data.ipynb

dans cette phase on utilise souvent le module preprocessing de sklearn "Sklearn.preprocessing" qui contient des classes appelées "transformateurs" et des fonctions mathématiques
nous traitons l'ensemble de nos données de façon cohérente,en transformant toute donnée future de la meme manière qu'on été transformé les données qu'on est servit à l'entrainement de la machine( grace aux transformateur et estimateur).

   •nettoyage et encodage:avant de démarer il fallait netoyer les données et encoder la colonne de classe (qui est qualitatif), mais le data set que j'ai trouvé est encodé et j'ai analysé les valeurs manquantes et rien trouver donc je croix qu'elle est netoyé aussi.
   
   •la normalisation:on choisit la technique de standarisation  en utilisant le transformateurs Standarscaler() 
    Standardisation
Consiste à centrer la variable sur zéro et normaliser la variance des données à 1. 
Pour normaliser l'ensemble de données, il vous suffit de soustraire chaque point 
de données de la moyenne du point de données et diviser le résultat par l’écart 
type des données.
   •dataset Split :on séparé le data set en 80% train_set et 20% test_set
   
   https://github.com/Maiss-a/Reconnaissance-de-l-activit-avec-l-acc-l-retion-/blob/main/CNN.ipynb
   
## 3- Le modèle CNN 
on ignore l'étape de l'extraction des caractéristique car le CNN la fait seul
on a changer le dimmensions de notre données pour utiliser un réseau de convolution avec 2dimension 
après avoir un overfitting dans notre modèle les solution utilisé sont :
augmenter l'apprentissage avec l'augmentation de nombre d'epochs
parametre tunning: régler le nombre de neurones , optimizer
cross validaton: utiliser K-fold cross validation 
