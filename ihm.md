# IHM

## Charte Graphique

Les éléments suivants constituent la charte graphique.

En cas de conflit entre la charte graphique préconisée et celle ci-dessous, c'est cette dernière qui domine. En effet, elle a été définie avec les besoins des utilisateurs \(**Petals**\) en tête.

* L'application doit occuper toute la largeur de l'écran. Pas de largeur fixe.
* Le design est réfléchi de manière à s'ajuster et s'adapter aux appareils de type ordinateur de table \(desktop\) ou tablette \(touch pad\). En suivant l'approche de conception _"desktop-first"_, l'interface d'un mobile n'est pas entièrement prise en charge.
* Le menu doit être accessible à tout instant, y compris quand la page devient très grande.
* L'application sera constitué d'une image marketing \(logo\) de Petals ESB et devra être toujours visible.
* L'application est découpée en plusieurs parties distinctes :
  * une barre de navigation latérale qui prend toute la hauteur sur la partie gauche et qui sert avant tout de barre de menu principal, mais aussi de barre de tâches.

    Elle permet de :

    * fermer et ouvrir la volet de navigation
    * consulter la liste des espaces de travail
    * visualiser une topologie
    * visualiser la liste des services
    * gérer les utilisateurs de cockpit \(espace réservé à l'administrateur\)
    * gérer ses préférences
    * se déconnecter

  * une barre de navigation horizontale sur la partie haute et qui sert de menu pour l'espace de travail.

    Elle permet de :

    * visualiser la liste des espaces de travail
    * sélectionner un espace de travail
    * définir un espace de travail
    * éditer un espace de travail
    * quitter l'espace de travail
    * supprimer un espace de travail
    * visualiser la liste des topologies
    * sélectionner une topologie
    * supprimer une topologie
    * importer une topologie
    * visualiser la liste des notifications

  * un volet de navigation qui permet de :
    * naviguer au travers une topologie Petals \(arbre représentant une topologie\)
    * rechercher/filtrer un élément sur une ou plusieurs topologie\(s\)
    * naviguer au travers les services d'une ou plusieurs topologie\(s\)
    * raffraîchir la liste des services
  * une page avec plusieurs parties distinctes qui permet de :
    * présenter chaque contenu pour chaque élément d'une topologie
    * procéder à des opérations de déploiement d'artefacts ou de configuration \(modification du cycle de vie, des paramètres ...\)
    * administrer les utilisateurs cockpit \(à condition d'avoir les droits administrateur\)
    * modifier les préférences utilisateur
* Les couleurs importantes de cockpit sont le violet \(primaire\), le orange \(secondaire\) et le blanc. En complément, les couleurs acceptées sont le rouge \(erreur\), le bleu \(information\), le vert \(succès\) et le gris.

Plus globalement, la logique du site doit être la suivante :

* On part d'un espace de travail, toujours. C'est la page d'accueil du site.
* On consulte une topologie, toujours. On navigue dans l'arbre.
* On descend d'un niveau pour arriver au conteneur.
* On descend encore d'un niveau pour arriver aux artefacts.

Dans cette logique, l'arbre du volet de navigation aide à se situer et à remonter d'un ou plusieurs niveaux. Toutefois, l'utilisateur a la possibilité de passer par le contenu du site pour consulter les parents ou enfants d'un élément sélectionné. De plus, cette approche coïncide \(volontairement\) avec la logique de fonctionnement et de distribution de Petals.

