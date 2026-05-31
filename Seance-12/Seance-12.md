# Gestion des exceptions

Si l'on souhaite ignorer les exceptions, il suffit de le préciser dans la méthode `main()`.

```
	public static void main(String[] args) throws Exception
```

> [!WARNING]
> Cela ne résout pas l'exception !

Pour traiter l'exception et la lever, il faut utiliser `try` et `catch`

```
	try
	
	{
	
		...
	
	}
	
	catch(Exception e) { ... }
```

`try` essaie une instruction. Son bloc teste si une exception existe. `catch` capture l'exception si elle est levée. L'objet `Exception` est utilisé. Il s'agit de la classe mère de toutes les exceptions. Il faut consulter la documentation pour bien cibler l'exception à lever. `e` est la variable correspondant à l'exception capturée. Le bloc `catch` précise ce qu'il faut faire en cas d'erreur.

> [!TIP]
> Il peut exister plusieurs exceptions, donc plusieurs `catch`.

```
	finally
	
	{
	
		...
	
	}
```

`finally` permet de clore le test. Tout ce que contient son bloc sera exécuter que ce soit `try` ou `catch` qui est déclenché.

> [!NOTE]
> Par défaut, `Exception e` gère toutes les exceptions. L'action la plus courante s'il existe une exception, consiste à afficher un message d'erreur :

```
	e.getMessage();
```

Il existe également une méthode permettant de visualiser davantage d'informations sur l'erreur :

```
	e.printStackTrace();
```

Lorsqu'une erreur se produit, un objet est créé : il s'agit d'une instance de classe, elle-même sous-classe de la classe `Exception`. Cet objet représente l'erreur commise. Dans ce cas, on dit que **« l'exception est levée »**.

L'exécution de la méthode est alors interrompue. Si l'exception est capturée (`catch()`), le traitement de l'erreur est déclenchée. À la fin du traitement informatique de l'erreur, la méthode interrompue reprend son exécution.

> [!NOTE]
> Si les bonnes erreurs ne sont pas attrapées, un message d'erreur s'affiche. Même si elles n'en empêchent pas une poursuite de l'exécution du programme, une erreur non levée ralentira considérablement l'exécution (uniquement si un `try` / `catch()` a été mis en place bien entendu.

> [!NOTE]
> La classe `Exception` est la classe la plus générale pour le programmeur, mais elle ne peut être appliquée en toute circonstance.



`throw` permet de créer une exception dans une classe qu'il faudra lever si une routine l'utilise, sinon le code ne sera pas exécuté.

	throw new Exception(IllegalArgumentException("L'âge doit être supérieur à 18 ans."))

Toutefois, de manière plus générale, `throw` est introduit dans une condition.

```
	try { ... } catch(IllegalArgumentException e) { ... }
```

> [!NOTE]
> Il faut créer un paquetage contenant toutes les exceptions.

> [!NOTE]
> `System.err.println(...)` est utilisé pour l'affichage des erreurs à la place de `System.out.println(...)`.



`CheckException` est une exception que l'on **doit** gérer.

`RuntimeException` est une exception que l'on **peut** gérer. Elle apparaît à l'exécution.

	throw new RunTimeException(...);

Exemple : la division par zéro

```
	int a = 5:
	
	int b = 0;
	
	try
	
	{
	
		System.out.println(a/b);
	
	}
	
	catch(ArithmeticException e)
	
	{
	
		System.err.println("La division par zéro est impossible.");
	
	}
```

On peut remplacer `ArithmeticException` par `RuntimeException` ou `Exception`.

`NullPointerException` apparaît lorsqu'on appelle une méthode qui ne référencie rien.
