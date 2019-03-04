# Ouvrir un espace de travail depuis un autre espace

{% hint style="info" %}
La notation suivante est prise :
{% endhint %}

* \[ tâche \] fait référence à une autre tâche.
* Action \(sans crochets\) fait référence à une action utilisateur.

Concepts associés : un **Espace de Travail**.  
Préconditions : [\[ Se Connecter \]](se-connecter.md) [\[](charger-un-espace-de-travail.md)[ Ouvrir un espace de travail \]](charger-un-espace-de-travail.md)  
Postconditions : -  
Contraintes : -  
Complexité : -

### Scénario

{% hint style="info" %}
Dans un scénario, on ne mentionne pas les actions techniques \(pas de clic, de tooltip, etc\).
{% endhint %}

**Scénario normal :** Albert est connecté à un espace de travail, il ouvre le menu déroulant et sélectionne son nouvel espace de travail parmis la liste. Il est redirigé vers la page [visualiser](visualiser-un-espace-de-travail.md) de ce dernier.

### Maquette

![Menu d&#xE9;roulant accessible depuis un espace de travail](../../.gitbook/assets/proposition-fil-d-ariane-6.png)



### Informations complémentaires pour implémentation

* La liste des espaces de travail dans le menu déroulant ne contient que les espaces de travail auquel l'utilisateur a accès.
  * L'espace courant est présent dans la liste et mis en évidence \(ombrage, highlight, focus ...\). Cliquer dessus amène au détail de ce dernier.
  * Les autres espaces auxquels l'utilisateur a accès \(dont il est membre\) son presents mais non mis en évidence. Cliquer dessus fait quitter l'espace actuel et redirige l'utilisateur sur la page principale du nouvel espace de travail.
* Il n'y a pas de confirmation à donner lorsqu'on clique sur un des espaces de la liste, la redirection est immédiate.

