# Cas d'Usage

## S'authentifier

L'application doit permettre de s'authentifier.  
Cela permet de sécuriser la connexion à un espace de travail.

Un identifiant et mot de passe sont prérequis pour accéder aux fonctionnalités disponible du cockpit.

**Intérêt pour les Utilisateurs**

| Consultants | Exploitants | Novices |
| :--- | :--- | :--- |
| Offrir un environnement de travail personnel et sécurisé | Offrir un environnement de travail personnel et sécurisé | Offrir un environnement de travail personnel et sécurisé |

## Créer un espace de travail

L'application doit permettre de définir un nouvel espace de travail.  
Cette entité permet principalement de gérer un ou plusieurs **bus Petals**.

On doit également pouvoir ajouter une description courte.

Seul les utilisateurs ayant une permission sont autorisés à travailler sur celui-ci.   
Cette permission est accordée par l'administrateur.

**Intérêt pour les Utilisateurs**

| Consultants | Exploitants | Novices |
| :--- | :--- | :--- |
| Offrir un espace personnel ou partagé. | Regrouper le travail a effectué dans un répertoire. | S'approprier l'approche projet/utilisateur de Petals Cockpit. |

## Ouvrir un espace de travail

L'application doit permettre d'ouvrir un espace de travail depuis la liste affichée après s'être connecté mais aussi depuis un autre espace de travail.

La liste contient l'ensemble des espaces de travail de l'application, que l'utilisateur y ait accès ou non.

Dans la liste, les espaces de travail sont représentés par leurs noms, leurs descriptions courtes et le nombre d'utilisateurs y aillant accès. La description courte ainsi que les administrateurs doivent être affichable.

Au cours de l'utilisation de l'application, une fois un espace chargé, la liste des espaces de travail doit être accessible depuis le header.

**Intérêt pour les Utilisateurs**

| Consultants | Exploitants | Novices |
| :--- | :--- | :--- |
| Offrir une vision d'ensemble. | Offrir une vision d'ensemble. | S'approprier l'approche projet/utilisateur de Petals Cockpit. |

## Éditer un espace de travail

L'application doit permettre de modifier un espace de travail.

En fonction du niveau d'accès, l'utilisateur doit avoir les droits suffisants pour effectuer cette action.

Dans certains cas, une notification est envoyée à tous les utilisateurs de l'espace de travail une fois l'action effectuée.

Dans le cas où un utilisateur se trouve déjà sur la vue d'un espace de travail éditée, la mise à jour des informations doit s'effectuée en temps réel automatiquement.

**Intérêt pour les Utilisateurs**

| Consultants | Exploitants | Novices |
| :--- | :--- | :--- |
| Pas d'intérêt particulier. | Pas d'intérêt particulier. | Pas d'intérêt particulier. |

## Quitter le groupe de l'espace de travail

L'application doit permettre de quitter un espace de travail lorsque l'utilisateur se trouve à l'intérieur de celui-ci.

Un message de confirmation doit apparaître lors de cette étape.

Dans le cas où l'utilisateur souhaite faire à nouveau partie de l'espace de travail, il devra contacter l'administrateur en trouvant son nom depuis la liste des espaces de travail.

**Intérêt pour les Utilisateurs**

| Consultants | Exploitants | Novices |
| :--- | :--- | :--- |
| Ne plus faire partie d'un espace de travail. | Ne plus faire partie d'un espace de travail. | Repartir de zéro après avoir fait ses tests. |

## Supprimer un espace de travail

L'application doit permettre de supprimer un espace de travail lorsque l'espace de travail est ouvert.

En fonction du niveau d'accès, l'utilisateur doit avoir les droits suffisants pour effectuer cette action.

Un message de confirmation doit apparaître lors de cette étape.

Une notification est envoyée à tous les utilisateurs de l'espace de travail une fois l'action effectuée.

Dans le cas où un autre utilisateur travaille au même moment sur cet espace de travail, il doit pouvoir continuer de consulter l'ensemble des éléments présent mais ne peut plus effectuer d'actions.

**Intérêt pour les Utilisateurs**

| Consultants | Exploitants | Novices |
| :--- | :--- | :--- |
| Abandonner un espace de travail plus à jour. | Abandonner un espace de travail plus à jour. | Repartir de zéro après avoir fait ses tests. |

