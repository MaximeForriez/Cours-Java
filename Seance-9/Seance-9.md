# Chaînes de caractères

L'objet `String` instancie un type de classe `String`.

	String s = "...";

équivaut à :

	String s = new String("...");

Cela signifie que la classe `String` est **immuable**, c'est-à-dire que son contenu est non modifiable. Toute nouvelle affectation **crée** une nouvelle chaîne de caractères. Il est très important de comprendre qu'elle ne modifie pas la variable comme une variable ordinaire. Cela affecte le traitement en mémoire : modifier trop souvent une chaîne de caractères rend la mémoire plus lente. Cela affecte la performance des calculs. Par exemple, les chaînes de caractères se concaténant, elles ne s'ajoutent pas. La concatétation est de fait une opération lourde.

## Les méthodes `String`

`String` étant un objet, il possède des méthodes.

- `concat()`. L'opérateur de la concaténation permet d'avoir une compilation optimale par rapport à l'opérateur `+`.

- `length()` fournit la taille de la chaîne de caractères.

- `toUpperCase()` pemet de tout mettre en majuscule.

- `toLowerCase()` permet de tout mettre en minuscule.

- `trim()` retire tous les espaces d'une chaîne de caractères.

- `replace()` remplace un élément d'une chaîne de caractères par un autre.

- `charAt()` donne la position dans la chaîne de caractères (0, 1, ..., *n* - 1). La chaîne de caractères n'est par conséquent pas un tableau ordinaire.

- `substring()` extrait une sous-chaîne dans une chaîne de caractères (position, nombre de caractères à récupérer, *etc*.).

- `toString()` retourne la chaîne de caractères associée.

Il existe de nombreuses méthodes pour comparer deux chaînes de caractères.

- `equals()` teste l'égalité entre deux chaînes de caractères.

	s1.equals(s2);

- `compareTo()` teste la différence des caractères à partir de leur nombre ASCII.

	- Si le résultat est nul, les chaînes de caractères sont égales.

- `isEmpty()` teste si la chaîne de caractères est nulle.

- `toString()`

- `toCharArray()`

Si on charge le paquetage suivant : `import java.util.StringToKenizer;`. La méthode permet de mettre à la ligne les éléments séparés.

	StringToKenizer st = new StringToKenizer(s, "délimitateur_choisi")

## Les objets `Builder` et `StringBuffer`

`StringBuilder` et `StringBuffer` sont des **objets muables** qui sont des méthodes communes.

- `length()` donne le nombre de caractères.

- `capacity()` donne l'espace disponible dans la mémoire pour une chaîne de caractères. Si la chaîne de caractères est vide, elle vaut `16`.

- `append(...+...+)` ajoute en fin de chaîne de caractères. 

- `insert(0, "...")` ajoute une chaîne de caractères en début de chaîne. 

- `insert(position, "...")` insert une chaîne de caractères dans une chaîne de caractères.

Le `thread.safe` est une propriété associée au fait que le code est capable de fonctionner correctement lorsqu'il est exécuté simultanément au sein du même espace d'adressage par plusieurs flux.

Caractéristiques de `StringBuilder sb = new StringBuilder();`

- asynchrone

- 1 `Thread-safe`

Caractéristiques de `StringBuffer sb = new StringBuffer();`

- synchrone

- plusieurs `Thread-safe`

## Les autres fonctions

`String.valueOf(...)` convertit en `String`.

`.indexOf("...")` retourne la position du caractère dans la chaîne.

`.substring(n1, n2)` retourne l'extrait de la chaîne de caractères commençant par `n1` et finissant par `n2 - 1`.

`.startsWidth("...")` retourne `true` ou `false` si la chaîne de caractères correspond au début de la chaîne globale.
