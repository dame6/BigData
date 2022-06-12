# BigData 

POUR pouvoir éxecuter ce code il faut au préalable avoire un environement ou vous avez insataller pyspark ,jupyter notebook, Random et avoir java 1.8

comme je vous l'ai expliquer dans le mail je pour pouvoir texter le code il faut générer un jeux de donnée a laide deu classe Donnée  ensuite faire l'apprentissage du modele avec la classe Traitement et aussi sa sauvegarde 

pui on utilise les fonction de FPGrowth pour pour pouvoir voir les statisque et aussi  pouvoir faire des prévision sur les données de text créer aussi a l'aide de la classe  Donne
comme expliquer ci dessus  nous avons 3 classe :
1.#Classe session pour demarer une nouvelle session spark et #il a une seul fonction débutSession()

2.#classe donné pour la génération de jeux de donnée a étudié et chargement dans une Dataframe  et #il a 2 fonction dataframe() et affiche()
fonction affiche qui permet d'affiché le jeux de donnée
fonction dataframe il permet de charger le jeux de donnée généré en dataframe spark

3.# classe Traitement qui utulise les données générer pour les traité et construire une modéle et #il a 2 fonction modéle() et save_model()
fonction modéle permet de faire l'aprantisage avec FP-Growth il returne un model qu'on va utiliser pour voir les régle association  
save_model est une fonction de Traitement() pour sauvegarder le modéle pour pouvoir l'utiliser une autre fois


Génération de donnée
#génération de données avec la classe Donne(nbrl,nbre,pas,plage) il prend en argument nbrl=nombre de liste dans le jeu de donné ,nbre=nombre d'élément de la premiére liste et peut étre aussi des listes suivant, pas= qui permet de voir la variation du nombre d'élément dans les listes et le plage= qui donne la plage de valeur qu'on peut générer de 0 au valeur désigné

les fonction de FP-Growth dan pyspark
1:freqItemsets= fontion de Fp-growth pour sortir les éléments fréquent de notre model avec le nombre de foi qu'il sorte. 

2: associationRules=la fonction associationRules comme son nom l'indique sort les différents régle d'association dans le model.

3: transform =la fonction transform permet d'appliquer le model sur un jeux de donné de text qu'on peut aussi créer avecla classe Donné() 
