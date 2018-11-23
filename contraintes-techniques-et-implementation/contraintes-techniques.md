# Contraintes Techniques

## Bonnes pratiques à respecter

* L'application doit s'appuyer sur le guide [Material Design](https://material.io/design/) et respecter la charte graphique établie.
* L'application doit produire des pages HTML valides (vérification W3C).
* L'application doit intégrer une extension du CSS (Sass) pour simplifier et optimiser dans le mesure du possible un CSS complexe ou répétitif.
* Interdiction d'utiliser des images pour faire des cadres ou des sections aux angles arrondis.

## Conditions d'utilisation

* L'interface utilisateur de l'application doit être en anglais.
* La partie cliente de l'application doit tourner sous Firefox, Chrome et Safari.
* La partie serveur de l'application doit fonctionner sous Linux.
* L'application doit pouvoir être installée via une image Docker.

## Performances attendues

* Si la partie cliente est une single-page application, alors la première page devrait peser moins de 500 Ko (images comprises).
* Plus globalement, le poids de chaque page ne devrait pas excéder 500 Ko (images comprises).

## Autres aspects

* Les interactions entre Petals et l'application se feront au travers de JMX ou bien via HTTP.
* La notion de session d'utilisation doit être supportée.
* Le support de la haute disponibilité n'a pas à être garanti.
