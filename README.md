## <samp>Les Questions pour un entretien profile JAVA/JEE!</samp>

#### Partie 5: Programmation Réactive en Java

- 1 . Deux modèles de programmation :
  * 	Modèle multi threads bloquant
    *  Programmation impérative.
    *  Basé sur un pool de threads.
    *  Les entrées sorties bloquants
  * 	Modèle single thread non bloquant 
    *  Programmation Réactive.
    *  IO selector thread et des workers
    *  Les entrées sorties non bloquants (NIO java 7).  
    *  Je dépends à la Tence des clients.

- 2 .	Nodjs : c’est la première téchnologie qui a introduit la programmation asynchrone en se basant sur le pattern Reactor.

- 3 .  Programmation Réactive : Modèle de programmation basé sur les événements en utilisant une séquence d’observables (Streams).

- 4 .	Streams : Les flux de données sont simplement des quantités continues de données. Cela peut être n'importe quoi, des appels de service RESTful, des listes de données provenant d'une base de données, etc.

- 5 . Operations sur streams.
  * 	Intermediate operation: Renvoyer un nouveau flux sur lequel un traitement ultérieur peut être effectué.
    *  map(): produit un nouveau flux après avoir appliqué une fonction à chaque élément du flux d'origine. Le nouveau flux pourrait être de type différent.
    *  filter(): cela produit un nouveau flux qui contient des éléments du flux d'origine qui réussissent un test donné (spécifié par un prédicat).
  * 	Terminal operation: Marquer le flux comme consommé, après quoi il ne peut plus être utilisé.
    *  forEach(): il boucle sur les éléments du flux.
    *  collect(): nous collectons tous les éléments du flux dans une liste.

- 6 .	La différence entre Map et flatMap : 
  * 	Map : Transformer les objets d'un flux en un autre type d'objets.
  * 	FlatMap : FlatMap transforme chaque élément du flux en un flux d'autres objets.

- 7 . Deux API pour travailler avec la programmation réactive :
  * 	Reactive Streams : est une API pour développer des applications réactive, implementations : Reactor de Spring (pivotal), Vertx de Java.
  * 	Reactive X : est une API pour développer des applications réactive, implementations (RxJs, RxJava)

- 8 .	Publisher: est celui qui va émettre les données

- 9 .	Subscriber : est celui qui va les recevoir en s’abonnant au Publisher.

- 10 .	Backpressure : c’est le subscriber qui va décider combien de données qu’il va recevoir.

- 11 .	L’échange de données entre Publisher et Subscribe va se terminer par :
  *  	Complete : si tout se passe bien
  * 	Error : si il ya un problème.

- 12 .	Reactor : Est la bibliothèque réactive de choix pour Spring. Se compose principalement de deux types de Stream.
  * 	Flux<T>: Un Publisher correspondant à un échange de 1 à plusieurs éléments.
  * 	Mono<T> : Un Publisher correspondant à un échange de 0 à 1 élément.

- 13 .	Spring webflux : est un projet spring introduit pour prendre en charge la programmation réactive dans le Web. C'est une alternative à Spring MVC qui est basée sur Servlet, Il a été introduit pour la première fois avec Spring 5. (spring-boot-starter-webflux)
	
- 14 . Pouvons-nous exécuter des applications Spring Webflux sur Tomcat ?
La seule exigence est que le serveur soit conforme à la spécification Servlet 3.1+. Cependant, les applications Spring Webflux sont généralement déployées sur des serveurs Web tels que Netty et Undertow.
	
- 15 .  Quel est le cas d'utilisation de Spring Webflux ?
Nous devrions l'utiliser lorsque nous voulons construire des systèmes qui sont résistants à une charge élevée. avec un nombre reduit de threads.

- 16 .	WebClient : Api qui permet d’accéder des services distants d’une manière réactive, est une alternative au classique RestTemplate.


