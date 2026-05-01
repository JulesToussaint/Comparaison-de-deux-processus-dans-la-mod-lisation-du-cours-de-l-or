# Comparaison de deux processus dans la modélisation du cours de l'or
L'or est coincé entre deux classes d'actif : commodity et actif d'investissement. Pour palier à cette ambiguïté, ce notebook inspecte le comportement du cours de l'or et le compare à deux processus classiques dans la modélisation d'une commodity et d'un actif d'investissement.

Le processus de base pour modéliser la valeur d'une action, ou d'un actif d'investissement en général, est le Geometric Brownian Motion (GBM) qui obéit à cette équations stochastique :
$$
dX_t = \mu X_t dt + \sigma X_t dW_t
$$

A l'inverse, une commodity obéit à un process d'Ornstein-Uhlenbeck (OU) qui est dit "mean reverting", il ramène la valeur du produit vers sa moyenne. Il obéit àcette équation stochastique :
$$ dY_t = \kappa (\theta - Y_t)dt + \sigma dW_t, \quad Y_0 $$


Dans ce notebook, nous examinons les similitudes entre le cours de l'or et ces deux process, en se basant sur trois tests principaux :
- Le test d'autocorrélation
- Le test ADF, qui cherche à savoir si une série est stationnaire
- Le test ratio-variance
