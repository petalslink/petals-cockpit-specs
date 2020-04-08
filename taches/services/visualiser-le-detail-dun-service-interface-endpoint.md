# Visualiser les services et les interfaces

Sélectionner une interface ou un service dans l'arbre affiche \(à droite\) la page de détail respectivement de l'interface et du service. Dans les deux cas cette vue se compose de deux parties: **related elements** et **endpoints detail** 

![Sections de la vue de d&#xE9;tail des interfaces et services.](https://lh4.googleusercontent.com/6j0q4_09jVgPSpH96p_oMdaSqQXakdX8D2mTpCA18ytsxB_04vm4-89Xesxvu036WtBYZd9BrOX31ZrY9TzaJsCOucIf9EGf09g2vd3oO6J8NkL7Vat9NZyF4AznVHCxQbG1v5ku)

**Related element** change en fonction de la vue.

* Detail d'interface: on affiche les services associés
* Detail de service: on affiche les interfaces associés

Dans les deux cas les elements sont des liens amenant à la vue de détail du service ou de l'interface. \(liens de navigation\)

**Endpoints detail** est se comporte de la même manière pour les deux vues. On va lister tous les endpoints liés à l'interface ou service dont on visionne le  détail.

Chaque endpoint sera présenté avec des informations associés \(qui doivent tous être des liens de navigation\):

* Nom du endpoint
* Nom de son composant
* Conteneur sur lequel il tourne
* Bus sur lequel le conteneur tourne

