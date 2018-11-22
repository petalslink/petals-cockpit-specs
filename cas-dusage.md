# Cas d'Usage

Cette page liste les cas d'usage pour Petals Cockpit.


## Généralités

### Authentification

L'application doit permettre de s'authentifier.  
Cela permet de sécuriser la connexion à un espace de travail.
Un identifiant et mot de passe sont des prérequis pour accéder aux fonctionnalités du cockpit.

S'il s'est déjà connecté une fois précédente, trois cas de figure se présentent :

* L'utilisateur cherche à atteindre la page d'accueil de Cockpit et la préférence **Retour à la dernière page visitée lors de la prochaine reconnexion** n'est pas activée. Une fois connecté, il revient alors sur la page d'accueil.
* L'utilisateur cherche à atteindre la page d'accueil de Cockpit et la préférence **Retour à la dernière page visitée lors de la prochaine reconnexion** est activée. Une fois connecté, il est redirigé vers la dernière page qu'il a visitée.
* L'utilisateur cherche à atteindre une autre page que l'accueil de Cockpit. Quelle que soit la valeur de la préférence **Retour à la dernière page visitée lors de la prochaine reconnexion**, l'utilisateur est redirigé vers la page qu'il cherchait à atteindre.

**Intérêt pour les Utilisateurs**

| Consultants | Exploitants | Novices |
| :--- | :--- | :--- |
| Offrir un environnement de travail personnel et sécurisé | Offrir un environnement de travail personnel et sécurisé | Offrir un environnement de travail personnel et sécurisé |


### Préférences

L'application doit permettre de définir des préférences pour l'utilisateur :

* La langue utilisée.
* Des modes d'affichage pour les collections (liste, grille, etc).
* Retour à la dernière page visitée lors de la prochaine reconnexion (désactivée par défaut).

A noter : certaines préférences peuvent être prépositionnées dans la configuration globale de l'application (soit graphiquement, par un utilisateur spécial, soit en dur dans des fichiers de configuration).

**Intérêt pour les Utilisateurs :**

| Consultants | Exploitants | Novices |  |
| :--- | :--- | :--- | :--- |
| Confort d'utilisation pour la pagination. S'adapter à de nouvelles topologies très vite. | Passer facilement d'un environnement à un autre (topologie de tests, topologie de production). | Vérifier que Petals, ce n'est pas si compliqué. Une information à fournir et la topologie entière est administrable. |  |


### Déconnexion

Une fois connecté, un utilisateur doit pouvoir se déconnecter, quel que soit l'endroit où il se trouve dans l'application.  

**Intérêt pour les Utilisateurs**

| Consultants | Exploitants | Novices |
| :--- | :--- | :--- |
| Offrir un environnement de travail personnel et sécurisé | Offrir un environnement de travail personnel et sécurisé | Offrir un environnement de travail personnel et sécurisé |


## Espaces de travail

Un **espace de travail** a un nom, une description, en option, une image, ainsi qu'une liste d'utilisateurs autorisés à y accéder.
Il contient également une liste de **bus Petals**, que l'on peut administrer depuis cet espace.

Le nom d'un espace de travail est unique, mais l'espace peut être partagé avec plusieurs utilisateurs.
On doit pouvoir attribuer des droits d'accès à l'espace de travail, et donc pouvoir attribuer des permissions aux utilisateurs sur cet espace
(accès autorisé ou refusé). **Un utilisateur ayant accès à un espace de travail a tous les droits dans cet espace. La gestion des droits pourra
être affinée plus tard.**

> Un espace de travail peut être utilisé pour séparer l'exploitation de différents projets Petals, ou bien l'exploitation de projets
Petals dans des phases différentes (test, pré-production, production).


### Définir un nouvel espace de travail

L'application doit permettre de définir un nouvel espace de travail.  

**Intérêt pour les Utilisateurs**

| Consultants | Exploitants | Novices |
| :--- | :--- | :--- |
| Créer facilement à un environnement de travail. | Répartir des lots de travail dans des espaces dédiés. | S'approprier l'approche projet/utilisateur de Petals Cockpit. |


