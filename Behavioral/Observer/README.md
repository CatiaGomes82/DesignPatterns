
## Observer
The Observer is a design pattern where an Observavble stores a list of subscribed events and automatically notifies when an event happens.

>An observable object usually contains 3 important parts:
>
>- observers: an array of observers that will get notified whenever a specific event occurs
> - subscribe(): a method in order to add observers to the observers list
>- unsubscribe(): a method in order to remove observers from the observers list
>- notify(): a method to notify all observers whenever a specific event occurs

### Example
[View social media example](./index.html)

### Pros
> Using the observer pattern is a great way to enforce separation of concerns and the single-responsiblity principle. The observer objects aren’t tightly coupled to the observable object, and can be (de)coupled at any time. The observable object is responsible for monitoring the events, while the observers simply handle the received data.

### Cons
> If an observer becomes too complex, it may cause performance issues when notifying all subscribers.