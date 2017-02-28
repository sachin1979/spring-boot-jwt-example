This is an implementation of first part of article at following website.
https://auth0.com/blog/securing-spring-boot-with-jwts/

To access the application
1) User http POST to localhost:8080/login from postman and in the BODY of port choose option RAW and paste following JSON
   {"username":"admin", "password":"password"}
2) Click on Send button.

In the response HEADER you will get an authorization header
Authorization →
      Bearer eyJhbGciOiJIUzUxMiJ9.eyJzdWIiOiJhZG1pbiIsImV4cCI6MTQ4OTE2ODExOX0.KcFaTg7Ypf9xXNfNePztqz7bfKoOIZfI9j9ID0sZ1VBf4x3_O8_7O9xT0ZRn5nHCyc7jfG7ttEqprszrpH6U7w
      
3) Change to HTTP Get and URL as 
localhost:8080/users

4) In the Headers, type Authorization as key name and value as 
eyJhbGciOiJIUzUxMiJ9.eyJzdWIiOiJhZG1pbiIsImV4cCI6MTQ4OTE2ODExOX0.KcFaTg7Ypf9xXNfNePztqz7bfKoOIZfI9j9ID0sZ1VBf4x3_O8_7O9xT0ZRn5nHCyc7jfG7ttEqprszrpH6U7w

5) Click on Send button and you will see the response from the server available.

The above BIG string is the JWT token.