### Charger un espace de travail

L'application doit permettre de charger un espace de travail.  
L'espace de travail doit apparaître dans une liste qui peut être vide lors de la première utilisation.

Pour chaque espace de travail qui se trouve dans cette liste, le nom des **bus Petals** présents doit apparaître clairement.
La liste des noms des espaces de travail accessibles par l'utilisateur courant doit être présente à tout moment pour effectuer un changement rapide.

**Intérêt pour les Utilisateurs**

| Consultants | Exploitants | Novices |
| :--- | :--- | :--- |
| Accéder à un environnement de travail. | Accéder à un environnement de travail. | Accéder à un environnement de travail. |


### Éditer un espace de travail

L'application doit permettre de modifier les propriétés d'un espace de travail (nom, description).  
Elle doit aussi permettre de modifier la liste des utilisateurs ayant accès à cet espace, et la liste des bus.
Après chaque modification, une notification est envoyée à tous les utilisateurs de l'espace de travail.

Pour les utilisateurs déjà connectés lors de la mise à jour, les changements doivent se répercuter immédiatement dans ce qu'il voit,
sans intervention explicite de sa part.

Cas spécial : si un utilisateur est désassocié d'un espace, alors il doit recevoir une notification l'en informant.
Si cet utilisateur est connecté au moment de son éviction, un message d'erreur doit lui parvenir et le rediriger vers la
page d'accueil de Cockpit.

**Intérêt pour les Utilisateurs**

| Consultants | Exploitants | Novices |
| :--- | :--- | :--- |
| Faciliter l'évolution d'un espace de travail. | Faciliter l'évolution d'un espace de travail. | Corriger des erreurs sans avoir à tout recréer. |


### Quitter un espace de travail

L'application doit permettre de quitter un espace de travail lorsque l'utilisateur se trouve à l'intérieur de celui-ci.
Un message de confirmation doit apparaître lors de cette étape.

Lorsqu'un utilisateur quitte un espace, cela n'a aucun impact sur les autres utilisateurs.

**Intérêt pour les Utilisateurs**

| Consultants | Exploitants | Novices |
| :--- | :--- | :--- |
| Quitter un environnement de travail. | Quitter un environnement de travail. | Quitter un environnement de travail. |


### Supprimer un espace de travail

L'application doit permettre de supprimer un espace de travail.  
Seuls les utilisateurs ayant accès à cet espace peuvent effectuer cette action.
Un message de confirmation doit apparaître lors de cette étape. Une notification est envoyée à tous les
utilisateurs de l'espace de travail une fois l'action effectuée.

Si d'autres utilisateurs sont connectés au moment de la suppression, un message d'erreur doit leur parvenir et les rediriger vers la
page d'accueil de Cockpit. 

Après suppression, un espace de travail peut être restauré.  
En fait, la suppression n'est pas automatique. L'espace supprimé est déplacé dans une corbeille, qui sera vidée automatiquement
au bout de 30 jours. Un message de rappel de la suppression (définitive) sera envoyé tous les 10 jours. Une fois la suppression
effective, un message de confirmation de la suppression sera envoyé.

**Intérêt pour les Utilisateurs**

| Consultants | Exploitants | Novices |
| :--- | :--- | :--- |
| Supprimer un espace devenu inutile. | Supprimer un espace devenu inutile. | Supprimer un espace devenu inutile. |


## Gestion des bus / topologie

Un bus Petals est aussi appelé topologie Petals.  
Un bus est constitué de conteneurs (aussi appelés nœuds) Petals, et d'un annuaire (*registry*) de services, elle-même constituée de
nœuds. On parle donc soit de nœuds Petals, soit de nœuds de l'annuaire de services.


### Importer une topologie

Les topologies ne sont pas définies dans Cockpit : elles dépendent des déploiements qui ont été réalisés.

