# Opérateurs

## L'opérateur d'affectation

	=

## L'opérateur de concaténation

	+
	
> [!NOTE]
> Cela sert à assembler les chaînes de caractères.

## Les opérateurs arithmétiques

`+` : addition

`-` : soustraction

`*` : multiplication

`/` : division

`%` : modulo

`(...)` : parenthèses

## Les opérateurs de comparaison

`==` : égalité

> [!WARNING]
>	24 == "24"
> Réponse : `True`

`===` : identité

> [!WARNING]
>	24 == "24"
> Réponse : `False`

`!=` : différent de

`<` : strictement inférieur

`<=` : inférieur ou égal

`>` : strictement supérieur

`>=` : supérieur ou égal

## Le signe d'un nombre

`+` : positif

`-` : négatif

## L'opérateur de la négation

`!`

## Les opérateurs de vérité

`true` : vrai

`false` : faux

## La crémentation

`+=` avec par exemple `A += X` équivaut à :

	A = ...
	
	A = A + X

`-=` avec par exemple `A -= X` équivaut à :

	A = ...
	
	A = A - X

`*=` avec par exemple `A *= X` équivaut à :

	A = ...
	
	A = A * X

`/=` avec par exemple `A /= X` équivaut à :

	A = ...
	
	A = A / X

`%=` avec par exemple `A %= X` équivaut à :

	A = ...
	
	A = A % X

> [!NOTE]
> Tout le paragraphe est écrit en pseudo-code pour comprendre le processus, et non en code `Java`.
	
## L'incrémentation

`++` avec par exemple `A++` équivaut à :

	A = ...
	
	A = A + 1

> [!NOTE]
> Tout le paragraphe est écrit en pseudo-code pour comprendre le processus, et non en code `Java`.

## La décrémentation

`--` avec par exemple `A--` équivaut à :

	A = ...
	
	A = A - 1

> [!NOTE]
> Tout le paragraphe est écrit en pseudo-code pour comprendre le processus, et non en code `Java`.

## L'ordre de la crémentation

`A++` est une **post-incrémentation**.

`A--` est une **post-décrémentation**.

`++A` est une **pré-incrémentation**.

`--A` est une **pré-décrémentation**.

L'ordre est super important.

La post-crémentation suit le processus suivant :

1. affectation de la variable ;

2. crémentation de la variable.

La pré-crémentation suit le processus suivant :

1. crémentation de la variable ;

2. affectation de la variable.

> [!NOTE]
> La pré-crémentation est utilisée :
> - pour des données complexes
> - pour affecter une variable `± 1`.
