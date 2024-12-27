- Types of web scopes 
1- Request scope—Spring creates an instance of the bean class for every HTTP request. The instance exists only for that specific HTTP request. 
2- Session scope—Spring creates an instance and keeps the instance in the server’s memory for the full HTTP session. Spring links the instance in the context with the client’s session. A session-scoped bean allows us to store data shared by multiple requests of the same client.
3- Application scope—The instance is unique in the app’s context, and it’s available while the app is running.
- **two different sessions** from the **same browser** cannot exist simultaneously under normal circumstances because the browser typically sends only **one session ID** in each request for a specific domain. This means that the browser can only maintain one active HTTP session at a time for a given domain.
-  An **HTTP session** is identified uniquely by a **session ID**.
- The session ID is sent by the client (browser) via a **session cookie** (e.g., `JSESSIONID`).
- A **new session** is created when a client makes their first request, and the server generates a unique session ID.
- **Sessions are different** when they have different session IDs, meaning each user or browser session has its own isolated context.
- **Different sessions** are used for different users (even on the same application), ensuring that their data (such as login credentials) is separate and not shared across sessions.
- Spring links a session-scoped bean instance to the HTTP session of the client. This way, a session-scoped bean instance can be used to share data among multiple HTTP requests from the same client
- Spring guarantees that a request-scoped bean instance is only accessible by one HTTP request. For this reason, you can use the instance’s attributes without worrying about concurrency-related problems. Also, you don’t need to worry that they might fill the app’s memory. Being they are short-lived, the instances can be garbage-collected once the HTTP request ends.
- Even if from the same client, the client can send HTTP requests concurrently. If these requests change data in the session-scoped instance, they might get into race-condition scenarios. You need to consider such situations and either avoid them or synchronize your code to support the concurrency.
- 