## Sélectionner une topologie

L'application doit permettre de sélectionner une topologie depuis un espace de travail ouvert.

Cette représentation n'a pas à tenir compte des notions de domaine et de sous-domaine, qui ne sont pour l'instant pas utilisées dans Petals ESB.

Les informations tel que la description d'une topologie et la liste des nœuds Petals doivent apparaître dans une page lors de la sélection de celui-ci.

L'utilisateur peut accéder aux containers Petals existants depuis cette vue.

**Intérêt pour les Utilisateurs**

| Consultants | Exploitants | Novices |
| :--- | :--- | :--- |
| Découvrir rapidement le nom/port pour chaque machine \(VM\). | Visualiser les nœuds Petals. | Voir les détails d'une topologie. |

## Visualiser une topologie

L'application doit permettre de visualiser, au travers d'un graphe \(arbre\), l'ensemble de la topologie Petals.  
Cette représentation doit s'adapter à la taille de l'écran tout en supportant un grand nombre de nœuds.

Pour chaque nœud, le nom du nœud doit apparaître clairement tout comme les artefacts.

L'affichage des nœuds doit être ordonnée par nom de nœud. Enfin, il faut pouvoir filtrer la représentation grâce à un nom d'hôte ou un nom de conteneur, afin de ne pas obligatoirement tout afficher.

**Intérêt pour les Utilisateurs**

| Consultants | Exploitants | Novices |
| :--- | :--- | :--- |
| Découvrir rapidement une topologie en intervention. | Visualiser son domaine d'exploitation dans son ensemble. | S'approprier l'approche distribuée de Petals ESB. |

## Attacher une topologie

L'application doit permettre d'attacher une topologie à un espace de travail ouvert depuis celui-ci.

Il est nécessaire de compléter un formulaire comprenant une _ip_, un _port JMX_, un _nom utilisateur_, un _mot de passe_ et une _phrase secrète_ pour charger les informations d'un ou plusieurs nœuds depuis la machine contacter mais aussi, d'autres machines sur lequels pourraient se trouver un ou plusieurs nœuds supplémentaires de la topologie.

**Intérêt pour les Utilisateurs**

| Consultants | Exploitants | Novices |
| :--- | :--- | :--- |
| Découvrir une topologie. | Découvrir une topologie. | Découvrir une topologie. |

## Détacher une topologie

L'application doit permettre de détacher une topologie d'un espace de travail.

En fonction du niveau d'accès, l'utilisateur doit avoir les droits suffisants pour effectuer cette action.

Un message de confirmation doit apparaître lors de cette étape.

Une notification est envoyée à tous les utilisateurs de l'espace de travail une fois l'action effectuée.

Dans le cas où un utilisateur se trouve sur une des vues de la topologie affichée, il doit pouvoir consulter l'ensemble des informations des pages précédentes mais ne peut plus effectuer d'action sur la topologie détacher.

**Intérêt pour les Utilisateurs**

| Consultants | Exploitants | Novices |
| :--- | :--- | :--- |
| Choisir de ne plus travailler avec une topologie. | Choisir de ne plus travailler avec une topologie. | Repartir de zéro et réattacher une nouvelle topologie. |

## Visualiser les services d'une topologie Petals

L'application doit permettre de visualiser au travers 1 graphe \(arbre\) l'ensemble des services déployés dans l'infrastructure.  
Cette représentation doit s'adapter à la taille de l'écran tout en supportant un grand nombre de **services**, d'**interfaces** et d'**end-points**.

Pour chaque service sélectionné, il faut pouvoir afficher son/ses nom d'interface\(s\), nom de service, et nom d'end-point\(s\).

Pour chaque nom d'interface et de service sélectionné, son **namespace** et sa **localpart** doivent apparaître clairement. L'affichage des noms d'interfaces et services doit commencé par sa localpart.

La représentation des noms d'interfaces doit apparaître en premier, suivie des noms de services et enfin les noms d'end-points. Il doit être possible de modifier l'ordre de la représentation.

L'application doit aussi permettre de filtrer l'arbre selon différents critères.

L'application doit permettre de rechercher un élément parmis l'arbre de représentation **Service Endpoint**. Les critères de recherche se limiteront à des infos de déploiement: nom d'interface, nom de service et d'end-point.

