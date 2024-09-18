# Encapsulation des données sous `Java`

## Les accesseurs

Les **accesseurs** sont des méthodes qui permettent :

1. l'accès (ou la lecture). `getters` donnent l'accès à un attribut.

2. la modification (ou l'écriture). `setters` modifient un attribut.

Ils prennent tout leur sens dans le cadre du principe informatique d'encapsulation : **les classes extérieures n'ont pas accès aux attributs d'une classe**. De fait, si l'on peut modifier une variable, il est préférable de construire deux méthodes.

Exemple.

	private expirationAnnee;
	
	//Constructeur à définir
	
	//Getter
	
	public int getExpirationAnnee()

	{

		return this.expirationAnnee;
	
	}
	
	//Setter
	
	public void setExpirationAnnee(int expiration)
	
	{
	
		return this.expirationAnnee = expiration;
	
	}

> [!NOTE]
> Les accesseurs permettent de modifier une fois le code et une seule, et d'en obtenir des répercussions partout dans le programme.

Les accesseurs permettent de respecter le principe informatique de l'encapsulation des variables. Cela donne un contrôle de l'accès aux attributs.

## Les variables de classe

Les **variables de classe** n'appartiennent à aucune instance particulière. Ce sont des variables partagées.

Exemple.

	private static int nombreEnregistrement = 5;
	
Le modificateur `static` indique qu'il s'agit d'une variable de classe.

Elles sont communes à toutes les instances créées. Si l'une la ou les modifie, l'autre la ou les récupère avec sa modification. La variable n'est pas réinitialisée.

> [!NOTE]
> Il est possible de construire des **méthodes de classe** obéissant aux mêmes principes. Cela peut être utile pour créer des accesseurs par exemple.

## Variable statique *vs*. variable d'instance

La **variable de classe** (V.C.) (ou statique) ne dépend que de la classe, par exemple, un compteur d'objets créés par la classe.

La **variable d'instance** dépend de l'objet créé.

Dans le cas d'une variable de classe, les objets créés par cette classe utiliseront cette même variable ; elle sera partagée.

> [!NOTE]
> L'appel d'une variable de classe dans une autre classe s'effectue bien entendu par un `getter` avec une méthode de classe. Elle est appelée par `nomClasse.nomVariable()`.


























