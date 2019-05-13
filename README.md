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


