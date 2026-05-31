# Polymorphisme

Le **polymorphisme** est utile dans le cadre de la combinaison des classes abstraites et des interfaces. Le programme évoluera plus rapidement. Par exemple, la commande pour instancier les variables est :

	ClasseAbstraite[] var new ClasseAbstraite[...];
	
	var[0] = new ObjetFille1();
	
	var[1] = new ObjetFille2();
	
	var[2] = new ObjetFille3();

On dit qu'on a fait du **surclassement**. L'idée est de créer un tableau d'objets abstraits dans lequel on va stocker les classes concrètes.

	Interface[] elements = new Interface[...]

équivaut à :

	new Interface[new Object1(), ...]

Exemple : classe abstraite et classes concrètes.
