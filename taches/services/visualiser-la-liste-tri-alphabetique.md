# Visualiser la liste des services

La liste des services comporte l'ensemble des interfaces, services et endpoints présents dans les bus du workspace courant; elle se situe à gauche de la page. Elle se présente sous la forme d'un d'un arbre hiérarchisé \(interfaces &gt; services &gt; endpoints\). Les éléments peuvent être pliés ou dépliés en cliquant sur la flèche en bout de ligne, afin de masquer leurs enfants. 

A la sélection d'un élément, on affiche son détail dans la vue à droite.  

* Sous chaque interface on retrouve tous les services qui lui sont associé. \(Un même service peut donc potentiellement être présent plusieurs fois dans l'arbre\)
* Sous chaque service, tous les endpoints qui lui sont associés. 
* Par défaut, seul les interfaces sont visibles, les autres éléments sont pliés.
* Il faut un moyen de voir le nom du service en entier \(tooltip sur une icone par exemple\)
* Les namespaces sont répétés à chaque ligne \(dans un premier temps du moins\)
* La liste propose un bouton afin de rafraîchir la liste.
* Une barre de recherche permet de filtrer l'arbre selon la recherche \(de la même manière que dans l'arbre des topologies\)

![](../../.gitbook/assets/selectioninterface%20%282%29.png)



{% hint style="warning" %}
Ci dessous sont les features à venir. Elle ne sont pas nécessaires dans un premier temps
{% endhint %}

* Permettre d'organiser les résultats de l'arbre par ordre alphabétique ou par ordre alphabétique inversé. Ce tri ne s'applique que les éléments du premier niveau de l'arbre.
* Ajouter des boutons **fold all** et **unfold all** qui permettent de plier ou déplier **tous** les elements de l'arbre simultanément**.**
* Permettre de changer la largeur du panel de gauche contenant l'arbre **\(A DISCUTER\)** Les namespaces pouvant être très long, cela pourrait éviter des problème de visionnage au client.
* Réduire le niveau de l'arbre, précisé dans [la section dédiée](change-tree-level.md)
* Afin de réduire la taille des éléments de l'arbre, on peut afficher le namespace des interfaces avant celles ci, au même niveau de l'arbre; ce qui formera une sorte de section sur laquelle le namespace s'applique. Cela permettra de retirer le namespace de chaque élément si celui ci est le même \(on pourra aussi le retirer des services en dessous\). Il faudra cependant faire attention à bien conserver le namespace de chaque service si il est différent de celui de la section. Maquette ci dessous.

![Arbre avec sections de namespace](../../.gitbook/assets/selectioninterface%20%283%29.png)

