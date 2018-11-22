# Contraintes Techniques

* L'application doit s'appuyer sur le guide [Material Design](https://material.io/design/) et respecter la charte graphique établie.
* L'application doit produire des pages HTML valides (vérification W3C).
* L'application doit intégrer une extension du CSS (Sass) pour simplifier et optimiser dans le mesure du possible un CSS complexe ou répétitif.
* Interdiction d'utiliser des images pour faire des cadres ou des sections aux angles arrondis.
* L'application doit être internationalisée (français et anglais).
* L'application doit tourner sous Firefox, Chrome et Safari.
* Les interactions entre Petals et l'application se feront au travers de JMX ou bien via HTTP.
* L'application doit être codée en Java pour le *back-end*, et en Javascript (ou l'un de ses dérivés) pour le *front-end*.
* L'application doit pouvoir être ajoutée à un serveur d'intégration continue (Jenkins).
* L'application doit pouvoir être testée de manière automatique (Selenium ou équivalent).
* L'application doit être déployable sur un serveur Tomcat.
* Le packaging de l'application doit être au format WAR.
* Le poids de l'application ne doit pas excéder 15 Mo.

Sur ce dernier point, une taille supérieure justifierait des questions sur la pertinence de la technologie d'implémentation choisie et sur son fonctionnement (une solution pure JSP + Servlet ferait moins de 2 Mo, ressources incluses).

* La notion de session d'utilisation doit être supportée.
* Le support de la haute disponibilité n'a pas à être garanti.

Il n'est pas attendu que l'application puisse tourner sur un cluster de serveurs d'applications.    
En revanche, on tentera d'utiliser les solutions les plus simples et les plus courantes possibles pour réduire les développements à mettre en œuvre si ce besoin venait à venir.
