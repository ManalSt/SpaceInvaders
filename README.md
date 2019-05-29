# Space Invaders

## Fonctionnalité n°1 : Déplacer un vaisseau dans l'espace de Jeu.
### Story n°1 : Créer un espace de jeu.

Space Invaders est un projet basé sur la méthode du developpement TDD, ainsi que sur la méthode du refactoring.

Pour notre première story, le but est de créer un espace de jeu pour le jeu Space Invaders, chose qui nous permettera de bouger notre vaisseau dans l'espace.Nous avons mis au point un test, qui nous  par la suite, de pouvoir créer du code. Au début, notre test ne fonctionnait pas (rouge), mais avec l'ajout du code, notre test a fonctionné (vert). Le but de cette méthode (TDD) est de faire passer ce test le plus rapidement possible (vert).Comme résultat, nous avons obtenu une classe (SpaceInvaders), et une methode toString. La prochaine étape de cette story et le refactoring. Un refactoring consiste à changer la structure interne d’un logiciel sans en changer son comportement observable. Dans cette story,on a renommé une variable 's' en 'espaceDeJeu' en utilisant le raccourci ALT+SHIFT+R, cela nous donne une meilleure lisibilité du code. Après chaque modification , il ne faut surtout pas oublier de verifier si nos tests passent toujours ( on rappelle que le but du refactoring est de garder le même comportement observable du code).


### Story n°2 : Positionner un nouveau vaisseau dans l'espace de jeu.

Toujours avec la même demarche que la story précédente, nous allons positionner un nouveau vaisseau dans l'espace de jeu. Pour cela, il nous faudra des coordonnées x et y. Première chose à faire : écrire un nouveau test qui nous permettera d'ecride du code qui fera passer ce dernier. Pour ce test, nous avons utilisé les données suivantes : 

    un jeu Space Invader de longueur 15 et de hauteur de 10
    un nouveau vaisseau à positionner aux coordonnées x=8 et y=9 de l'espace de jeu.
    le caractère V pour marquer la présence d'un vaisseau dans l'espace de jeu lorsque celui-ci est affiché sous forme de         chaine de caractères ASCII.
    
 Les test suivent un pattern AAA (Arrange Act Assert). Arrange sert à l'initialisation du test. Act exécute le test et appelle la méthode à tester. Assert sert à vérifier le comportement attendu et le comportement réel de la méthode à tester.

Suite à l'écriture du test, des nouvelles méthodes ont été créé (positionnerUnNouveauVaisseau), de nouvelles classes sont apparues (Vaisseau) et une modification de la méthode toString. Pour cette story, le refactoring sera un Extract Methode qui  va nous permettre de remplacer, par exemple, rapidement l'instruction vaisseau!=null dans la méthode toString par un appel à la nouvelle méthode this.aUnVaisseau() avec le raccourci ALT+SHIFT+M. Toujours dans le meme story, nous avons mis au point deux tests qui permettent de ne pas déplacer le vaisseau en dehors des limites. Cela nous donne une modification de la méthode 'positionnerUnNouveauVaisseau' qui contient des conditions sur le déplacement du vaisseau ( des conditions IF). Enfin, nous avons améliorer la qualité du code avec une dernière Extract Methode.




### Story n°3 : Déplacer le vaisseau vers la droite dans l'espace de jeu.

Comme chaque, story, nous avons commencé par écrire un test. Ensuite, nous avons implémenté la méthode deplacerVaisseauVersLaDroite sur la classe SpaceInvaders et la méthode seDeplacerVersLaDroite dans la classe Vaisseau.


## Fonctionalité n°2 : Dimensionner le vaisseu.

Le but principal de cette fonctionalité est de donner des dimensions au vaisseau.

Comme chaque fonctionalité, on implemente d'abord des tests : premièrement on implémente un test qui permet de dimenensionner un vaisseau, puis on implémente la méthode "positionnerUnNouveauVaisseau" pour faire passer le test au vert et on modifie la classe Vaisseau. Puis nous passons à l'étape du refractoring.

