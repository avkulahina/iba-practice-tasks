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

## Task 5 - Add roles

## Task 6 - Add pagination
