# Variables

Le `Java` est un **langage typé**. On doit par conséquent définir le type de variables lors de la déclaration des variables. Cette déclaration doit être précédée d'un modificateur.

Il existe trois sotes de variables :

- **les variables d'instance** ;

- **les variable de classe** ;

- **les variables locales aux méthodes**.

## Règles pour nommer les variables

Le nom ne doit pas contenir de caractères spéciaux, ni d'espaces (que l'on remplace généralement par un *underscore*.

Le nom commence soit par une lettre, sont par un *underscore*.

Il existe plusieurs conventions pour nommer les variables :

- le `camelCase` : `uneVariable` (en `Java`) ;

- le `PascalCase` : `UneVariable` (classe en `Java`) ; 

- le `snakeCase` : `une_variable`.

- *etc*.

## Affectation des variables

	private int ageUtilisateur = 0;

`int` : type (déclaration de la variable)

`= 0` : affectation. Il est conseillé de mettre une affectation par défaut. On dit que la variable est initialisée.

> [!NOTE]
> On ne déclare qu'une fois une variable.

> [!NOTE]
> **Les variables son supprimées à chaque fin de méthode**. Il n'est par conséquent pas nécessaire de mettre le modificateur.

Pour fermer une variable :

	nomVariable.close()

Pour afficher une variable :

	System.out.println(ageUtilisateur);

> [!NOTE]
> Par défaut, toute variable numérique est transformée en texte par cette méthode.

> [!NOTE]
> La variable dépend du **contexte**.

## Variables d'instance

Les variables d'instance servent à définir les propriétés qui structurent une classe.

Elles sont initialisées par défaut à `0` ou `null` selon le type de ces variables.

Elles prennent des valeurs :

- **soit dans le cadre de l'exécution du constructeur de la classe** ;

- **soit lors de l'exécution d'une méthode**.

Leur accessibilité est définie par les **modificateurs**.

Leur durée de vie correspondent à celle de l'objet.

Elles doivent avoir un type.

Par convention, elles se déclarent soit en début de classe, soit en fin de la classe.

## Variables de classe

Les variables de classes sont définies par le modificateur `static`.

Elles sont mises en place dès que la classe est chargée, seront même que soit créée une instance de classe.

Tous les objets de la classe créés plus tard vont partager les informations qui figurent dans ces variables.

## Variables locales aux méthodes

Les variables locales sont celles que l'on définit habituellement comme des variables locales aux fonctions.

Elles doivent être initialisées dès leur définition, définition pouvant intervenir à n'importe quel moment dans le code de la fonction.

Elles doivent avoir un type.

## Conversion des variables

Exemple :

	int b = (int) 7.8

`(int)` convertit le nombre qui suit, un `double`, en entier `int`. Cela prend en compte la partie entière. Cela équivaut à `Integer.valueOf(7.8)`.


