# BabaWasYou
 
Analyse théorique :

1. De quel type de jeu s’agit-il ?
Ce jeu est de type Puzzle/Réflexion en solo.

2. Après une heure de jeu, nommez les différentes mécaniques de gameplay
rencontrées.
   1- Déplacement (WQSD)
   2- Possibilité de pousser certains éléments de l'environnement.
   3- Recommencer le niveau (R)
   4- Revenir à l'action précédente (Z)
   5- Possiblité de prendre le contrôle des éléments du jeu (Rock/Crab/Flag/Wall/Key/etc)
   6- Modifier l'état et les propriétés (YOU/WIN/PUSH/DEFEAT/STOP/OPEN/SHUT/etc) des éléments du jeu à l'aide des block "texte" (BABA/WALL/CRAB/FLAG/ROCK/DOOR/IS/AND)

3. Ce jeu est considéré comme un jeu fait pour des développeurs, expliquez en quoi.
Ce jeu force à réfléchir aux différentes règles misent en place par le dev et comment les utiliser pour réussir le niveau

4. L’association des mots se font selon certaines règles :
“Baba Is Wall” -> valide /
“Wall Is You” -> valide /
“You Is Baba” -> non valide /
“Baba and Wall Is You” -> valide
Expliquez comment ces règles fonctionnent.

L'association suit la logique "Nom de l'acteur -> IS/AND -> Conséquence (Etat(STOP/YOU/etc) et/ou autre acteur(WALL/CRAB))
On renseigne d'abords les différents acteur concernés grâce aux blocks de texte, puis les opérateurs "AND" et "IS", et enfin, la conséquence comme un changement d'état, de propriété ou de mesh (ex: Baba Is Wall ou Wall Is You).


5. Vu le nombre de combinaisons possibles, d’après vous, comment le développeur
a-t-il fait pour obtenir un tel résultat ? Expliquez en termes techniques (pseudo-code,
algorithmes, type de données, modifications du gameplay…) comment vous auriez
mis en place une telle mécanique de gameplay.

Je pense que le dev a utilisé des gameplays tags pour les différents règles présentes dans le jeu (PUSH/WIN/etc) permettant ainsi de couvrir plusieurs états à la fois.
Pour le "changement d'objets", une énumération de string permettrai de définir le mesh, étant donné que l'acteur n'a qu'un mesh à la fois.
Pour tout ce qui est MOTS et OPERATORS, une énumération serait de chaque pourrait avoir pu être utilisées

6. Personnel : le jeu vous a-t-il plu ? Pourquoi ?

Jeu intéressant, demandant rapidement de plus en plus de réflexion et d'itération pour résoudre les énigmes. 
Challengeant comme il faut, puis côté sympa de se rendre compte que la solution était "simple" ou facile à trouver alors que tu es sur le niveau depuis 10-20min. 



Pratique :
1. Définissez, selon vous, la mécanique de gameplay principale du jeu, et reproduisez
là sous le moteur de jeu de votre choix (vous pouvez faire cette mécanique sur un
projet en 2D ou 3D).

D'après moi, la méca principale serait le changement de propriétés des acteurs lorsque le joueur intéragi avec les différents blocs du niveau

2. Décrivez, étape par étape, comment vous avez mis en place cette mécanique.
Utilisation d'Enumeration pour les Mots, Operateurs et Règle
L'opérateur check en haut et en bas si un Mot et une Règle si trouve, puis de gauche à droite. Si le résultat est concluant, les tags s'ajoutent aux objets concernés, sinon il les retirent à l'aide de réference créer lors de l'ajout des tags

3. Expliquez en quoi cette mécanique est primordiale tout au long du jeu.

Elle permet une pluralité de gameplay immenses, que ce soit dans la création d'énigmes, ou bien dans la résolution de ces dernières.

4. Pourquoi cette mécanique vous a-t-elle plu ?
