# Ouvrir un espace de travail

{% hint style="info" %}
La notation suivante est prise :
{% endhint %}

* \[ tâche \] fait référence à une autre tâche.
* Action \(sans crochets\) fait référence à une action utilisateur.

Concepts associés : un **Espace de Travail**.  
Préconditions : [\[ Se connecter \]](se-connecter.md)  
Postconditions : [\[ Visualiser un Espace de Travail \]](visualiser-un-espace-de-travail.md)  
Contraintes : -  
Complexité : -

### Scénarios

{% hint style="info" %}
Dans un scénario, on ne mentionne pas les actions techniques \(pas de clic, de tooltip, etc\).
{% endhint %}

**Scénario normal :** Albert veut sélectionner un espace de travail pour travailler. Plusieurs sont listés. Il sélectionne celui qui s'appelle **pre-prod** et valide son choix. ￼  
  
**Scénario alternatif 1 :** Albert veut sélectionner un espace de travail pour travailler. Aucun n'est listé. Il peut donc soit [créer un nouvel espace de travail](definir-un-espace-de-travail.md), soit [se déconnecter](se-deconnecter.md). ￼  
  
**￼Scénario alternatif 2 :** Albert veut sélectionner un espace de travail pour travailler. Plusieurs sont listés. Il sélectionne celui qui s'appelle **pre-prod** mais ne peut valider son choix. En effet, il n'a pas les droits suffisants. Il peut toutefois récupérer le nom de l'administrateur de cet espace pour prendre contact avec lui.

### Maquettes

![Page d&apos;accueil des espaces de travail \(vide\)](../../.gitbook/assets/vue-no-workspace.png)

![Page d&apos;accueil des espaces de travail](../../.gitbook/assets/workspace-select-v3.png)

### Informations complémentaires pour implémentation

* La sélection d'un espace de travail se fait par simple clic sur la zone qui lui est dédiée dans la liste.
* Une icône utilisateur est attaché à chaque espace de travail indiquant le nombre de personnes y ayant accès.
* Survoler l'icône utilisateurs permet d'afficher un _tooltip_ avec le nom de son ou ses administrateurs. 
* La liste des espaces est triée. Ceux auxquels l'utilisateur a accès sont listés en premier. Les autres viennent après.
* Une icône \(ou un fond de couleur différente\) marque différemment les espaces auxquels l'utilisateur n'a pas accès.
* La description affichée dans un espace de travail sera courte et limité à peu de caractères. 
* Une description plus complète sans limitation de caractères sera présente dans la vue d'un espace de travail sélectionné. Par défaut, la description sera vide.

{% hint style="info" %}
Pour l'instant, l'utilisateur ne voit que les espaces de travail auxquels il peut accéder. Le survol du badge indique le nom de tout les utilisateurs de l'espace de travail et la notion d'administrateur ainsi que les droits d'accès sera implémentées plus tard.
{% endhint %}

{% hint style="warning" %}
Faire la distinction entre une _description détaillée_ et une _description bref_ d'un espace de travail pour ne pas surcharger la vue et faciliter la lecture des espaces de travail dans la liste.
{% endhint %}

