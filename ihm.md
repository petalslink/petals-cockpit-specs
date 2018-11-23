# IHM

## Charte Graphique

Les éléments suivants constituent la charte graphique.

En cas de conflit entre la charte graphique actuelle et celle ci-dessous, c'est cette dernière qui domine. En effet, elle a été définie avec les besoins des utilisateurs (**Petals**) en tête.

* L'application doit occuper toute la largeur de l'écran. Pas de largeur fixe.
* Le design est réfléchi de manière à s'ajuster et s'adapter aux appareils de type ordinateur de table (desktop) ou tablette (touch pad). En suivant l'approche de conception _"desktop-first"_, l'interface d'un mobile n'est pas entièrement prise en charge.
* Les téléphones mobiles et résolutions inférieures à 800 pixels de large n'ont pas à être supportées.
* Le menu doit être accessible à tout instant, y compris quand la page devient très grande.
* L'application doit inclure une image marketing (logo) de Petals ESB, qui doit être toujours visible.
* Les couleurs importantes de cockpit sont le violet \(primaire\), le orange \(secondaire\) et le blanc. En complément, les couleurs acceptées sont le rouge \(erreur\), le bleu \(information\), le vert \(succès\) et le gris.


## Démarche

La logique de l'application doit être la suivante :

* On part de la page d'accueil.
* On sélectionne un espace de travail.
* Dans cet espace, on choisit une topologie.
* On arrive alors à une vue d'ensemble.
* On peut descendre d'un cran pour se focaliser sur un conteneur particulier, ou sur les consoles tierces (supervision, etc).

Dans cette logique, l'arbre du volet de navigation aide à se situer et à remonter d'un ou plusieurs niveaux. Toutefois, l'utilisateur a la possibilité de passer par le contenu du site pour consulter les parents ou enfants d'un élément sélectionné. De plus, cette approche coïncide (volontairement) avec la logique de fonctionnement et de distribution de Petals.


## Organisation de l'espace

* L'application est découpée en plusieurs parties distinctes :
  * Une barre de navigation latérale qui prend toute la hauteur sur la partie gauche et qui sert avant tout de barre de menu principal, mais aussi de barre de tâches.
  * Une barre de navigation horizontale sur la partie haute, et qui sert de menu pour l'espace de travail.

Elle permet de...
A REVOIR (plein de doublons dans les barres) + schéma
 