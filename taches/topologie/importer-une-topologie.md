# Importer une topologie

{% hint style="info" %}
La notation suivante est prise :

* \[ tâche \] fait référence à une autre tâche.
* Action \(sans crochets\) fait référence à une action utilisateur.
{% endhint %}

Concepts associés : un **Espace de Travail**, une **Topologie**.  
Préconditions : \[ [Charger un Espace de Travail](../espace-de-travail/charger-un-espace-de-travail.md) \]  
Postconditions : -  
Contraintes : -  
Complexité : -

Scénario normal : Bertrand \[ [charge un espace de travail](https://petals.gitbook.io/petals-cockpit-specs/~/drafts/-LRuomoM7dXVloqg5wXd/primary/v/docs-wip/taches/espace-de-travail/charger-un-espace-de-travail) \]. Il est redirigé vers la dernière topologie sélectionnée. Un ensemble de nœuds Petals apparaît sur la page topologie. Bertrand va sur la page d'importation de bus. Il ajoute les informations requises du formulaire \(_ip_, _port_, _id_, _mot de passe_, _phrase secrète_\) et importe sa topologie. Une barre de chargement apparaît indiquant la progression de l'importation en cours. Une fenêtre apparaît et indique que l'importation s'est bien effectuée. Bertrand est redirigé vers la page de sa topologie.

Scénario alternatif : Bertrand \[ [définit un nouvel espace de travail](https://petals.gitbook.io/petals-cockpit-specs/~/drafts/-LRuomoM7dXVloqg5wXd/primary/v/docs-wip/taches/espace-de-travail/definir-un-espace-de-travail) \]. Bertrand est redirigé vers la page d'importation. Une fenêtre apparaît lui indique qu'aucune topologie n'est présente sur l'espace de travail. Bertrand [importe sa topologie](https://petals.gitbook.io/petals-cockpit-specs/~/drafts/-LRuomoM7dXVloqg5wXd/primary/v/docs-wip/taches/topologie/importer-une-topologie) avec succès et ensemble de nœuds Petals apparaît alors sur la page topologie.

Scénario d'erreur : Bertrand \[ [charge un espace de travail](https://petals.gitbook.io/petals-cockpit-specs/~/drafts/-LRuomoM7dXVloqg5wXd/primary/v/docs-wip/taches/espace-de-travail/charger-un-espace-de-travail) \]. Bertrand va sur la page d'importation de bus. Il ajoute les informations requises du formulaire \(_ip_, _port_, _id_, _mot de passe_, _phrase secrète_\) et importe sa topologie. Une barre de chargement apparaît indiquant la progression de l'importation en cours. Un message clair lui indique qu'une erreur est survenue lors de l'importation.

