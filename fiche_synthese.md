|  | Type de problème mathématique | Difficulté du problème d’un point de vue mathématiques | Modèle utilisé | Comparaison avec modèles non IA | Syntaxe/encodage des entrées | Type de transformation (entre l'entrée et la sortie) | Généralisation des modèles | 
| ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| Article 1 | Intégration et équations différentielles | Avancée | Transformer | Meilleure pour transformer | Arbre/Notation polonaise | Symbolique à symbolique | Difficulté de généralisation à toutes les méthodes de génération de données |
| Article 2 | Identifier série de récurrence | Avancée | Transformer | Meilleure pour transformer | Arbre/Notation polonaise | Numérique à symbolique | Bonne généralisation à différente fonction, mais la nombres la séquence doivent rester dans une certaine range. |
| Article 3 | Propriétés de systèmes différentiels | Avancée | Transformer | Proche des modèles non IA (dont l'accuracy est ici de 100%) | Arbre/Notation polonaise | Symbolique à numérique | Bonne généralisation (bonne performance pour des données de taille et de dimensions supérieures) |
| Article 4| Démonstration de théorèmes géométriques | Avancée | Transformer couplé à un outil de calcul formel| Supérieur | langage inspiré par un logiciel de calcul de preuve (JGEX) | Formel à Formel | Bonne application à des problèmes issus des olympiades mathématiques |



## Description de la problématique

Cette revue d'articles nous a permis de considérer un ensemble d'études portant sur l'utilisation d'architectures type transformers pour de réaliser différentes tâches mathématiques. 
Une première limite avancée par les auteurs des 3 premiers articles concernait, au vue de l'état de l'art, la difficulté affichée de ce type de modèle à affectuer des tâches arithmétiques simples. Les auteurs ont montré que leur encodage des données et une méthode efficace de génération de dataset permet d'entraîner ces modèles et de surpasser (ou a minima d'égaler) les outils de références utilisés pour ce type de tâche mathématiques.
Notre dernier article a lui traité d'un usage combiné d'un modèle Transformers avec un outil de calcul de formel dédié à la démonstration de théorème géométrique. L'avantage de cette méthode réside dans le fait de pouvoir générer de nouvelles étapes de preuves sur lequel le modèle n'a pas été entraîner. De plus, en sauvegardant les sorties du modèle, les étapes successives de raisonnement pouvaient être lues et vérifier par un humain. 


Il serait donc intéressant de voir à présent si cette dernière approche pourrait être appliquée à d'autres domaines mathématiques afin de créer un modèle capable d'expliciter les différentes étapes de résolution pour un problème donnée.
Notre problématique est donc la suivante : peut-on concevoir un modèle basé sur une architecture type transformers capable d'expliciter les différentes étapes de résolution d'un problème donné (i.e démonstration d'un théorème d'algèbre, explicitation des différentes étapes d'une opération mathématique, résolution guidée d'un problème, etc ...)
