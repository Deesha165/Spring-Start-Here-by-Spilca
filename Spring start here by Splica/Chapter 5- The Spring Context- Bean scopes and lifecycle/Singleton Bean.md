- A race condition is a situation that can happen in multithreaded architectures when multiple threads try to change a shared resource leading to inconsistency issues.
- One of the advantages of constructor injection is that it allows you to make the instance immutable (define the bean’s fields as final).
Using beans boils down to three points 
- Make an object bean in the Spring context only if you need Spring to manage it so that the framework can augment that bean with a specific capability. If the object doesn’t need any capability offered by the framework, you don’t need to make it a bean. 
- If you need to make an object bean in the Spring context, it should be singleton only if it’s immutable. Avoid designing mutable singleton beans. 
- If a bean needs to be mutable, an option could be to use the prototype scope.
 
