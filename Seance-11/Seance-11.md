# Lecture au clavier (ou saisie de données)

Pour lire la saisie de données, il faut charger le paquetage `java.io.*`. Deux objets sont possibles : `BufferedRender` et `Scanner`.

## L'objet `BufferedRender`

L'objet `BufferedRender` considère que **toute** saisie est une chaîne de caractères.

Il lit les chaînes de caractères. L'objet est synchrone avec une mémoire tampon de 8129 caractères.

1. Choix du périphérique

```
	InputStreamReader isr = new InputStreamReader(System.in);

```

2. Commande d'appel de la saisie

```
	BufferedReader br = new BufferReader(isr);
```

Les méthodes de l'objet `BufferedReader` sont :

- `read()` pour lire un caractère ;

- `readLine()` pour lire une chaîne de caractères ;

- `skip(n)` pour ignorer `n` caractères.

## L'objet `Scanner`

L'objet `Scanner` permet de lire et de vérifier, de contrôler des données de toute nature. Il est asynchrone avec une mémoire tampon de 1024 caractères.

```
	import java.util.Scanner;

	...
	
	Scanner sc = new Scanner(System.in);
```

Pour lire et vérifier les données, les méthodes de l'objet `Scanner` sont :

- `nextLine()`

- `nextChar()`

- `nextByte()`

- `nextFloat()`

- `nextDouble()`

- `nextInt()`

- `nextBoolean()`

> [!NOTE]
> `Scanner` permet également de lire des fichiers.
