- The methods in the **Feign client interface** serve as both:
1. **Functions**: They represent the Java methods you call in your code to trigger remote API calls.
2. **EndPoint Shape**: They define the **structure** of the HTTP requests (like URL paths, query parameters, request bodies) that will be made to the remote API.
- Structure of method in OpenFeign proxy interface
@FeignClient annotation to specify remote URI that we will call
1 - **Method in the Interface**: Defines a function in your Java code.
2-  **Annotations on the Method**: Specify the details of the HTTP request.
3- **Method Parameters**: Represent values that you send to the remote API, such as path variables, query parameters, or the request body.
4- **Return Type**: Represents the data type you expect from the API response.