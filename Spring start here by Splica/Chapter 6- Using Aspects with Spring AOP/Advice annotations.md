@Around annotation allows you to **intercept** the method execution both before and after the method is invoked and it is the most flexible.
Other than @Around, Spring offers the following advice annotations: 
1- @Before—Calls the method defining the aspect logic before the execution of the intercepted method. 
2- @AfterReturning—Calls the method defining the aspect logic after the method successfully returns, and provides the returned value as a parameter to the aspect method. The aspect method isn’t called if the intercepted method throws an exception. 
3- @AfterThrowing—Calls the method defining the aspect logic if the intercepted method throws an exception, and provides the exception instance as a parameter to the aspect method. 
4- @After—Calls the method defining the aspect logic only after the intercepted method execution, whether the method successfully returned or threw an exception.
