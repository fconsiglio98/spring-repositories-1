# Exercise - Spring Boot - Spring Repositories 1
* write a Spring Boot application with the necessary dependencies that:
  * uses `Rest Repositories HAL Explorer`
  * connects to a local MySQL db
  * drops the schema at the end of the session
  * defines a table of cars, where each `Car` has:
    * a primary key
    * a `modelName` not null
    * a `serialNumber` not null
    * a `currentPrice` that can be null
  * defines a repository for the cars, so that it's possible to use `HAL Explorer` to explore the data
* use the `HAL Explorer` to add 2 cars in the database
* use the `HAL Explorer` to list all the cars in the database
* **note for reviewers**: examples of HAL post requests can be found in `HAL-REQUESTS.md`
