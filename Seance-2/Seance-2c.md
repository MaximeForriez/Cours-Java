# Gestion des importations

- L'importation préalable d'une ressource de `Java` permet d'éviter d'alourdir le code. Il faut bien comprendre :

	import java.util.*;
	
	public class ...

	{
	
		...
		
		Scanner
		
		...
	
	}

équivaut strictement à :

	import java.util.*;
	
	public class ...

	{
	
		...
		
		java.util.Scanner
		
		...
	
	}

C'est ce que l'on appelle l'**importation statique**.

- Pour aller plus loin, l'importation statique permet d'importer tous les champs et toutes les méthodes statiques d'une classe. Par exemple, `import static java.lang.Math.abs;`permet d'utiliser `abs()` au lieu de `Math.abs()`

Plus généralement, on peut écrire : `import static java.lang.Math.*`

> [!NOTE]
> Cette possibilité est peu utilisée par les programmeurs, car, si une fonction `abs()` est créée, quelqu'un qui reprendrait le code, ne saurait pas si la fonction est `abs()` ou `Math.abs()`
