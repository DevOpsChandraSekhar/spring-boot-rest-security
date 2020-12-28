# springboot
# Clone or Fork this entire repository
  https://github.com/DevOpsChandraSekhar/springrest.git
  
# Spring boot rest, H2 database and Spring security example
1.	Spring Boot 2.4.1.RELEASE
2.	Spring 5.3.2.RELEASE 
3.	Spring Data JPA 2.4.2.RELEASE
4.  Spring Security 5.4.2.RELEASE
5.	H2 In-memory Database 1.4.200
6.	Tomcat Embed 9.0.41
7.	Maven 3
8.	Java 8

# You can run app from eclipse or cmd line interface.
  1. From command line try 
  
  *mvn spring-boot:run
  *A normal GET and POST will return a 401, all endpoints are protected, need authentication.
  
  1. curl localhost:8080/books

  2. *curl -X POST localhost:8080/books -H "Content-type:application/json" 
    -d {\"name\":\"ABC\",\"author\":\"mkyong\",\"price\":\"8.88\"}
	
  3. Send a GET request along with user login.
     *curl localhost:8080/books -u user:password
	 
  4. curl localhost:8080/books/1 -u admin:password
  
  5. Try to send a POST request with ‘user’ login, it will return 403, Forbidden error. This is because the user has no right to send a POST request.
     *curl -X POST localhost:8080/books -H "Content-type:application/json" 
    -d {\"name\":\"ABC\",\"author\":\"mkyong\",\"price\":\"8.88\"} -u user:password

  6. Try to send a POST request with admin login
     *curl -X POST localhost:8080/books -H "Content-type:application/json" 
    -d {\"name\":\"ABC\",\"author\":\"mkyong\",\"price\":\"8.88\"} -u admin:password
    