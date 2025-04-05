#Sonarqube with OWASP dependency scanning

This is a repository with code based on SpringBoot Petclinic (REST version): https://github.com/spring-petclinic/spring-petclinic-rest

It is further integrated with SonarQube and OWASP dependency scanning.

## Pre-requisite
1. Sonarqube server
2. Sonarqube project token

## Steps

Generate OWASP report
````
mvnw dependency-check:aggregate -PsonarReports
````

Perform SonarQube Analysis (replace project key, host url and token accordingly)
````
mvnw verify sonar:sonar -Dsonar.projectKey=demo -Dsonar.host.url=http://localhost:9001 -Dsonar.login=sqp_f1386a00f961c2ccbdb3438ac2af53f9911a1fb7
````
