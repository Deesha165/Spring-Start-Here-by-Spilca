- **@ResponseBody** to inform the dispatcher servlet that this method doesn’t return a view name but the HTTP response directly.
- We want to somehow prevent repeating the **@ResponseBody** annotation for each method. To help us with this aspect, Spring offers the **@RestController** annotation, a combination of **@Controller** and **@ResponseBody**. You use **@RestController** to instruct Spring that all the controller’s actions are REST endpoints.
- We use the **@ExceptionHandler** method to associate an exception with the logic the method implements
- `@RestControllerAdvice` is a specialized annotation in Spring Boot used to handle exceptions globally across all controllers in a RESTful web application.
- it is a combination of `@ControllerAdvice` and `@ResponseBody`. This means:
    1- It acts as an advice (interceptor) for all controllers.
    2- It automatically serializes responses into JSON or other formats (like XML) as needed.
- We use the **@ExceptionHandler** method to associate an exception with the logic the method implements.
- **@RequestBody** to accept data from body and good for post methods.
- In a Spring app, the Spring MVC mechanism supports the implementation of REST endpoints. You either need to use the @ResponseBody annotation to specify that a method directly returns the response body or replace the @Controller annotation with @RestController to implement a REST endpoint. If you don’t use one of these, the dispatcher servlet will assume the controller’s method returns a view name and try to look for that view instead.
- You can manage the HTTP status and headers by making your controller’s action return a ResponseEntity instance.
- You can manage the exceptions in the controller’s action directly or separate the logic executed if the controller’s action throws an exception using a REST controller advice class.
- 