## Version1-Gatling
skeleton framework for Gatling API performance testing

### Dependencies

* Java
* Maven
* IDE for Scala development. I.e. IntelliJ IDEA


### Setup

#### Secrets

Insert an application properties file

    src/test/resources/properties/application.properties

## Run Tests

### Environment settings

Set the system property to point to a system property environment
        
    -Denv

### Maven

Execute entire

    $mvn clean gatling:test -Denv=staging


Execute specific simulation

    $mvn gatling:test -Denv=staging -Dgatling.simulationClass=simulations.Sessions.GetSessionsByQueryParamsSimulation

### Parameters

Parameters have been defaulted in scenarios against volumetrics but optional parameters can be defined on the terminal

    -DrampUsers=X
    -DrampDuration=X
    -DatOnceUsers=X 
    -DconstantUsersPerSec=X -DconstUsersDuration=X

## Folder Structure
```
└── src
    └── test
        ├── resources
        │   ├── bodies
        │   ├── data
        │   └── properties
        └── scala
            ├── config
            ├── Requests
            ├── Scenarios
            ├── Simulations
            └── utils
```