**Intérêt pour les Utilisateurs**

| Consultants | Exploitants | Novices |
| :--- | :--- | :--- |
| Lister les services. | Visualiser les services en production dans son ensemble. | S'approprier la notion de service et comprendre ce qui tourne dans Petals. |

## Sélectionner un nom d'interface

L'application doit permettre de sélectionner un nom d'interface depuis l'arbre.

Il doit être possible d'ouvrir un volet latéral et afficher des informations supplémentaires en détails \(nom du _WSDL\*_, noms de services, noms d'end-points\). Par défaut, ce volet est déjà ouvert.

> WSDL\* : Web Services Description Language

Il doit être également possible d'effectuer des actions pour afficher seulement tous les services ou end-points de l'interface sélectionnée.

**Intérêt pour les Utilisateurs**

| Consultants | Exploitants | Novices |
| :--- | :--- | :--- |
| Découvrir rapidement l'ensemble des informations rattaché au même service. | Visualiser le nom des services. | Voir les détails pour un nom d'interface donné. |

## Sélectionner un nom de service

L'application doit permettre de sélectionner un nom de service depuis l'arbre.

Il doit être possible d'ouvrir un volet latéral et afficher des informations supplémentaires en détails \(nom du _WSDL\*_, noms d'interfaces, noms d'end-points\). Par défaut, ce volet est déjà ouvert.

> WSDL\* : Web Services Description Language

Il doit être également possible d'effectuer des actions pour afficher seulement toutes les interfaces ou end-points du service sélectionné.

**Intérêt pour les Utilisateurs**

| Consultants | Exploitants | Novices |
| :--- | :--- | :--- |
| Découvrir rapidement l'ensemble des informations rattaché au même service. | Visualiser le nom du WSDL, des interfaces et end-points. | Voir les détails pour un nom de service donné. |

## Sélectionner un nom d'end-point

L'application doit permettre de sélectionner un nom d'end-point depuis l'arbre.

Il doit être possible d'ouvrir un volet latéral et afficher des informations supplémentaires en détails \(nom du _WSDL\*_, noms d'interfaces, noms de services\). Par défaut, ce volet est déjà ouvert.

> WSDL\* : Web Services Description Language

Il doit être également possible d'effectuer des actions pour afficher seulement toutes les interfaces ou services du end-point sélectionné.

Pour chaque end-point, il faut connaître sa localisation \(le nœud de déploiement auquel il est rattaché\).

**Intérêt pour les Utilisateurs**

| Consultants | Exploitants | Novices |
| :--- | :--- | :--- |
| Découvrir rapidement l'ensemble des informations rattaché au même service. | Visualiser le nom du WSDL, service, interfaces et nœud de déploiement. | Voir les détails pour un nom d'endpoint donné. |

## Lister l'ensemble des artefacts déployés sur un nœud Petals

Pour un nœud donné, l'application doit pouvoir lister les artefacts Petals déployés sur ce nœud.  
Pour chaque artefact, il faut donner son identifiant et son état \(démarré, arrêté...\).

**Intérêt pour les Utilisateurs**

| Consultants | Exploitants | Novices |
| :--- | :--- | :--- |
| Découvrir rapidement ce qui tourne sur un nœud donné. | Voir ce qui est déployé sur un nœud donné. | Comprendre les artefacts Petals et les visualiser une fois déployés. |

## Visualiser les propriétés d'un nœud Petals

Pour un nœud donné, il faut pouvoir lister ses propriétés. Ces propriétés sont les suivantes :

* Propriétés du système \(OS, JVM\).
* Propriétés du nœud Petals, définies dans le **server.properties**.

Il s'agit de visualisation, donc pas de modification à chaud via l'application.

**Intérêt pour les Utilisateurs**

| Consultants | Exploitants | Novices |  |
| :--- | :--- | :--- | :--- |
| Récupérer les informations utiles sur un nœud, afin d'identifier les causes d'un problème, le tout, de manière centralisée. | Récupérer des informations sur un nœud, le tout, de manière centralisée. Intéressant pour communiquer des informations au support. | Découvrir les propriétés importantes de Petals. |  |

## Installer un artefact Petals

