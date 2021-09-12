## <samp>Les Questions pour un entretien profile JAVA/JEE!</samp>

#### Partie 5: Programmation Réactive en Java

- 1 . Deux modèles de programmation :
  * 	Modèle multi threads bloquant : 
    *  Programmation impérative.
    *  Basé sur un pool de threads.
    *  Les entrées sorties bloquants
  * 	Modèle single thread non bloquant : 
    *  Programmation Réactive.
    *  On a IO selector thread et des workers
    *  Les entrées sorties non bloquants (NIO java 7).  
    *  Je dépends à la Tence des clients.

- 2 . Programmation Réactive : Modèle de programmation basé sur les événements en utilisant une séquence d’observables.

- 3 .	Stream : Un flux est une séquence d'événements en cours classés dans le temps. Il peut émettre trois choses différentes : une valeur (d'un certain type), une « error » ou un signal « completed».
	
- 4 .	Nodjs : c’est la première technologie qui a introduit la programmation asynchrone en se basant sur le pattern Reactor.

- 5 . Api Servlet réactive: à partir de l’API servlet 3.1+ on a des servlets avec inputs/outputs non bloquant.

- 6 . Deux API pour travailler avec la programmation réactive :
  * 	Reactive Streams : Implementations ( Reactor de Spring (pivotal), Vertx de Java)
  * 	Réactive X : Implementations (RxJs, RxJava)

- 7 . Spring WebFlux:

- 8 .	Publisher: est celui qui va émettre les données

- 9 .	Subscriber : est celui qui va les recevoir en s’abonnant au Publisher.

- 10 .	Backpressure : c’est le subscriber qui va décider combien de données qu’il va recevoir.

- 11 .	L’échange de données entre Publisher et Subscribe va se terminer par :
  *  	Complete : si tout se passe bien
  * 	Error : si il ya un problème.

- 12 .	Reactor : Se compose principalement de deux types de Stream.
  * 	Flux<T>: Un Publisher correspondant à un échange de 1 à plusieurs éléments.
  * 	Mono<T> : Un Publisher correspondant à un échange de 0 à 1 élément.

- 13 .	Spring webflux : est un projet spring introduit pour prendre en charge la programmation réactive dans le Web. C'est une alternative à Spring MVC qui est basée sur Servlet, Il a été introduit pour la première fois avec Spring 5.

- 14 . Operations stream:

- 15 .	La différence entre Map et flatMap : 
  * 	Map : operateur pour convertir un élément de flux de données, retourner le même flux.
  * 	FlatMap : operateur pour convertir un élément de flux de données, retourner un flux de données par élément.

- 16 .	WebClient : Api qui permet d’accéder des services distants d’une manière réactive, est une alternative au classique RestTemplate.
