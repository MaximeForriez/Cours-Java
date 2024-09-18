# Construction d'une classe

Une classe est une idée, un concept, une entité.

Une classe a un modificateur.

Une classe correspond par convention à un fichier.

Le point d'entrée est la méthode `main()` dans le fichier principal. Toutes les autres classes ont besoin d'un **constructeur**.

## Déclaration d'un objet

Un objet se déclaire et s'initialise comme une variable ordinaire.

En général, les objets sont déclarés dans la classe principale.

La création d'un objet présuppose que la classe le créant existe. La classe correspond à un modèle, un plan. La création d'un objet est une **instanciation de classe**, il s'agit de donner vie au modèle, à l'objet.

	Objet variable = new Objet();

S'il existe des paramètres dans la classe, il faut les initialiser :

	Objet variable = new Object("nom", age);

**Les objets sont responsables de leur état**.

## L'objet `this`

`this` fait référence à l'objet créé par la classe. Il renvoie à l'instance en cours. C'est l'objet courant, la classe en cours d'exécution.

`this` permet de faire un code générique s'il y a plusieurs objets qui utilisent la même méthode.

`this` est utile dans le cas où le code utilise un même nom de variable.

Exemple :

	class Classe1
	
	{
	
		private String title;
		
		...
		
		public Classe1(String title)
		
		{
			
			...
			
			this title = title;
			
			...
			
		}
	
	}

`Classe1()` est le **constructeur**. Il porte le nom de la classe ; c'est une fonction qui ne retourne rien et qui est dotée d'une syntaxe particulière.

Le premier `private String title` déclare et initialise la variable.

Le second `String title` dans `public Classe1(String title)` déclare une variable locale à la méthode.

Dans la méthode `public Classe1(String title)`, `this.title` fait référence au premier `String title`, tandis que le second fait référence à la variable locale de la méthode.

`this` est utilisé différemment pour les attributs et les méthodes d'instance.

## Les attributs

Les **attributs** sont les variables appartenant à une classe. Ils se placent avant ou après les méthodes de la classe. Ils se déclarent avec le modificateur `private`.

Exemple :

	private String variable1;
	
	private String variable2;

	public Objet(String nom, int age)
	
	{
	
		this.variable1 = nom;
		
		this.variable2 = age;

	}

Dans la méthode `public Objet(String nom, int age)`, les variables `nom` et `age` constituent des variables d'entrée permettant d'exécuter la classe lorsqu'elle est appelée.

Dans la classe principale, dans la fonction `main()`, on pourra écrire :

	Objet variable = new Objet("nom", age);

Cette ligne crée un objet avec les paramètres souhaités dans l'ordre du constructeur de la classe instanciée.

> [!NOTE]
> Par défaut, les variables sont `public`.

> [!NOTE]
> `String variable = "nom";` équivaut à :
>	`String variable = new String("nom");`
> car `String` est un objet.

## Les méthodes

Une **méthode** est une fonction appartenant à une classe. Elle permet d'éviter les répétitions de code.

La classe principale contient la méthode `main()`.

1. Elle est `static`, car la classe principale n'est pas « instanciable ». Elle est ancrée, c'est-à-dire non dynamique.

2. Elle est déclarée avec `void`, car la fonction ne renvoie à rien.

Toute autre méthode contenue dans la classe principale doit être : `public`, `static` et `void`.

Une méthode doit appliquer une fonction à la fois.

La notion de retour `return` permet de renvoyer une information lorsque l'on appelle la méthode.

Exemple :

	public static int getNumberTwo()

	{

		return 2;

	}

Le `int` dans `public static int getNumberTwo()` déclare le type de retour attendu par la fonction. `return 2` retourne bien un entier.

> [!NOTE]
> L'instruction de retour arrête la méthode avec ou sans renvoi d'une information.

> [!WARNING]
> Il faut un `return` par méthode, sauf si l'on écrit des conditions.

`return` permet de passer les valeurs d'une variable locale d'une méthode à une autre.

Les paramètres d'une méthode se déclarent dès le début. La variable a pour « durée de vie » la méthode. Dit autrement, si les méthodes sont conçues, il est inutile de supprimer la variable.

	public static void say(String msg)
	
	{
	
		System.out.println(msg);
	
	}

Dans `main()`, il suffit d'écrire `say("Hello")` pour appeler la fonction.

Dans `public static void say(String msg)`, `msg` est un **paramètre**, tandis que l'appel dans `main()` de `say("Hello")`, `"Hello"` est un **argument**.

On ne peut pas avoir de valeurs optionnelles par défaut en `Java`. Dit autrement, si on déclare plusieurs paramètres, l'utilisation de la fonction doit contenir **tous** les paramètres déclarés. Pour créer des paramètres par défaut, il faut faire ce que l'on appelle de la **surcharge de méthodes**.

## La surcharge des méthodes

La surcharge de méthodes consiste à créer plusieurs méthodes du même nom, mais avec une déclaration de paramètres différente. Cela est suffisant pour que `Java` considère qu'il s'agit de méthodes différentes.

Exemple : la fonction somme `sum`

	public static int sum(int a, int b)

	{
	
		return a + b;
	
	}

	public static float sum(float a, float b)
	
	{
	
		return a + b;
	
	}

La surcharge de méthodes est idéale pour des méthodes avec des types de variables différentes.

## Remarque

Il est tout à fait possible d'appeler un objet dans sa classe propre ; là où se localise son propre constructeur. L'objet créé doit juste se situer dans une autre méthode.
