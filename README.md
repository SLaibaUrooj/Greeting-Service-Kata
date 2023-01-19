# Greeting-Service-Kata
Falcon Clean Architecture - Excercises

This code defines a Greetings class that has the following functionality:

1.   Initializes an empty dictionary greetings_storage and calls the load_config method when an instance of the class is created.
2.   load_config method loads the environment variables that start with "GREET_" and adds them to the greetings_storage dictionary, then it prints "GREETING DASHBOARD!" and the current greetings_storage
3. user_info method takes in a lang and user arguments and assigns them to language and user_name attributes of the instance, then calls the greet method.
4. greet method checks if the language attribute of the instance is a key in the greetings_storage dictionary, if it is, it prints the value at that key along with the user_name attribute, otherwise it prints "Sorry, greeting not available in" followed by the language attribute.
5. store method takes in a dictionary greets and assigns it to the greetings_storage attribute, then prints the new greetings_storage.
6. An instance of the Greetings class is created at the end of the code and assigned to the variable greetObj.

This implementation follows the **Twelve-Factor App** principles by:

1.   Storing the greetings in the environment variables(config) under GREET_ prefix
2.   Loading the config in the constructor to initialize the greetings storage
3.   Treating the greetings storage as an attached resource
4.   Keeping the greet method stateless by only using the language and user_name properties
5. Not using any backing service
6. Not providing any admin process

You can run this code by setting the environment variables with the format GREET_LANGUAGE="GREETING_MESSAGE" and running the script with python.
