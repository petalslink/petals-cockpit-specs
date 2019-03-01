# IHM

## Charte Graphique

Les éléments suivants constituent la charte graphique.

En cas de conflit entre la charte graphique préconisée et celle ci-dessous, c'est cette dernière qui domine. En effet, elle a été définie avec les besoins des utilisateurs \(**Petals**\) en tête.

* L'application doit occuper toute la largeur de l'écran. Pas de largeur fixe.
* Le design est réfléchi de manière à s'ajuster et s'adapter aux appareils de type ordinateur de table \(desktop\) ou tablette \(touch pad\). En suivant l'approche de conception _"desktop-first"_, l'interface d'un mobile n'est pas entièrement prise en charge.
* La taille minimale \(résolution\) de la zone d'affichage \(à l'intérieur du navigateur web\) est définie à 960 pixels de large \(par 540 pixels de haut\) les largeurs correspondent à md, lg et xl sur [flex layout](https://github.com/angular/flex-layout/wiki/Responsive-API#mediaqueries-and-aliases) et à small-tablet \(la plus grande taille de small\), medium, large et xlarge sur [material design](https://material.io/design/layout/responsive-layout-grid.html#breakpoints). Au dessous de cette taille, l'application peut avoir des problèmes d'affichage.
* Le menu doit être accessible à tout instant depuis un espace de travail ouvert, y compris quand la page devient très grande.
* L'application sera constitué d'une image marketing \(logo\) de Petals ESB et devra être toujours visible.

![logo petals cockpit](.gitbook/assets/logo-petals-sidebar.jpg)

* L'application est découpée en plusieurs parties distinctes :
  * une barre de navigation latérale appelée "sidebar" qui prend toute la hauteur sur la partie gauche et qui sert avant tout de barre de navigation principal pour cockpit. 

    Elle permet de :

    * visualiser une topologie \(visible que si un espace de travail est ouvert\)
    * visualiser la liste des services \(visible que si un espace de travail est ouvert\)
    * visualiser les consoles \(visible que si un espace de travail est ouvert\)
    * gérer les utilisateurs de cockpit \(espace réservé à l'administrateur\)
    * gérer ses préférences \(toujours visible lorsque l'utilisateur est connecté\)
    * se déconnecter \(toujours visible lorsque l'utilisateur est connecté\)

![](.gitbook/assets/sidebar.png)

* une barre de navigation horizontale sur la partie haute et qui sert de menu pour l'espace de travail ouvert.

  Elle permet de :

  * se rendre sur la vue de sélection d'un espace de travail en quittant l'espace courant
  * se rendre sur la vue de création d'un nouvel espace de travail en quittant l'espace courant
  * visualiser le nom de l'espace de travail ouvert
  * visualiser la liste des espaces de travail
  * sélectionner un autre espace de travail
  * visualiser la liste des notifications \(facultatif\)
  * visualiser le fil d'ariane à partir d'un bus sélectionné

![toolbar espace de travail sans bus s&#xE9;lectionn&#xE9; \(pas de fil d&apos;ariane\)](.gitbook/assets/barre-menu-workspace%20%281%29.png)

![toolbar espace de travail avec bus s&#xE9;lectionn&#xE9; \(exemple depuis un conteneur\)](.gitbook/assets/fil-dariane.png)

![menu espace de travail](.gitbook/assets/workspace-overview-menu-1.png)

* les différentes vues principales lorsqu'un espace de travail est ouvert :
  * vue topologie
    * un volet de navigation qui permet de :
      * naviguer au travers une topologie Petals \(arbre représentant une ou plusieurs topologie\(s\)\)
      * rechercher/filtrer un élément sur une ou plusieurs topologie\(s\)
    * présenter chaque contenu pour chaque élément d'une topologie
    * procéder à des opérations de déploiement d'artefacts ou de configuration \(modification du cycle de vie, des paramètres ...\)
    * ...
  * vue services
    * un volet de navigation qui permet de :
      * naviguer au travers les services d'une ou plusieurs topologie\(s\)
      * raffraîchir la liste des services
      * ...
  * vue api \(à définir\)
  * vue consoles \(à définir\)
* une page avec plusieurs parties distinctes qui permet de :
  * administrer les utilisateurs cockpit \(à condition d'avoir les droits administrateur\)
  * modifier les préférences utilisateur 
* Les couleurs importantes de cockpit sont le violet \(primaire\), le orange \(secondaire\) et le blanc. En complément, les couleurs acceptées sont le rouge \(erreur\), le bleu \(information\), le vert \(succès\) et le gris.

Plus globalement, la logique du site doit être la suivante :

* On part d'un espace de travail, toujours. C'est la page d'accueil d'un espace ouvert.
* On consulte une topologie. On navigue dans l'arbre.
* On descend d'un niveau pour arriver au conteneur.
* On descend encore d'un niveau pour arriver aux artefacts.

Dans cette logique, l'arbre du volet de navigation aide à se situer et à remonter d'un ou plusieurs niveaux. Toutefois, l'utilisateur a la possibilité de passer par le contenu du site pour consulter les parents ou enfants d'un élément sélectionné ou bien par le fil d'ariane. De plus, cette approche coïncide \(volontairement\) avec la logique de fonctionnement et de distribution de Petals.

