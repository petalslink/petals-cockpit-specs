---
description: >-
  Description des permissions, des rôles qui les contiennent ainsi que des
  fonctionnalités dont elles restreignent l'accès.
---

# Rôles et permissions

L'accès aux ressources et actions doivent être restreintes dans Cockpit. D'une part pour limiter les diverses administrations \(techniques et métier\) aux personnes responsables, d'autre part pour protéger les données sensibles \(production par exemple\). Ici sont listés les différentes **permissions** à accorder ainsi que les **rôles** qui groupent ces permissions.

### Précisions préliminaires

Les permissions ne font pas uniquement références aux fonctionnalités existantes ou spécifiés, mais aussi aux fonctionnalités à venir. Ces dernières sont, de fait, mal définies. Il est cependant nécessaire de déjà les lister afin d'en comprendre l'intention. Certains rôles n'existeront pas tant que les fonctionnalités et permissions correspondantes ne seront pas implémentés.

Il faut noter aussi, que **les rôles/permissions sont attribués a un couple utilisateur + espace de travail** **mis à part le rôle d’**_**administrateur cockpit**_ **qui est global**. Le contextuel d'_administrateur workspace_  est lié à un utilisateur **et** un espace, il en va de même pour les permissions. Un rôle n'attribue donc des permissions qu'au sein d'un espace de travail. Un même utilisateur pourra donc avoir un même rôle sur différent espaces et ne pas l'avoir sur d'autres.

## Permissions:

### liste des permissions

* **administration cockpit** ajouter supprimer utilisateurs de cockpit. Attribution du rôle administrateur cockpit. Paramètres généraux de l'application.
* **administration workspace** ajouter supprimer utilisateurs d'un workspace, attribution de rôle liés au workspace, edition de description et short description du workspace. Suppression du workspace.
* **attacher/détacher un bus** d'un espace de travail
* **attacher/détacher un conteneur** d'un bus
* **deploy, undeploy d'un artefact jbi + paramètres** deploy, undeploy un artefact jbi \(Composant, SA, SL\). Modification des paramètres des artefacts \(à chaud ou au déploiement\).
* **gestion cycle de vie d'un artefact jbi** start, stop, shutdown... un artefact jbi \(Composant, SA, SL\).
* **modification du niveau de log** d'un artefact ou d'un container.
* **édition de modèle** _sans considérer la manière dont la fonctionnalité sera intégrée à l'interface:_ création et __modification d'un modèle de déploiement logique dans cockpit.
* **déployer un modèle** appliquer un modèle logique à une topologie \(déploiement physique sur des conteneurs\).
* **administration flux** le détail de ce qu'est un flux \(ou service, flow, process\) reste à définir. Cette feature concerne principalement le contrôle et le rejeu de processus métier \(spécifiques à des SE type flowable\)
* **visualisation/recherche des traces monit:** visualiser dans cockpit les traces monit des conteneurs.

### remarques

L'accès aux différentes vues d'un espace de travail \(topologie, services, api, modèle, monitoring\) ne fait pas partie des permissions, il n'est pas limité en soi. Une fois que l'on a accès à l'espace de travail on a accès à ces vues. Les actions ou ressources proposés par ces vues peuvent cependant être limités.

## Rôles

### liste des rôles

* **administrateur workspace:** généralement le créateur du workspace ou chef de projet. A toute les permissions sur un workspace, notamment celle de donner les rôles et permissions sur le workspace. 
* **administrateur cockpit:** administrateur technique de cockpit, au niveau global. 

## Association rôle - permission

| perm/role | admin cpt | admin wksp |
| :--- | :--- | :--- |
| **admin globale** | ✔ |  |
| **admin wksp** | ✔ | ✔ |
| **att/det bus** |  | ✔ |
| **att/det cont** |  | ✔ |
| **lifecycle art** |  | ✔ |
| **deploy/param art** |  | ✔ |
| **niveau logs** |  | ✔ |
| **edit modèle** |  | ✔ |
| **deploy modèle** |  | ✔ |
| **admin flux** |  | ✔ |
| **traces monit** |  | ✔ |

## Attribution des rôles & permissions

* Tout utilisateur de cockpit peut créer un espace de travail, il devient alors automatiquement **administrateur d'espace de travail** de cet espace. 
* Tout **administrateur d'espace de travail** peut attribuer des permissions aux utilisateur de l'espace de travail.
* Le premier rôle d'**administrateur cockpit**  peut être donné à l'aide d'un token \(affiché dans la console de l'application\) lors du lancement du backend \(si aucun **administrateur cockpit** n'existe\). Ou bien inséré directement en DB grâce à une commande.
* Le dernier administrateur cockpit ne peut pas être supprimé des utilisateurs \(il doit donner le rôle à au moins un autre utilisateur avant\).
* Le dernier administrateur workspace ne peut pas être supprimé des utilisateurs du workspace en question \(il doit donner le rôle à au moins un autre utilisateur avant\).

