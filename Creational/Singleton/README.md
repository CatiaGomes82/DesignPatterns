
## Singleton
> Singleton pattern restricts the instantiation of a class and ensures that only one instance of the class runs. This instance can be shared through the application, making Singletons great for managing global state in an application.

An implementation of singleton class should: 

* Have only one instance
* Instance should be globally accessible

### Example
[View product list example](./index.html)

### Pros
> Restricting the instantiation to just one instance could potentially save a lot of memory space. However, Singletons are actually considered an anti-pattern, and can (or.. should) be avoided in JavaScript.

### Cons
> #### Testing
> Testing code that relies on a Singleton can get tricky. Since we can't create new instances each time, all tests rely on the modification to the global instance of the previous test. The order of the tests matter in this case, and one small modification can lead to an entire test suite failing. After testing, we need to reset the entire instance in order to reset the modifications made by the tests.
>
> #### Dependency hiding
> When importing another module, superCounter.js in this case, it may not be obvious that module is importing a Singleton. In other files, such as index.js in this case, we may be importing that module and invoke its methods. This way, we accidentally modify the values in the Singleton. This can lead to unexpected behavior, since multiple instances of the Singleton can be shared throughout the application, which would all get modified as well.
>
> #### Global state
> A Singleton instance should be able to get referenced throughout the entire app, as a global variable. Having global variables is generally considered as a bad design decision. Global scope pollution can end up in accidentally overwriting the value of a global variable, which can lead to a lot of unexpected behavior.
>
> The common usecase for a Singleton is to have some sort of global state throughout your application. Having multiple parts of your codebase rely on the same mutable object can lead to unexpected behavior.