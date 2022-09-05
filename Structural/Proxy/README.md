
## Proxy
>A proxy object can determine the behavior whenever we're interacting with the object, for example when we're getting a value, or setting a value.
>
>A proxy can be useful to add validation.
>
> In JavaScript: instead of interacting with the target object directly, we'll interact with the Proxy object.
>
> Although there are many methods that you can add to the Proxy handler, the two most common ones are get and set:
>
> * get: Gets invoked when trying to access a property
> * set: Gets invoked when trying to modify a property

### Example
[View money transaction example example](./index.html)

### Pros
> Proxies are a powerful way to add control over the behavior of an object. A proxy can have various use-cases: it can help with validation, formatting, notifications, or debugging.

### Cons
> Overusing the Proxy object or performing heavy operations on each handler method invocation can easily affect the performance of your application negatively. It's best to not use proxies for performance-critical code.