Le deuxième test s'assure qu'il est impossible de positionner un vaisseau qui depasse de l'espace de jeu. Cela nous donne une nouvelle exception à lever et une nouvelle classe pour cette dernière, ainsi qu'une nouvelle implémentation pour la méthode. Les deux derniers tests sont responsable du déplacement du vaisseau en prenant compte de sa dimension  vers la gauche et vers la droite. Avec un refactoring, le fonctionnalité 3 est terminée.

## Fonctionalité n°3: Choisir le vitesse du vaisseau.

Pour cette fonctionalité nous allons définir la vitesse du vaisseau.

Premièrement,la vitesse d'un objet peut-être définie par un vecteur v à 2 dimensions (dx et dy) où :

* dx correspond au déplacement (c-a-d à un nombre de pixels pour le projet SpaceInvaders) effectué en 1 unité de temps sur l'axe des abscisses
* dy correspondra au déplacement (c-a-d à un nombre de pixels pour le projet SpaceInvaders) effectué en 1 unité de temps sur l'axe des ordonnées.
 
On ajoute donc un attribut "Vitesse" à la classe Vaisseau et on modifie les deux méthodes "deplacerVerslaDroite" et "deplacer versLaGauche" qui portent implicitement l'attribut vitesse sous forme de "-1" et "+1", on modifie donc ces deux valeures avec l'attribut vitesse et on l'initialise à 0 pour faire fonctionner le test correspondant.
Pour deplacer le vaisseau vers la droite avec une vitesse donnée, on a encore besoin d'un test couvrant cette fonctionalité.Nous avons alors transformeé la signature de la méthode "positionnerUnNouveauVaisseau" dans les tests automatiquement à l'aide de l'IDE pour effectuer ce changement le plus rapidement possible et le plus surement possible pour que la méthode puisse prendre en compte le nouvel attribut vitesse.

Après, nous nous sommes interessé au cas limites tels que : le vaisseau doit rester immobile car déjà en butée droite de l'espace de jeu et le vaisseau peut se déplacer partiellement et atteindre la butée, toujours avec la meme méthode du TDD. Puis nous nous sommes interessé au déplacement du vaisseau avec une vitesse quelcuonque.

## Fonctionalité n° 4 : Tirer un missile depuis le vaisseau.


L'objectif de cette fonctionnalité est de pouvoir tirer un missile depuis le vaisseau afin de donner un peu plus d'interactivité au jeu.

Pour réaliser cet objectif, il faut faire en sorte, qu'à chaque tir, un nouvel objet missile soit ajouté au jeu, en prenant soin de bien positionner ce missile au dessus du vaisseau au moment du tir. Une fois tiré, le missile devra se déplacer à la verticale de manière autonome et disparaître du jeu une fois le haut de l'écran de jeu atteint.

Premièrement, on utilise l'extract superclass depuis le menu de refactoring pour créer une nouvelle superclasse Sprint et qui sera la superclasse de Vaisseau. On effectue un petit refractoring au niveau des constructeurs des deux classes Sprite et Vaisseau.

A l'issue de ce refactoring, le diagramme de classes autour de la classe Vaisseau devrait d'aileurs ressembler à :

![Diagramme de Classes après refactoring](https://raw.githubusercontent.com/ManalSt/SpaceInvaders/master/Classes_S4_VaisseauSprite_ApresRefactoring.png)


Nous avons aussi créer une nouvelle classe de test qui concerne le missile. Cela nous amène à créer une nouvelle Classe Missile et l'ajout d'un attribut de type Missile sur la classe SpaceInvaders.
Au final, et après l'implémentation d'atres tests, j'ai obtenu le diagramme suivant :










![Diagramme de Classes](https://raw.githubusercontent.com/ManalSt/SpaceInvaders/master/object.png)

