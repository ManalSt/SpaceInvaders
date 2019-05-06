# SpaceInvaders

Space Invaders - 

Fonctionnalité n°1 : Déplacer un vaisseau dans l'espace de Jeu.
Créer un espace de jeu.

Pour cette première partie, nous allons nous concentrer sur la partie du code de notre jeu Space Invaders qui consiste à faire bouger le vaisseau spacial dans l’espace du jeu.
Nous avons ajouté en premier lieu un test qui est censé verifier l’existence de cet espace de jeu, le test échoue bien entendu, c’est là ou on commence à coder la classe responsable de la création de l’espace de jeu. C’est la méthode du TDD qui consiste à enrichir le programme petit à petit jusqu’a ce que le test en question passe du rouge au vert.
Pour un code plus clair et plus concret, nous avons utilisé la méthode du refractoring pour renommer des variables plus efficacement ( sans avoir recours à changer la variable chaque fois qu’elle apparaît dans le code. 

Fonctionnalité n°É : Positionner un nouveau vaisseau dans l’espace de jeu.

Pour cette story, nous utiliserons aussi la fameuse méthode du TDD. On commence par créer un test qui illustre le comportement normal de la story c-a-d que le vaisseau devrait bien être positionné aux coordonnées x et y transmises puisque ces coordonnées se situent bien dans l'espace jeu. Puis on essaye de rendre le code du test compilable