L'application doit permettre d'installer un ou plusieurs artefacts Petals sur un nœud donné.  
Les artefacts déployables sont librairies partagées, composants, service assemblies et service-units.  
Tant qu'un déploiement n'est pas terminé, l'application ne permet pas d'effectuer un autre déploiement en parallèle.

Le déploiement doit pouvoir se faire depuis un ou plusieurs fichiers en local. Ou bien il doit pouvoir se faire en précisant l'URL de l'artefact à déployer.

**Intérêt pour les Utilisateurs**

| Consultants | Exploitants | Novices |  |
| :--- | :--- | :--- | :--- |
| Installer en un clin d'œil des artefacts Petals. | Idéalement, pas utilisé par l'exploitant \(pas de déploiement à chaud en production\). Mais peut être utilisé pour installer des artefacts. | Pour débuter avec Petals et installer ses premiers artefacts. |  |

## Désinstaller un artefact Petals

La désinstallation d'artefacts Petals doit se faire simplement depuis leur page, lorsque cet artefact est à l'arrêt ou selon différents critères.

**Intérêt pour les Utilisateurs**

| Consultants | Exploitants | Novices |  |
| :--- | :--- | :--- | :--- |
| Désinstaller des artefacts Petals selon différents critères. | Désinstaller des artefacts Petals selon différents critères. | Désinstaller des artefacts Petals selon différents critères. |  |

## Modifier le cycle de vie d'un artefact Petals

L'application doit permettre de démarrer, arrêter ou passer en état _shutdown_\(installer\) n'importe quel artefacts Petals déployé sur un nœud.

Pour chaque artefact, une représentation graphique en image des états possible et de l'état actuel doit être visible.

**Intérêt pour les Utilisateurs**

| Consultants | Exploitants | Novices |  |
| :--- | :--- | :--- | :--- |
| Jouer sur le cycle de vie des artefacts \(utile par exemple pour recharger des paramètres\). | Jouer sur le cycle de vie des artefacts \(utile par exemple pour recharger des paramètres\). | Jouer sur le cycle de vie des artefacts. |  |

## Modifier à chaud des paramètres de Petals

Les composants Petals héritent, au travers du CDK, de certains paramètres configurables.  
Les paramètres suivants devraient être modifiables à chaud \(_during runtime_\) depuis le cycle de vie du composant :

* acceptor-pool-size
* acceptor-stop-max-wait
* processor-keep-alive-time
* processor-max-pool-size
* processor-pool-size
* processor-stop-max-wait

De la même façon, il y a dans le conteneur des paramètres accessibles et utiles \(transporteur, routeur\) :

* http-port
* https-enabled

D'autres paramètres pourront être rajoutés plus tard \(à terme, tous devraient être supportés par l'application\).

**Intérêt pour les Utilisateurs :**

| Consultants | Exploitants | Novices |  |
| :--- | :--- | :--- | :--- |
| Utile pour tuner des composants Petals. | Adapter les taille des pools aux besoins de production \(ajustements\). Modifier des propriétés du composant. | Voir ce qui est paramétrable. |  |

## Modifier à chaud des niveaux de log

L'application doit permettre de modifier à chaud les niveaux de log des composants Petals.  
Elle doit aussi permettre de modifier à chaud les niveaux de log pour des modules du conteneur.  
Avant modification, il faut bien sûr pouvoir lire le niveau de log actuel.

**Intérêt pour les Utilisateurs :**

| Consultants | Exploitants | Novices |  |
| :--- | :--- | :--- | :--- |
| Extrêmement utile pour diagnostiquer des problèmes. | Diagnostiquer des problèmes, suivre les indications du support. | Vérifier la dynamicité des traces dans Petals ESB. |  |

## Définir ses préférences

L'application doit permettre de définir des préférences pour l'utilisateur. Elles permettront d'améliorer le confort d'utilisation.

**Intérêt pour les Utilisateurs :**

| Consultants | Exploitants | Novices |  |
| :--- | :--- | :--- | :--- |
| Confort d'utilisation pour la pagination. S'adapter à de nouvelles topologies très vite. | Passer facilement d'un environnement à un autre \(topologie de tests, topologie de production\). | Vérifier que Petals, ce n'est pas si compliqué. Une information à fournir et la topologie entière est administrable. |  |

