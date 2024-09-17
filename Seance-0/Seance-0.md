# Installation de `Java`

## Choisir un éditeur de code

Comme tout projet informatique, il faut choisir un éditeur de code :

- `Notepad++` ;

- `CodeBlock` ;

- *etc*.

Toutefois, dans un environnement professionnel, deux éditeurs sont principalement utilisés :

- `Visual Studio Code` (`VS Code`);

- `Eclipse`, éditeur spécifique permettant de coder du `Java`. L'avantage de son utilisation est qu'il identifie certaines erreurs avant la compilation et qu'il possède, comme `VS Code` un terminal.

## Télécharger les outils de développement `Java`

1. Trouver la page `Java SE Downloads`

2. Télécharger le J.D.K.

> [!NOTE]
> Le J.D.K. regroupe le J.R.E. et le Server J.R.E. Le `JRE` est l'environnement de lancement et l'outil de développement, tandis que le `Server JRE` inclut les fonctions internet.

3. Installe le J.D.K.

	- Cliquer sur `Next Step`
	
	- Décocher `Activer le contenu Java dans le navigateur`

4. Activer `Java` dans l'environnement du système d'exploitation

	- Repérer `javac.exe` et en copier l'adresse : `C:\Programmes\Java\jdk[...]\bin\`
	
	- Aller dans `Paramètres Windows`
	
		- Chercher `Environment` et cliquer sur `Modifier les variables d'environnement système`
		
			- Ouverture de la fenêtre `Propriétés système`

	- Dans la fenêtre `Propriétés système`, cliquer sur `Variable d'environnement`
	
		- Modifier la variable système `Path`
		
			- Ouverture de la fenêtre `Modifier la variable d'environnement`

	- Dans la fenêtre `Modifier la variable d'environnement`, clique sur `Nouveau`
	
		- Insérer le chemin vers `javac.exe`

> [!WARNING]
> S'il y a une erreur lors de la compilation, c'est qu'il faut placer la ligne plus haut dans la liste des variables d'environnement.
