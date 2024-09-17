# Premier programme

`Java` n'étant pas un langage procédural, le premier programme est par conséquent une classe.

Par convention, chaque fichier contient une classe et le nom du fichier doit porter le nom de classe. Étant donné qu'il s'agit d'une classe unique, il s'agit de la clase contenant la méthode `main()` dans laquelle sera ultérieurement placée toutes les instructions principales appelant les classes. 

	import java.lang.*

	public class MainApp
	{

		public static void main(String[] args)

		{

			System.out.println("Bonjour !");

		}

	}

`import` permet d'avoir accès aux répertoires de classes natives de `Java`. Par défaut, il s'agit de `java.lang.*`.

> [!NOTE]
> `*` permet de télécharger toutes les classes du paquetage `java.lang`.

> [!NOTE]
> Depuis 2016, une partie des paquetages sont redevenus payants.

> [!NOTE]
> Pour avoir la totalité des paquetages, il faut consulter la documentation `Java`.

## Quelques paquetages usuels

`java.applet.*` → classes permettant d'exécuter des applications `Java` sur internet

`java.awt.*` → classes permettant de constituer des interfaces homme-machine

`java.beans.*` → 

`java.io.*` → gestion des entrées et des sorties

`java.lang.*` → classes faisant partie intégrante du langage `Java`

`java.math.*` → 

`java.net.*` → développement des applications réseaux

`java.nio.*` → 

`java.rmi.*` → 

`java.security.*` → 

`java.sql.*` → dialogue avec des bases de données relationnelles

`java.text.*` → 

`java.time.*` → 

`java.util.*` → classes utiles pour le développement d'application `Java`

`java.accessibility.*` → 

`java.crypto.*` → 

`java.imageio.*` → 

`java.net.*` → 

`java.print.*` → 

`java.script.*` → 

`java.swing.*` → complément de `java.awt.*`

`java.tools.*` → 

`java.xml.*` → 

*etc*.

## Première description de la méthode `main()`

`public` : modificateur indiquant que la méthode (ou la variable, ou la classe) est lisible dans toutes les classes

`static` : moyen d'accès, portée de la méthode

`void` : type des variables renvoyées

`main(String[] args)` :

- `String[]` : type de variables

- `args` : signature de la méthode

`System.out.println()` :

- `System.out` est une classe native de `Java`

- `println` est une méthode de la classe `System.out` permettant d'afficher une chaîne de caractères **et** d'aller à la ligne.

`"..."` contient la chaîne de caractères `"Bonjour !"`

## Exécution du code sous `Windows`

Il faut **impérativement** exécuter le code sous un terminal `Windows PowerShell`, à condition d'avoir installé une variable d'environnement dans le `Path`.

1. Ouvrir le bon répertoire. Pour faciliter la lecture, mettre le répertoire sur le `Desktop`

2. Créer les classes en langage machine avec la commande :

	javac MainApp.java

Un fichier `*.class` est créé.

> [!NOTE]
> S'il y a plusieurs fichiers, écrire : `*.java`


3. Exécuter le programme avec la commande :

	java Main App

On exécute toujours la fonction principale.

> [!NOTE] S'il y a un problème, il est possible de stopper l'exécution avec : `ctrl` + `c`.
