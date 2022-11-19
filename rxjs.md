# Reactive programming
- A programming paradigm concerned with flows of data streams emitted from observables to observers subscribed to them.
- See the example given in this [animation][reactive-programming].

[reactive-programming]: https://codecraft.tv/courses/angular/reactive-programming-with-rxjs/streams-and-reactive-programming/

# Reactive eXtension (RX)
- Implementation of reactive programming.
- Async event management based on observable streams (e.g. events).
- Data streams can be built from anything, not just click events (see [intro to rxjs][intro-to-rxjs]).
- Functions can be used to transform these streams (e.g. filter, map...).

[intro-to-rxjs]: https://gist.github.com/staltz/868e7e9bc2a7b8c1f754

# Rxjs
- A library implementing RX in javascript, that works well with Angular.
- Besides the official documentation, check also [learnrxjs.io][learnrxjs].
- Installed as usual with:

```terminal
$ npm install rxjs
```

[learnrxjs]: https://www.learnrxjs.io

## Observable
- An observable is a stream or source of data arriving over time.
- It can be creating from anything (e.g. an event).

## Subject
- A special type of observable that multicasts values to multiple observers.
- In contrast, a plain Observable only send notifications to a single Observer (See [the difference][unicast-vs-multicast] between the two).

[unicast-vs-multicast]: https://luukgruijs.medium.com/understanding-rxjs-subjects-339428a1815b

## Observer
- Consumer of values delivered by an Observerable.
- It's simply a set of callbacks for each notification delivered by the observable:
  - next: called on successful emission.
  - error: called on error.
  - complete: called on completion.

## Subscriptions
- Like a tap to turn on to get the stream of water.
- Subscription is created by supplying an observer (i.e. a callback) to react to the event received.

## Operators
- A way to manipulate values from an observable to create an observable of transformed values.
- See how the [map operator][map-operator] can be used to transform the emitted values similarly to `Array.map()`.

[map-operator]: https://www.learnrxjs.io/learn-rxjs/concepts/rxjs-primer#operators
