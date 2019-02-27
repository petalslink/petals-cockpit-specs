# Visualiser un espace de travail

{% hint style="info" %}
La notation suivante est prise :
{% endhint %}

* \[ tâche \] fait référence à une autre tâche.
* Action \(sans crochets\) fait référence à une action utilisateur.

Concepts associés : un **Espace de Travail**.  
Préconditions : [\[ Se Connecter \]](se-connecter.md) [\[ Ouvrir un espace de travail \]](charger-un-espace-de-travail.md)  
Postconditions : -  
Contraintes : -  
Complexité : -

### Scénarios

{% hint style="info" %}
Dans un scénario, on ne mentionne pas les actions techniques \(pas de clic, de tooltip, etc\). 
{% endhint %}

**Scénario normal :** Albert veut éditer les informations de l'espace de travail pour mettre à jour la description bref ou détaillée. Il édite le contenu, modifie le texte, et valide son changement. Il peut toujours annuler son action s'il ne souhaite pas effectuer les modifications en cours.

**Scénario alternatif 1 :** Albert veut éditer les informations de l'espace de travail pour mettre à jour la liste des membres ayant accès à l'espace de travail. Il souhaite ajouter un nouveau membre. Il saisi le nom filtré, sélectionne l'utilisateur parmi la liste déroulante, et ajoute le nouveau membre. La liste est mis à jour.

**Scénario alternatif 2 :** Albert veut éditer les informations de l'espace de travail pour mettre à jour la liste des membres ayant accès à l'espace de travail. Il souhaite supprimer un nouveau membre. Il cherche le membre parmi la liste et le supprime à l'aide de l’icône de suppression. La liste est mise à jour.

**Scénario alternatif 3 :** Albert veut importer un bus dans l'espace de travail courant. Il ajoute les informations pré-requises et importe le bus. \(étape suivante à définir\)

### Maquettes

![Page d&apos;accueil d&apos;un espace de travail ouvert](../../.gitbook/assets/workspace-overview%20%281%29.png)

![Page d&apos;accueil d&apos;un espace de travail ouvert \(&#xE9;dition\)](../../.gitbook/assets/workspace-overview-edit.png)

![Menu d&#xE9;roulant accessible depuis un espace de travail](../../.gitbook/assets/workspace-overview-menu.png)

### Remarque

Pour visualiser un espace, l'utilisateur peut :

* Le sélectionner depuis la vue [\[ Charger un espace de travail \]](charger-un-espace-de-travail.md).
* Le sélectionner depuis le menu déroulant.
* Lorsqu'il est connecté, cliquer sur le nom de l'espace de travail dans le fil d'Ariane.

La description supporte le format markdown pour améliorer sa mis en page et dispose d'une prévisualisation lors de son édition.

