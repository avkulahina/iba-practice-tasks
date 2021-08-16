# Not boring Java course

### Requirements

- java 8
- IDE (like Eclipse, VsCode etc)
- Postman
- github account and repository
- git repository shoud have `master(main)` branch. The master branch should have ONLY `README.md` in the beggining
- every task should be developed in a separate branch like `task2_docker`. Every task should have at least 2 commits. After the completeion of the task you need to make a pull request to master branch. Every commit shoud match the convention, e.g.:

`feat: add Dockerfile with MongoDB`

`fix: update Dockerfile, use MongoDb 4.XX`

`docs: write documentation about starting Docker container`

`refactor: remove odd lines in Dockerfile`

- helpful resources 

https://www.studytonight.com/java/
https://www.programiz.com/java-programming/hello-world
https://www.javatpoint.com/java-tutorial



## Task 1 - Codewars

- Register yourself on [Codewars](https://www.codewars.com)
- complete all task
- review the solutions of other developers after each task
- post the link to your profile (or nickname)

[How do I compare numbers? - 8 kyu](https://www.codewars.com/kata/55d8618adfda93c89600012e/java)

[Java Functional Programming - P1 - 7kyu](https://www.codewars.com/kata/54a6b43e478d8ee14c000a5d)

[Java Functional Programming - P2 - 7kyu](http://www.codewars.com/kata/java-functional-programming-part-2-multiline-functions)

[Java Functional Programming - P3 - 7kyu](http://www.codewars.com/kata/java-functional-programming-part-3-closured-for-business)

[Java Functional Programming - P4 - 5kyu](http://www.codewars.com/kata/java-functional-programming-part-4-row-row-row-your-boat-gently-down-the-dot-dot-dot)

[Regex validate PIN code - 7kyu](https://www.codewars.com/kata/55f8a9c06c018a0d6e000132)

[Shop Inventory Manager - 6kyu](https://www.codewars.com/kata/55d1d06def244b18c100007c)

[PaginationHelper - 5kyu](https://www.codewars.com/kata/515bb423de843ea99400000a)

[Longest Common Subsequence (Performance version) - 4kyu](https://www.codewars.com/kata/593ff8b39e1cc4bae9000070)


## Task 2 - Prepare an environment

- Download and install [Docker](https://docs.docker.com/get-docker/)
- read about docker containers https://docs.docker.com/get-started/
- prepare a `Dockerfile` that starts an container with MongoDb or Neo4j
- make sure you can connect to your docker database instance from your local machine
- make the docker use your local filesystem, so when you destroy the instance you won't loose the data
- create 3 tables in database: 

User(id, Name, Surname, Age)
Item(id, Name, Description, Price)
Cart(id, User id, Item Id, Count)

Fill in 2 users, 10 items and one cart

## Task 3 - Start building an app

Create a RESTful service that perform CRUD operations.

https://www.mongodb.com/blog/post/rest-apis-with-java-spring-boot-and-mongodb

https://developer.okta.com/blog/2019/12/26/java-mongodb-crud

- GET /user should return a set of users
- GET /user/{id} should return a single user
- POST /user should create a user using given payload
- PUT /user/{id} should update the user
- DELETE /user/{id} should delete the user
- GET /item should return a set of items
- GET /item/{id} should return a single item
- POST /item should create an item using given payload
- PUT /item/{id} should update the item
- DELETE /item/{id} should delete the item
- GET /cart should return a set of carts (id, user id, user name, user surname, array of items (id, name, description, price, count))
- GET /cart/{id} should return a single cart
- POST /cart should create a cart using given payload
- PUT /cart/{id} should update the cart
- DELETE /cart/{id} should delete the cart

## Task 4 - Add an Authentication mechanisim

- Add [Swagger](https://www.baeldung.com/swagger-2-documentation-for-spring-rest-api) to the app, for easier access and documentation purposes

- Add [logger](https://www.baeldung.com/spring-boot-logging). Add att least 3 messages with different logger levels: DEBUG, INFO, ERROR.

- Add route `/authenticate` that will accept username and password, and return JWT token. All other routes must be secured using following http _Authorization_ header. Read this [article](https://www.toptal.com/java/rest-security-with-jwt-spring-security-and-java).


## Task 5 - Add roles

Register on [Auth0](https://auth0.com/). Create a new route `me/role` that will be authenticated using Auth0 SSO. 
![integrate](./img/integrate.png)

Select Regular Web Application and Java Spring Boot.

![web app](./img/regular-web-app.png)
![spring boot](./img/spring-boot.png)

Create at least 2 users and 2 roles (Admin and Reader). 
![user](./img/user.png)

The route must return following response for Admin user:

```
{
    "role" : "Admin",
    "message": "I'm Admin!"
}
```

The route must return following response for Reader user:


```
{
    "role" : "Reader",
    "message": "I can only read :("
}
```

And 401 Unathorized in case user does not exist.

Create a PR with screenshots it works for different roles.

## Task 6 - Code practice

- [Vowel Count: String, Cycle](https://www.codewars.com/kata/54ff3102c1bad923760001f3/java)
- [Enumerable Magic: Array, Predicates](https://www.codewars.com/kata/54598d1fcbae2ae05200112c)
- [Playing with Cubes: OOP](https://www.codewars.com/kata/55c0a79e20be94c91400014b)
- [Bingo: OOP](https://www.codewars.com/kata/566d5e2e57d8fae53c00000c)
- [Remove duplicate words: String, Regex](https://www.codewars.com/kata/5b39e3772ae7545f650000fc)
- [Circular list](https://www.codewars.com/kata/5b2e60742ae7543f9d00005d)
- [Prize Draw: Sort](https://www.codewars.com/kata/5616868c81a0f281e500005c)
- [Greatest Common Divisor: Recursion](https://www.codewars.com/kata/5500d54c2ebe0a8e8a0003fd)
- [FIXME - Bugs](https://www.codewars.com/kata/596c6eb85b0f515834000049)
- [FIXME: Hello - Bugs](https://www.codewars.com/kata/5b0a80ce84a30f4762000069)
- [Sorable Shapes - Design Patterns](https://www.codewars.com/kata/586669a8442e3fc307000048)
- [Black Jack: Conditional](https://www.codewars.com/kata/5bebcbf2832c3acc870000f6)