L'application doit donc permettre d'importer une topologie depuis un espace de travail ouvert.  
Il est nécessaire de compléter un formulaire comprenant une _ip_, un _port JMX_, un _nom utilisateur_, un _mot de passe_ et une _phrase secrète_.
Ces informations permettent de contacter un ou plusieurs nœuds Petals et ainsi d'introspecter la topologie.

Cette opération peut prendre plusieurs minutes.  
Elle peut aussi rencontrer plusieurs erreurs. Il est donc impératif de montrer une barre de progression dans l'interface
graphique. Le résulat de l'opération doit être clairement indiqué à la fin, y compris les erreurs rencontrées en cas d'échec.

D'autres métadonnées doivent être associées à une topologie, comme un nom, une description, et évenutuellement, une image.

**Intérêt pour les Utilisateurs**

| Consultants | Exploitants | Novices |
| :--- | :--- | :--- |
| Découvrir une topologie. | Découvrir une topologie. | Découvrir une topologie. |


### Éditer une topologie

Il doit être possible de mettre à jour les propriétés d'une topologie : nom, description, image, propriétés de connexion.

**Intérêt pour les Utilisateurs**

| Consultants | Exploitants | Novices |
| :--- | :--- | :--- |
| Faciliter la maintenance et l'identification d'une topologie. | Faciliter la maintenance et l'identification d'une topologie. | Faciliter la maintenance et l'identification d'une topologie. |


### Sélectionner une topologie

L'application doit permettre de sélectionner une topologie (déjà importée) dans un espace de travail ouvert.    
Les informations telles que le nom et la description d'une topologie doivent apparaître dans la liste de sélection.

Une fois une topologie sélectionnée, il devient possible d'accéder à la liste des conteneurs et d'administrer cette topologie.

**Intérêt pour les Utilisateurs**

| Consultants | Exploitants | Novices |
| :--- | :--- | :--- |
| Visualiser l'ensemble des topologies. | Accéder à l'administration d'une topologie. | Voir les détails d'une topologie. |


### Visualiser une topologie

Lorsqu'une topologie a été sélectionnée, l'application doit en offrir une vue d'ensemble, au travers d'un graphe \(arbre\).  
Cette représentation doit s'adapter à la taille de l'écran tout en supportant un grand nombre de nœuds.

Pour chaque nœud, le nom du nœud doit apparaître clairement, tout comme les artefacts.
L'affichage des nœuds doit être ordonné par nom de nœud. Enfin, il faut pouvoir filtrer la représentation grâce à un nom d'hôte ou un nom de conteneur, afin de ne pas obligatoirement tout afficher.

**Intérêt pour les Utilisateurs**

| Consultants | Exploitants | Novices |
| :--- | :--- | :--- |
| Découvrir rapidement une topologie en intervention. | Visualiser son domaine d'exploitation dans son ensemble. | S'approprier l'approche distribuée de Petals ESB. |


### Supprimer une topologie

L'application doit permettre de supprimer une topologie.  
Un message de confirmation doit apparaître lors de cette étape.
Une notification est envoyée à tous les utilisateurs de l'espace de travail une fois l'action effectuée.

Si un autre utilisateur est connecté au moment de la suppression, un message d'erreur doit lui parvenir et le rediriger vers la
page d'accueil de l'espace de travail.

**Intérêt pour les Utilisateurs**

| Consultants | Exploitants | Novices |
| :--- | :--- | :--- |
| Supprimer une topologie. | Supprimer une topologie. | Repartir de zéro et réimporter une nouvelle topologie. |



## Gestion d'artefacts sur un nœud Petals

Pour tous les cas d'usage qui suivent, il est supposé qu'une topologie a été sélectionnée dans un espace de travail.


### Visualiser les services d'une topologie Petals

L'application doit permettre de visualiser l'ensemble des services déployés dans l'infrastructure.  
Cette représentation doit s'adapter à la taille de l'écran tout en supportant un grand nombre de **services**, d'**interfaces** et d'**end-points**.
Pour chaque service sélectionné, il faut pouvoir afficher son/ses nom d'interface\(s\), nom de service, et nom d'end-point\(s\).

