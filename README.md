# images
Images des éditions

nstallation des images par recherche/remplace:

1.

Chercher :

<pb

Remplacer par :

<pb facs="http://gongoradigital.github.io/img/1660_apologetico/1660_apologetico_f.JPG"

Note: dans cette première étape, f.JPG est une valeur vide: f1r.JPG est le format attendu, correspondant au f. 1r, et ainsi de suite.

 

2.

Chercher :

<pb facs="http://gongoradigital.github.io/img/1660_apologetico/1660_apologetico_f.JPG" n="f. ([b|c|d]?[1-9]+[r|v])"

<pb facs="http://gongoradigital.github.io/img/1660_apologetico/1660_apologetico_f$1.JPG" n="f. $1">

 
3.
Vérifier les facs="http://gongoradigital.github.io/img/1660_apologetico/1660_apologetico_f.JPG" restants, où il faut introduire une valeur après le "f" final.

Note 1: Dans l'étape 2, la chaîne de caractères [b|c|d]? signifie: soit "b", soit "c", soit "d", soit "ensemble vide" (tel est le sens du point d'interrogation). Cela correspond à la foliation établie à partir des les signatures des préliminaires de mon édition: Sign.: []2, b4, c4, d3. Il faudra donc voir au cas par cas s'il est nécessaire d'introduire cet élément dans l'expression régulière. Concernant [1-9]+, cela signifie: tout caractère numérique entre 1 et 9, qu'il y en ait un seul ou plusieurs. De même, [r|v] signifie: soit "r", soit "v". Cette regex permet donc de trouver autant les f. des préliminaires que la foliation du reste du texte.

Note 2: Pour les deux premiers folios de l'Apologético, f. []1r-v et f. []2r-v, les caractères correspondant aux crochets vides posent problème dans l'hyperlien: j'ai donc renommé (dans l'entrepôt et dans l'hyperlien) les images  fa1r-v et fa2r-v en gardant toutefois dans l'édition l'écriture initiale. Le résultat est donc:
<pb facs="http://gongoradigital.github.io/img/1660_apologetico/1660_apologetico_fa1r.JPG" n="f. []1r"/>

Note 3: La valeur .png ou .jpg, qui doit obligatoirement apparaître en minuscules, peut changer en fonction du format des images.

Note 4: L'étape 3 a été nécessaire pour résoudre les cas où la recherche de l'étape 2 ne trouvait pas tous les <pb>. Cela arrive quand un saut de ligne est intercalé entre "<pb" et "n=". Frédéric: comment peut-on résoudre cela pour améliorer la recherche -dans ce cas comme dans beaucoup d'autres-? Merci d'avance.