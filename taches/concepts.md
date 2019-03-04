# Concepts

Les concepts sont les objets manipulés par l'utilisateur dans l'application.  
Dans notre application, il y a **5 concepts essentiels** :

* Un **espace de travail** est l'entité qui préserve le projet et son contenu. Nous pouvons représenter cela comme un répertoire. Il vise à gérer les différents éléments qui composent l'espace de travail : notamment l'importation d'un ou plusieurs bus Petals et la configuration des éléments qui s'y rapportent ainsi que la consultation des services existants.
* La **topologie** décrit un bus Petals. Elle est se compose d'un ensemble de containers Petals et d'un ensemble de membre de Registry Petals. On peut étendre son concept aux artefacts déployés sur les containers Petals.
* Un **conteneur** Petals est un membre de la topologie du bus sur lesquels les consommateurs et fournisseurs de services sont déployés et exécutés. Un conteneur est identifié par un nom. Il est associé à un nom d'hôte et un port JMX. Deux conteneurs peuvent avoir le même hôte, mais des ports différents. Et des noms différents aussi.
* Le **membre du registre** Petals assure le maintient de l'annuaire des services déployés sur le bus, avec leur localisation.
* Les **artéfacts** déployés sur un container Petals sont un ensemble de runtime et de configurations proposant consommateurs et fournisseurs de services. Ils se classent en 4 catégories :
  * Les **composants** qui sont des moteurs d'exécution auquel une configuration doit être adjointe afin d'implémenter consommateurs et fournisseurs de services. Deux natures de composants existent : les _binding-components_ qui sont des moteurs d'exécution faisant office de connecteurs, et les _service-engines_ qui sont des moteurs de services n'ayant aucun lien avec l'extérieur de l'ESB.
  * Les **service-units** sont des configurations permettant de configurer un composant afin d'implémenter consommateurs et fournisseurs de services.
  * Les **librairies partagées** sont des librairies associées aux composants afin de pouvoir leur ajouter un ensemble de classes nécessaires à la bonne exécution des configurations de services telles que des drivers JDBC, JMS, ...
  * Les **service-assemblies** sont les archives permettant de déployer une ou plusieurs service-units sur un container Petals.

À noter que l'accès à un espace de travail et donc à une topologie existante est limité à ses utilisateurs.

Il est important de remarquer qu'il y a une hiérarchie dans ces concepts.  
La topologie est la racine de tout. C'est un ensemble de nœuds.  
Au niveau en-dessous, on trouve le nœud Petals, qui est constitué d'un conteneur et d'artefacts. Et ces artefacts se décomposent, on l'a vu, en différentes catégories.  
Les services sont également rattachés à un nœud **Petals**.

Cette hiérarchie doit être respectée dans l'application.  
Elle doit fonctionner sur ce principe d'introspection, de zoom. Pour accéder à un niveau, on doit passer par celui du dessus. Cet aspect est fondamental pour la facilité d'apprentissage et d'utilisation de cette application, mais aussi pour appréhender Petals ESB dans sa globalité. En plus d'être utile, cet outil doit être pédagogique \(pré-requis pour les utilisateurs de type novices\).

C'est aussi avec cette approche à niveaux que nous allons classer les tâches.

