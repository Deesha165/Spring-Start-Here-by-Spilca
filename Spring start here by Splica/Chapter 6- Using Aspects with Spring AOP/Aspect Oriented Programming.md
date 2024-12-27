- Aspects are a way the framework intercepts method calls and possibly alters the execution of methods.
- To create an aspect, you follow these steps (figure 6.5): 
- 1- Enable the aspect mechanism in your Spring app by annotating the configuration class with the @EnableAspectJAutoProxy annotation. 
- 2- Create a new class, and annotate it with the @Aspect annotation and add a Bean for it at spring context.
- 3- Define a method that will implement the aspect logic and tell Spring when and which methods to intercept using an advice annotation. 
- 4- Implement the aspect logic
- An aspect is an object that intercepts a method call and can execute logic before, after, and even instead of executing the intercepted method. This helps you decouple part of the code from the business implementation and makes your app easier to maintain.
- To tell Spring which methods an aspect needs to intercept, you use AspectJ pointcut expressions. You write these expressions as values to advice annotations. Spring offers you five advice annotations: @Around, @Before, @After, @AfterThrowing, and @AfterReturning. In most cases we use @Around, which is also the most powerful.
- Multiple aspects can intercept the same method call. In this case, it’s recommended that you define an order for the aspects to execute using the @Order annotation
### **Key Concepts of AOP:**

1. **Aspect**: A module that encapsulates a cross-cutting concern. An aspect contains advice, which defines what to do and when to do it (before, after, or around method execution).
    
2. **Join Point**: A point in the execution of the program where an aspect can be applied. This could be a method call, a method execution, a field access, or others.
    
3. **Advice**: The actual code that runs when a particular join point is reached. It defines the action to be taken (e.g., logging, security checks). There are different types of advice:
    
    - **Before advice**: Code that runs before the method execution.
    - **After advice**: Code that runs after the method execution (whether the method completes normally or throws an exception).
    - **Around advice**: Code that surrounds the method execution, providing the ability to control whether or not the method is executed, modify arguments, or alter the return value.
4. **Pointcut**: An expression that selects specific join points where advice should be applied. It defines "where" the advice should run in the application (e.g., all methods in a class, methods with a specific annotation, etc.).
    
5. **Weaving**: The process of applying aspects to a target object, modifying its behavior at runtime or compile-time.