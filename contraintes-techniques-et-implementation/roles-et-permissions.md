---
description: >-
  Description des permissions, des rôles qui les contiennent ainsi que des
  fonctionnalités dont elles restreignent l'accès.
---

# Rôles et permissions

L'accès aux ressources et actions doivent être restreintes dans Cockpit. D'une part pour limiter les diverses administrations \(techniques et métier\) aux personnes responsables, d'autre part pour protéger les données sensibles \(production par exemple\). Ici sont listés les différentes **permissions** à accorder ainsi que la description du **rôle** **administrateur cockpit**.

### Précisions préliminaires

Les permissions ne font pas uniquement références aux fonctionnalités existantes ou spécifiés, mais aussi aux fonctionnalités à venir. Ces dernières sont, de fait, mal définies. Il est cependant nécessaire de déjà les lister afin d'en comprendre l'intention. Certains rôles n'existeront pas tant que les fonctionnalités et permissions correspondantes ne seront pas implémentés.

Il faut noter aussi, que **les permissions sont attribués a un couple utilisateur + espace de travail**. Un permission n'autorise donc des actions qu'au sein d'un espace de travail. Un même utilisateur peut avoir une même permission sur différent espaces et ne pas l'avoir sur d'autres. Les espaces de travail sont considérés totalement indépendants, sans considération des bus qui y sont attachés \(un même bus peut être attaché à différents espaces\).

## Permissions:

Une permission donne accès a une fonctionnalité jugée sensible sur un espace de travail.

### liste des permissions

* **administration workspace** ajouter supprimer utilisateurs d'un workspace, attribution de permissions aux utilisateurs du workspace \(effectives sur ce workspace\), edition de description et short description du workspace. Suppression du workspace.
* **attacher/détacher un bus** d'un espace de travail.
* **attacher/détacher un conteneur** d'un bus de l'espace de travail.
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

Il n'y a qu'un rôle, il est attribué à un ou plusieurs utilisateur de cockpit, et est effectif globalement sur toute l'application :

* **administrateur cockpit:** administrateur technique de cockpit, au niveau global. Dispose de la permission _administration workspace_ ****sur tous les espaces. Il est le seul utilisateur de cockpit qui peut visualiser n'importe quel espace et jouir des droits accordés par la permissions _administration workspace_ sans faire nécessairement partie de ses membres. Cependant afin d’effectuer des actions protégées par d'autres permissions sur un espace, il doit au préalable s'ajouter aux membre et s'accorder la permission associée. 

## Attribution des rôles & permissions

* Tout utilisateur de cockpit peut créer un espace de travail, il reçoit automatiquement **toute les permissions sur cet espace**. 
* Le premier rôle d'**administrateur cockpit**  peut être donné à l'aide d'un token \(affiché dans la console de l'application\) lors du lancement du backend \(si aucun **administrateur cockpit** n'existe\). Ou bien inséré directement en DB grâce à la commande _add-user_.
* Le dernier administrateur cockpit ne peut pas être supprimé des utilisateurs de cockpit \(il doit donner le rôle à au moins un autre utilisateur avant\).
* Un workspace doit forcément avoir un de ses membres qui dispose de la permission _administration workspace._ Si il n'y a qu'un membre de l'espace qui dispose de cette permission, il ne peut pas être supprimé des membres de l'espace en question \(il doit donner le rôle à au moins un autre membre avant\).

