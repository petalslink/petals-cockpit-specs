# Gestion des Erreurs

Les scénarios mis en avant dans les tâches comportent des cas d'erreur.  
Ces cas correspondent à des erreurs fonctionnelles. En revanche, ces scénarios n'intègrent pas la gestion des erreurs techniques \(telle qu'une coupure réseau ou la chute d'un nœud alors qu'une opération d'administration est en cours\).

L'apparition d'une stack d'erreur Java dans une page web est inacceptable.  
Les erreurs techniques doivent toutes êtres récupérées par l'application.

Un message intelligible doit être adressé à l'utilisateur pour lui signifier qu'une erreur technique est survenue. On tentera, dans la mesure du possible, de fournir une explication simple sur la nature de cette erreur. Il sera proposé à l'utilisateur de rafraîchir la page d'ici quelques instants. Ce rafraîchissement peut même être effectué automatiquement par l'application ou le navigateur web.

Une trace plus avancée, pour le support, devra être laissée dans les logs de l'application.

