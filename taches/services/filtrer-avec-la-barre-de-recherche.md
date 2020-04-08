# Système de recherche avancée par tag

{% hint style="danger" %}
**Feature optionnelle. N'est pas nécessaire pour le refactor.**
{% endhint %}

Un système de recherche par tags sera intégré à la barre de recherche. Il sera comparable à celui de gitlab \(qui sera notre référence\). On pourra ainsi affiner la recherche en attribuant à chaque élément une série de tags \(qui correspondent aux informations que l'on peut retrouver dans le détail de leur vues\). En plus \(ou au-lieu\) d'un filtrage standard, on pourra réduire les éléments de l'arbre en n'affichant que ceux qui correspondent. Il faudra cependant toujours afficher les éléments au dessus des éléments affichés, la hiérarchie de l'arbre reste inchangée \(comme pour la recherche classique\). Il faudra aussi conserver un éventuel changement de niveau lors de la recherche.

Quelques exemples :

{% hint style="warning" %}
La syntaxe ci dessous est donnée à titre d'exemple. Le choix final est laissé à la discrétion du développeur pour lui faciliter la tâche. \(tant que l'on répond aux exigences bien évidement\)
{% endhint %}

{% tabs %}
{% tab title="Classique" %}
Taper dans la barre de recherche

```text
camion
```

N'affiche que les elements dont le nom comporte le string "camion"
{% endtab %}

{% tab title="1 Tag" %}
Taper dans la barre de recherche

```text
interface="camion" 
```

N'affiche que les elements dont le nom d'interface comporte le string "camion"
{% endtab %}

{% tab title="2 Tags" %}
Taper dans la barre de recherche

```text
interface="camion" bus="poubelle"
```

N'affiche que les elements dont 

* le nom d'interface comporte le string "camion"
* **Et** le endpoint associé tourne sur le bus dont le nom comporte le string "poubelle"
{% endtab %}

{% tab title="2 Tags + classique" %}
Taper dans la barre de recherche

```text
interface="camion" bus="poubelle" magique
```

N'affiche que les elements dont

* le nom d'interface comporte le string "camion"
* **Et** le endpoint associé tourne sur le bus dont le nom comporte le string "poubelle"
* **Et** dont le nom comporte le string "magique"
{% endtab %}
{% endtabs %}

{% hint style="info" %}
Par la suite quand on écrit "l'élément contient X" il sera toujours sous entendu "le nom de l'élément contient le string X"
{% endhint %}

**Liste des tags acceptés:**  
- **Interface**: l'interface associée à l'élément contient X.  \(Ou l'élément lui, même si c'est une interface\)  
- **Service**: le service associée à l'élément contient X.  \(Ou l'élément lui, même si c'est un service\)  
- **Endpoint**: le endpoint associé à l'élément contient X.  \(Ou l'élément lui, même si c'est un endpoint\)  
- **Namespace**: le namespace de l'élement contient X.  
- **Localpart**: la localpart de l'élément contient X.  
- **Bus**: le bus sur lequel tourne un endpoint associé à l'élément contient X. \(Ou l'élément peut être le endpoint en question\)  
- **Composant**: le composant sur associé au endpoint associé à l'élément contient X. \(Ou l'élément peut être le endpoint en question\)  
- **Conteneur**: le conteneur sur lequel tourne un endpoint associé à l'élément contient X. \(Ou l'élément peut être le endpoint en question\)

Il faut faciliter l'utilisations des tags pour le client. Pour cela nous allons proposer plusieurs moyens d'ajouter un tag à la barre de recherche avec la syntaxe correcte. Ces différents moyens devront se terminer en plaçant le prompteur au bon endroit pour commencer à renseigner le string recherché dans le tag. Plusieurs moyens de les pré-saisir: 

1. Commencer à taper un des noms de tags le proposera par complétion automatique: petit encadré au dessous montre les choix possibles, appuyer sur espace ou entrée inscrit le tag \(alternativement nous pourrions aussi cliquer dessus, ou se déplacer avec les flèches de direction du clavier\).
2. Un menu déroulant peut être ajouté proche de la barre de recherche, il listerai tous les tags disponibles et en sélectionner un l'ajouterai à la barre de recherche.

