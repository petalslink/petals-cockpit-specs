# Ouvrir un espace de travail depuis un autre espace

{% hint style="info" %}
La notation suivante est prise :
{% endhint %}

* \[ tâche \] fait référence à une autre tâche.
* Action \(sans crochets\) fait référence à une action utilisateur.

Concepts associés : un **Espace de Travail**.  
Préconditions : [\[](charger-un-espace-de-travail.md)[ Ouvrir un espace de travail \]](charger-un-espace-de-travail.md)  
Postconditions : -  
Contraintes : -  
Complexité : -

### Scénario

**scénario normal:** Albert est connecté à un espace de travail, il ouvre le menu déroulant et choisi son nouvel espace de travail. Il est redirigé vers la page [visualiser](visualiser-un-espace-de-travail.md) de ce dernier.



### Maquette

![Menu d&#xE9;roulant](../../.gitbook/assets/header-menu-workspaces.png)



### Remarque

* La liste des espaces du menu déroulant ne contient que les espaces de travail auquel l'utilisateur a accès.
  * L'espace courant est présent dans la liste et mis en évidence \(ombrage, highlight, focus ...\). Cliquer dessus amène au détail de ce dernier.
  * Les autres espaces auxquels l'utilisateur a accès \(dont il est membre\) son presents lmais non mis en évidence. Cliquer dessus fait quitter l'espace actuel et amène sur la page détail du nouvel espace.
* Il n'y a pas de confirmation à donner lorsqu'on clique sur un des espaces de la liste, la redirection est immédiate.

