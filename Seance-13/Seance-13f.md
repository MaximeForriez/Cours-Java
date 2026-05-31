# Égalité des objets

Deux objets de la même classe sont distincts ou ne le sont pas.

Deux objets sont **distincts** s'ils ne partagent aucune variable, ni la variable qui référence chaque objet, ni les variables d'instance qui structurent chaque objet (les propriétés de chaque objet).

Deux objets sont **semblables** si les valeurs de leurs variables d'instance (propriétés) sont égales entre elles.

> [!NOTE]
> On peut référencer un même objet à partir de deux variables distinctes. Dans ce cas, les deux variables sont différentes, mais leur contenu est le même puisqu'elles référencent le même objet.

> [!WARNING]
> Si les objets sont totalement distinctes, les modifications sur l'un n'affectent pas l'autre. S'ils ne sont pas totalement distincts, en particulier lorsque deux variables du type de la classe référencent le même objet, les modifications sur l'objet lui-même sont accessibles à partir de deux variables.
