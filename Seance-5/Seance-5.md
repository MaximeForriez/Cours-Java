# Conditions

## Les opérateurs logiques

`&&` : et

`||` : ou (exclusif)

## L'écriture d'une condition avec `if`

Exemple :

	int value = 24;
	
	if(value == 24)

	{

		...

	}

	else if
	
	{
		
		...
		
	}
	
	else
	
	{
	
		...
	
	}
	
`else if` introduit des conditions intermédiaires facultatives.

`else` introduit la condition finale et unique.
	
	
## L'écriture d'une condition avec `switch`

Exemple :

	int value = 100;
	
	switch(option)

	{

		case 1:
		
		...
		
		break;
		
		...
		
		default:
		
		...
		
		break;

	}

`switch` teste un **nombre** ou une **chaîne de caractères** uniquement.

`case` correspond à `if(option == 1)`.

`break` est le point d'arrêt de la condition.

`default` est le cas par défaut.

> [!WARNING]
> L'écriture d'un `switch` n'est pas uniforme dans tous les langages de programmation.