Pour chaque nom d'interface et de service sélectionné, l'espace de nom et la partie locale doivent apparaître clairement. L'affichage des noms d'interfaces et services doit commencer par la partie locale : `partie-locale - http://espace.de.nom`

La représentation des noms d'interfaces doit apparaître en premier, suivie des noms de services et enfin les noms d'end-points. Il doit être possible de modifier l'ordre de la représentation. L'application doit aussi permettre de filtrer l'arbre selon différents critères. L'application doit permettre de rechercher un élément parmis l'arbre de représentation **Service Endpoint**. Les critères de recherche se limiteront à des infos de déploiement : nom d'interface, nom de service et d'end-point.

**Intérêt pour les Utilisateurs**

| Consultants | Exploitants | Novices |
| :--- | :--- | :--- |
| Lister les services. | Visualiser les services en production dans son ensemble. | S'approprier la notion de service et comprendre ce qui tourne dans Petals. |


### Sélectionner un nom d'interface

L'application doit permettre de sélectionner un nom d'interface depuis l'arbre et de se focaliser dessus.  
Une fois sélectionné, des informations supplémentaires s'affichent (nom du _WSDL_, noms de services, noms d'end-points).

**Intérêt pour les Utilisateurs**

| Consultants | Exploitants | Novices |
| :--- | :--- | :--- |
| Découvrir rapidement l'ensemble des informations rattachées à une interface. | Découvrir rapidement l'ensemble des informations rattachées à une interface. | Découvrir rapidement l'ensemble des informations rattachées à une interface. |


### Sélectionner un nom de service

L'application doit permettre de sélectionner un nom de service depuis l'arbre et de se focaliser dessus.  
Une fois sélectionné, des informations supplémentaires s'affichent (nom du _WSDL_, noms d'interfaces, noms d'end-points).

**Intérêt pour les Utilisateurs**

| Consultants | Exploitants | Novices |
| :--- | :--- | :--- |
| Découvrir rapidement l'ensemble des informations rattachées à un service. | Découvrir rapidement l'ensemble des informations rattachées à un service. | Découvrir rapidement l'ensemble des informations rattachées à un service. |


### Sélectionner un nom d'end-point

L'application doit permettre de sélectionner un nom d'end-point depuis l'arbre et de se focaliser dessus.  
Une fois sélectionné, des informations supplémentaires s'affichent (nom du _WSDL_, noms d'interfaces, noms de service, composant associé et nœud Petals sur lequel il est déployé).

**Intérêt pour les Utilisateurs**

| Consultants | Exploitants | Novices |
| :--- | :--- | :--- |
| Découvrir rapidement l'ensemble des informations rattachées à un end-point. | Découvrir rapidement l'ensemble des informations rattachées à un end-point. | Découvrir rapidement l'ensemble des informations rattachées à un end-point. |


### Lister l'ensemble des artefacts déployés sur un nœud Petals

Pour un nœud donné, l'application doit pouvoir lister les artefacts Petals déployés sur ce nœud.  
Pour chaque artefact, il faut donner son identifiant et son état \(démarré, arrêté...\).

**Intérêt pour les Utilisateurs**

| Consultants | Exploitants | Novices |
| :--- | :--- | :--- |
| Découvrir rapidement ce qui tourne sur un nœud donné. | Voir ce qui est déployé sur un nœud donné. | Comprendre les artefacts Petals et les visualiser une fois déployés. |


### Visualiser les propriétés d'un nœud Petals

Pour un nœud donné, il faut pouvoir lister ses propriétés.  
Ces propriétés sont les suivantes :

* Propriétés du système (OS, JVM).
* Propriétés du nœud Petals, définies dans le fichier **server.properties**.

Il s'agit de visualisation, donc pas de modification à chaud via l'application.

**Intérêt pour les Utilisateurs**

