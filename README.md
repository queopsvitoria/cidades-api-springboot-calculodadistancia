# cidades-api-springboot-calculodadistancia
https://distanciacidades.herokuapp.com/
Requirements
Linux
Git
Java 8
Docker
IntelliJ Community
Heroku CLI
DataBase
Postgres

Populate
data
cd ~/computador/sql-paises-estados-cidades/PostgreSQL


psql -h localhost -U postgres_user_city cities -f pais.sql
psql -h localhost -U postgres_user_city cities -f estado.sql
psql -h localhost -U postgres_user_city cities -f cidade.sql

psql -h localhost -U usuario cities

CREATE EXTENSION cube; 
CREATE EXTENSION earthdistance;
Postgres Earth distance
earthdistance--1.0--1.1.sql
OPERATOR <@>
postgrescheatsheet
datatype-geometric
Access
docker exec -it cities-db /bin/bash

psql -U postgres_user_city cities
Query Earth Distance
Point

select ((select lat_lon from cidade where id = 4929) <@> (select lat_lon from cidade where id=5254)) as distance;
Cube

select earth_distance(
    ll_to_earth(-21.95840072631836,-47.98820114135742), 
    ll_to_earth(-22.01740074157715,-47.88600158691406)
) as distance;
Spring Boot
https://start.spring.io/
Java 8
Gradle Project
Jar
Spring Web
Spring Data JPA
PostgreSQL Driver
Spring Data
jpa.query-methods
Properties
appendix-application-properties
jdbc-database-connectio
Types
JsonTypes
UserType
Heroku
DevCenter
Code Quality
PMD
https://pmd.github.io/pmd-6.8.0/index.html
Checkstyle
https://checkstyle.org/

https://checkstyle.org/google_style.html

http://google.github.io/styleguide/javaguide.html

wget https://raw.githubusercontent.com/checkstyle/checkstyle/master/src/main/resources/google_checks.xml
