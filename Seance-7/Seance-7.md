# Tableaux

Les tableaux ont un type. Ils sont déclarés par des crochets `[]`.

Exemple d'un tableau de même type :

	int[] tab = new int[taille_du_tableau];
	
`int[]` déclare un tableau d'entiers.

On peut aussi écrire :

	int tab[] = new int[taille_du_tableau];

Exemple d'un tableau (d'entiers) directement initialisé

	init[] tab = {0, 1, 2, 3, ...}

> [!NOTE]
> La notation `int... tab` permet de déclarer plusieurs variables de type `int` et de les récupérer sous la forme d'un tableau.
	
## Parcourir un tableau

	for(int i = 0 ; i < tab.length ; i++)
	
	{
	
		tab[i];
	
	}

> [!WARNING]
> Attention à l'affectation du tableau. Soient deux tableaux `tab1` et `tab2`, écrire `tab1 = tab2` signifie que l'on affecte le pointeur de `tab1` à `tab2`. Dit autrement, modifier `tab1[0]`, par exemple, affecte `tab2[0]`, puisque `tab1` et `tab2` pointent vers le même tableau.

## Copier les valeurs d'un tableau avec une boucle `for`

	for(i = 0 ; tab1.length ; i++)
	
	{
	
		tab2[i] = tab1[i];
	
	}

Les valeurs de `tab1` sont copiées dans `tab2`.

## Comparer deux tableaux

Déclaration préalable de `tab1` et `tab2`

	if(tab1 == tab2)
	
	{
	
		System.out.println("Vrai");
	
	}
	
	else
	
	{
	
		System.out.println("Faux");
	
	}

> [!NOTE]
> Le `if` compare les références des pointeurs. Si les références sont égales, `tab1` et `tab2` sont égaux.

> [!NOTE]
> On fait également une boucle pour comparer les valeurs.
