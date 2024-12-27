- Any test has three main parts : 
1- Assumptions—We need to define any input and find any dependency of the logic we need to control to achieve the desired flow scenario. For this point, we’ll answer the following questions: what inputs should we provide, and how should dependencies behave for the tested logic to act in the specific way we want? 
2- Call/Execution—We need to call the logic we test to validate its behavior. 
3- Validations—We need to define all the validations that need to be done for the given piece of logic. We’ll answer this question: what should happen when this piece of logic is called in the given conditions?
-  Sometimes in tests you want to eliminate dependencies to some components to allow the test to focus on how some but not all parts interact. In such cases, we replace the components we don’t want to test with “mocks”: fake objects you