| Consultants | Exploitants | Novices |
| :--- | :--- | :--- | :--- |
| Récupérer les informations utiles sur un nœud, afin d'identifier les causes d'un problème, le tout, de manière centralisée. | Récupérer des informations sur un nœud, le tout, de manière centralisée. Intéressant pour communiquer des informations au support. | Découvrir les propriétés importantes de Petals. |


### Installer un artefact Petals

L'application doit permettre d'installer un ou plusieurs artefacts Petals sur un nœud donné.  
Les artefacts déployables sont librairies partagées, composants, service assemblies et service-units.  
Tant qu'un déploiement n'est pas terminé, l'application ne permet pas d'effectuer un autre déploiement en parallèle.

Le déploiement doit pouvoir se faire depuis un ou plusieurs fichiers en local. Ou bien il doit pouvoir se faire en précisant l'URL de l'artefact à déployer (URL HTTP, [Maven](https://ops4j1.jira.com/wiki/spaces/paxurl/pages/3833866/Mvn+Protocol), etc).

**Intérêt pour les Utilisateurs**

| Consultants | Exploitants | Novices |
| :--- | :--- | :--- | :--- |
| Installer en un clin d'œil des artefacts Petals. | Idéalement, pas utilisé par l'exploitant (pas de déploiement à chaud en production). Mais peut être utilisé pour installer des artefacts. | Pour débuter avec Petals et installer ses premiers artefacts. |


### Désinstaller un artefact Petals

La désinstallation d'artefacts Petals doit se faire simplement depuis leur page, lorsque cet artefact est à l'arrêt.

**Intérêt pour les Utilisateurs**

| Consultants | Exploitants | Novices |
| :--- | :--- | :--- | :--- |
| Désinstaller des artefacts Petals. | Désinstaller des artefacts Petals. Normalement pas utilisé en production. | Désinstaller des artefacts Petals. |


### Modifier le cycle de vie d'un artefact Petals

L'application doit permettre de démarrer, arrêter ou passer en état _shutdown_\(installer\) n'importe quel artefacts Petals déployé sur un nœud.
Pour chaque artefact, une représentation graphique est attendue, et illustrant l'état actuel et les états possibles.

**Intérêt pour les Utilisateurs**

| Consultants | Exploitants | Novices |
| :--- | :--- | :--- | :--- |
| Jouer sur le cycle de vie des artefacts (utile par exemple pour recharger des paramètres). | Jouer sur le cycle de vie des artefacts (utile par exemple pour recharger des paramètres). | Jouer sur le cycle de vie des artefacts. | 


### Modifier à chaud des paramètres de Petals

Les composants Petals héritent, au travers du CDK, de certains paramètres configurables.  
Les paramètres suivants devraient être modifiables à chaud \(_during runtime_\) depuis le cycle de vie du composant :

* acceptor-pool-size
* acceptor-stop-max-wait
* processor-keep-alive-time
* processor-max-pool-size
* processor-pool-size
* processor-stop-max-wait

De la même façon, il y a dans le conteneur des paramètres accessibles et utiles (transporteur, routeur) :

* http-port
* https-enabled

D'autres paramètres pourront être rajoutés plus tard (à terme, tous devraient être supportés par l'application).

**Intérêt pour les Utilisateurs :**

| Consultants | Exploitants | Novices |  |
| :--- | :--- | :--- | :--- |
| Utile pour tuner des composants Petals. | Adapter les taille des pools aux besoins de production \(ajustements\). Modifier des propriétés du composant. | Voir ce qui est paramétrable. |  |


### Modifier à chaud des niveaux de log

L'application doit permettre de modifier à chaud les niveaux de log des composants Petals.  
Elle doit aussi permettre de modifier à chaud les niveaux de log pour des modules du conteneur.  
Avant modification, il faut bien sûr afficher le niveau de log actuel.

**Intérêt pour les Utilisateurs :**

| Consultants | Exploitants | Novices |  |
| :--- | :--- | :--- | :--- |
| Extrêmement utile pour diagnostiquer des problèmes. | Diagnostiquer des problèmes, suivre les indications du support. | Vérifier la dynamicité des traces dans Petals ESB. |  |
