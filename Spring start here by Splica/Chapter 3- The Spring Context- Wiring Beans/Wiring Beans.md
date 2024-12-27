- two ways you can establish the relationships among beans: 
1- Link the beans by directly calling the methods that create them (which we’ll call wiring). 
2- Enable Spring to provide us a value using a method parameter (which we’ll call auto-wiring) and also refer to as Dependency Injection.
- When two methods annotated with @Bean call each other, Spring knows you want to create a link between the beans. If the bean already exists in the context (3A), Spring returns the existing bean without forwarding the call to the @Bean method. If the bean doesn’t exist (3B), Spring creates the bean and returns its reference.
- Using the @Autowired annotation to inject beans
 - there are three ways we can use the @Autowired annotation: 
    1-Injecting the value in the field of the class, which you usually find in examples and proofs of concept 
    2- Injecting the value through the constructor parameters of the class approach that you’ll use most often in real-world scenarios 
    3- Injecting the value through the setter, which you’ll rarely use in production ready code
- Be aware of deadlock problem when two dependencies rely on each other.
- Using the @Qualifier annotation, you clearly mark your intention to inject a specific bean from the context.