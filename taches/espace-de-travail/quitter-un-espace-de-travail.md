# Fermer un espace de travail

{% hint style="info" %}
La notation suivante est prise :
{% endhint %}

* \[ tâche \] fait référence à une autre tâche.
* Action \(sans crochets\) fait référence à une action utilisateur.

Concepts associés : un **Espace de Travail**.  
Préconditions : [\[ Se Connecter \]](se-connecter.md) [\[ Ouvrir un Espace de Travail \]](charger-un-espace-de-travail.md)  
Postconditions : [\[ Ouvrir un espace de travail \]](charger-un-espace-de-travail.md)  
Contraintes : -  
Complexité : -

{% hint style="warning" %}
"Fermer" un espace de travail signifie s'en déconnecter. A la fin de l'action, l'espace de travail n'est pas impacté et l'utilisateur fait toujours partie des membres y aillant accès.
{% endhint %}

### Scénario

{% hint style="info" %}
Dans un scénario, on ne mentionne pas les actions techniques \(pas de clic, de tooltip, etc\).
{% endhint %}

**Scénario normal :** Albert veut quitter son espace de travail, il ouvre le menu déroulant et retourne à la page de selection d'espaces.

### Maquette

![Menu d&#xE9;roulant accessible depuis un espace de travail](../../.gitbook/assets/proposition-fil-d-ariane-6.png)

### Information complémentaire pour implémentation

* Il n'y a pas de demande de confirmation pour fermer l'espace courant.

