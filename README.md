Introduction 

  Dans le cadre de notre projet nous sommes amenés à implémenter l’algorithme 
PageRank en utilisant le vecteur ∇ et de faire une comparaison avec l’algorithme 
de base sur des graphes du web par rapport aux performances, efficacité et 
temps d’exécution.
L’algorithme initial est le PageRank, lors du calcul de graphiques Web, ou plus 
précisément de matrices creuses, l’algorithme utilise un vecteur stochastique de 
la taille de la matrice. Il est initialisé et la matrice est multipliée en quelques 
itérations jusqu'à ce que ce vecteur stochastique converge. Le second algorithme 
est une modification de l’algorithme de PageRank. En effet, cet algorithme 
utilise deux vecteurs nabla et delta où l’initialisation de chaque case de nabla est
le minimum de chaque colonne de la matrice G et l’initialisation de chaque case 
de delta est le maximum de chaque colonne de la matrice G.

Définition de l’algorithme 
 
 ∇[j] = mini G [i, j] 
 ∆[j] = maxi G [i, j]
 
 I. Initialiser X0 = ∇. Y0 = ∆ 
 
II. Faire une boucle sur k

  (a) X^k+1 = max (X^k, X^k*G + ∇ (1 − ||X^k ||1)
 (b) Y^k+1 = min (Yk, Y^k*G + ∇ (1 − ||Y^k ||1)
 
III. Jusqu’à ce que ||X^k − Y^k ||1 < e


Graphe du web

On prend en lecture des fichiers textes avec les informations suivantes :
x Première ligne on trouve le nombre de sommets du graphe.
x Deuxième ligne on trouve le nombre d’arcs du graphe.
x A partir de là sur chaque ligne on trouve le numéro de sommet, le degré 
sortant de ce sommet et des couples (destination, cout).


