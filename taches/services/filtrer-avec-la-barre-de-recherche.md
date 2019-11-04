# Filtrer avec la barre de recherche et le système de tag

Les résultats de l'arbre de service endpoint sont triés en fonction de ce que l'utilisateur inscrit dans la barre de recherche. Les éléments\( interfaces, services, endpoints\) de l'arbre se mettent à jour avec les résultats qui correspondent à la recherche.  
Dans une prochaine feature, un système de tag sera intégré à la barre de recherche,   
Lors de la sélection de la barre de recherche, une liste déroulante appelé select apparaît, proposant plusieurs choix.   
Il existe deux solutions pour sélectionner un choix :  
Le premier consiste à cliquer sur un élément de la liste déroulante.  
Le deuxième consiste à écrire le choix du select commençant par un " : ".  
Exemple : " :interface ", sélectionne l'item interface de la liste déroulante.  
Une fois le choix sélectionner, celui-ci s'insère dans la barre de recherche. L'arbre est mis à jour et présente les résultats qui correspondent au tag. En reprenant l'exemple de l'interface, l'arbre ne liste que les interfaces. Si l'utilisateur a inscrit du texte dans la barre de recherche en plus du tag, l'arbre ne liste que les interfaces dont le texte correspond à ce qui est inscrit dans la barre de recherche.  
A noter que plusieurs tags peuvent être entré dans la barre de recherche.  


  
_**liste des tags présents dans le sélect**_ **:**  
- Interface  
- Service  
- Endpoint  
- Namespace  
- Localpart  
- Bus  
- Composant  
- Conteneur

{% hint style="info" %}
Maquette montrant le début d'une recherche
{% endhint %}

{% hint style="info" %}
Maquette montrant le résultat d'une recherche.
{% endhint %}

