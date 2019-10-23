# Visualiser les services d'une topologie

Scénario : Albert souhaite visualiser le service d'une topologie, il accède à la vue d'ensemble. Par défaut, un encadré apparaît listant la totalité des interfaces. Une barre de recherche est mise à sa disposition lui permettant d’effectuer une recherche  \( A savoir une interface, un service ou un end-point \).

{% hint style="info" %}
Maquette ici
{% endhint %}



{% hint style="info" %}
La notation suivante est prise :
{% endhint %}

* \[ tâche \] fait référence à une autre tâche.
* Action \(sans crochets\) fait référence à une action utilisateur.

Concepts associés : une **Topologie**.  
Préconditions : -  
Postconditions : -  
Contraintes : -  
Complexité : -

Lorsque Albert effectue sa recherche, s'il ne sélectionne aucun élément de la liste, il voit apparaître dans sa recherche tous les éléments correspondant à sa recherche il peut donc voir les interfaces, les services et les end-points mélangés. Si la liste est supérieur à 10 éléments, un scroll apparaîtra et Albert pourra défiler le faire défiler pour trouver l'élément qu'il recherche.

{% hint style="info" %}
Maquette ici
{% endhint %}

  
Si Albert vient à sélectionner un élément il voit apparaître un  encadré rétractable sur la droite montrant le détail de sa recherche ainsi que les liens auquel l'élément sélectionné est rattaché. Cet encadré peut s'enlever via la croix ou l'icon info ⓘ. 

{% hint style="info" %}
Maquette ici
{% endhint %}



## Recherche en utilisant le sort by :

  
Scénario : Albert souhaite trouver en premier lieux les interfaces, puis les services qui dépend d'eux. pour se faire il peut sélectionner dans le sélect à droite de la search bar l'option "sort by interface" qui lui permettra d'avoir dans l'ordre : les résultats d'interfaces puis de service puis d'end-point.​

{% hint style="info" %}
Features à développer plus tard .
{% endhint %}

## Implémentation du sélect dans la barre de recherche

Scénario : Albert souhaite faire une recherche spécifique d'un end-point particulier, au lieu de voir la liste de tous les résultats, il peut filtrer pour n'avoir que la liste des end-points. Sa recherche s'en trouvera facilité.

{% hint style="info" %}
Features à développer plus tard .
{% endhint %}

## Sélection via l'encadré détail

Scénario : Albert souhaite effectuer une recherche d'interface, il se rend sur la barre de recherche et effectue sa recherche. En premier lieu il sélectionne le sélect pour ne voir apparaître uniquement les interfaces, ainsi la liste d'interfaces correspondant à sa recherche apparaît.

Lorsque Albert sélectionne une interface, un encadré détail apparaît listant les services et les end-points qui lui sont rattachés. la liste des interfaces présentes sous la barre de recherche reste inchangée.

Si Albert choisis un élément de navigation \( une Interface, un Service, ou un End-point \) il met à jour la liste sous la barre de recherche en lien avec le sort by avec les éléments qui lui sont liés. Exemple : 

{% hint style="info" %}
Features à développer plus tard .
{% endhint %}

