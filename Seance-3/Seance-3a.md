# Type de variables

| Type primitif | Type « Objet » associé ou Enveloppeur | Mémoire vive | Limite |
| :-: | :-: | :-: |:-: |
| boolean | Boolean | 1 octet | true (1) ou false (0) |
| byte | Byte | 1 octet | [-128,127] |
| char | Character | 2 octets | Unicode ! 65 536 caractères |
| short | Short | 2 octets | [-32 768, 32 767] |
| int | Integer | 4 octets | [-2 147 483 648, 2 147 483 647] |
| long | Long | 8 octets | [-2<sup>63</sup>, 2<sup>63</sup> - 1] |
| float | Float | 4 octets | [1,4 × 10<sup>-45</sup>, 3,4 × 10<sup>38</sup>] |
| double | Double | 8octets | [4,9 × 10<sup>-324</sup>, 1,7 × 10<sup>308</sup>] |
|  | String |  |  |

> [!NOTE]
> L'allocation de la mémoire vive est importante dans le cadre d'un système embarqué.

> [!NOTE]
> La chaîne de caractères `String` est un objet.

On distingue deux types de variables :

- **les variables ordinaires** ;

- **les variables « classe »** (les objets).

> [!NOTE]
> `void` ne retourne rien au niveau des méthodes.
