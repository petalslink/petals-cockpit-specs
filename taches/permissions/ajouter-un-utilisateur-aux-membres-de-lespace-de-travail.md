# Ajouter un utilisateur aux membres de l'espace de travail

{% hint style="info" %}
La notation suivante est prise :
{% endhint %}

* \[ tâche \] fait référence à une autre tâche.
* Action \(sans crochets\) fait référence à une action utilisateur.

Concepts associés : un **Espace de Travail**.  
Préconditions : [\[ Se Connecter \]](../espace-de-travail/se-connecter.md) [\[ Visualiser un espace de travail \]](../espace-de-travail/visualiser-un-espace-de-travail.md)  
Postconditions : -  
Contraintes : -  
Complexité : -

### Scénario

{% hint style="info" %}
Dans un scénario, on ne mentionne pas les actions techniques \(pas de clic, de tooltip, etc\).
{% endhint %}

**Scénario normal:** Albert veut éditer les informations de l'espace de travail pour mettre à jour la liste des membres ayant accès à l'espace de travail. Il souhaite ajouter un nouveau membre. Il saisi le nom filtré, sélectionne l'utilisateur parmi la liste déroulante, et ajoute le nouveau membre. La liste est mise à jour lorsque l'utilisateur est ajouté à l'espace de travail.

### Maquettes

![Ajouter un nouvel utilisateur &#xE0; l&apos;espace de travail](../../.gitbook/assets/workspace-overview-add-user.png)

![Nouveau membre du groupe de l&apos;espace de travail ajout&#xE9;](../../.gitbook/assets/workspace-overview-member-add.png)

### Information complémentaire pour implémentation

* Il faut disposer des permissions suffisante pour pouvoir ajouter un membre à l'espace de travail.
* Un membre ne peut-être ajouté que s'il est présent dans la liste filtrée.

