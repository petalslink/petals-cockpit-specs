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

**Scénario alternatif 1 :** Albert veut consulter les dernières actions effectuer par les utilisateurs de l'espace de travail courant. Il voit le nom des utilisateurs et le type d'action effectué. Il voit également depuis combien de temps l'action a été réalisé. Albert sélectionne les dernières actions puis les marque comme lus.

### Maquettes

![Page d&apos;accueil d&apos;un espace de travail ouvert \(vue administrateur\)](../../.gitbook/assets/workspace-overview-1.png)

![&#xC9;dition des descriptions de l&apos;espace de travail ](../../.gitbook/assets/workspace-overview-edit-description.png)

![Menu d&#xE9;roulant accessible depuis un espace de travail](../../.gitbook/assets/workspace-overview-menu.png)

### Informations complémentaires pour implémentation

* Il faut disposer des permissions suffisante pour pouvoir modifier les descriptions d'un espace de travail.
* Les actions sont triées par ordre de dernière modification.

Pour visualiser un espace, l'utilisateur peut :

* Le sélectionner depuis la vue [\[ Charger un espace de travail \]](charger-un-espace-de-travail.md).
* Le sélectionner depuis le menu déroulant.
* Lorsqu'il est connecté, cliquer sur le nom de l'espace de travail dans le fil d'Ariane.

La description supporte le format markdown pour améliorer sa mis en page et dispose d'une prévisualisation lors de son édition.  
Les maquettes réalisées impliquent que l'utilisateur dispose des permissions suffisantes et d'un rôle d'administrateur.

