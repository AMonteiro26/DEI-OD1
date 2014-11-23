# DEI-OD1

SQL database for the second Oficina de Design I (Digital Workshop I) project @ FCTUC.

## Installation

To build the tables, run __phpMyAdmin__ from a local or remote server, or use the demo version [available from the phpMyAdmin website](http://demo.phpmyadmin.net/master-config/).

Create a new database and [import the od1.sql file](http://www.inmotionhosting.com/support/website/phpmyadmin/import-database-using-phpmyadmin) or [copy and paste its contents](https://www.siteground.com/tutorials/phpmyadmin/phpmyadmin_mysql_query.htm) into the new database.

Please check the [wiki](https://github.com/emmnunes/DEI-OD1/wiki) for additional instructions on how to create the tables and example SQL queries.

## Tables

#### Rooms
_Lists all rooms in the building, by their official designation (E4.1)_
* id (Auto Incremented INT)
* room (e.g. _F1.1_)

#### Services
_Lists relevant University services located in the building_

__Columns:__
* id (Auto Incremented INT)
* name (VARCHAR — e.g. _GAPI — Gabinete de Apoio a Projectos de Investigação_)

#### Teachers
_Lists all of the department teachers_

__Columns:__
* id (Auto Incremented INT)
* name (VARCHAR — e.g. _Alberto Jorge Lebre Cardoso_)

#### Offices
_Defines teacher offices, by establishing relations between the rooms and teachers tables_

__Columns:__
* id (Auto Incremented INT)
* roomID (INT)
* teacherID (INT)

#### Service Rooms
_Defines rooms for services, by establishing relations between the rooms and services tables_

__Columns:__
* id (Auto Incremented INT)
* serviceID (INT)
* roomID (INT)

## Contributing

Students should fork this project and work on top of the original table structure, by adding any information that's relevant to the project, e.g.

* ~~adding teacher offices, by creating a table which makes use of the teachers and rooms tables~~
* ~~establishing relations between services and rooms~~
* adding office hours for teachers
* adding spatial information to rooms (e.g. floor, tower, etc.)
* adding faculty facilities (e.g. bathrooms)
* adding typology information to the rooms (e.g. meeting room, classroom, study room, etc.)
* adding capacity information to rooms
* flagging private or inacessible rooms

All changes considered useful for the entire class will be merged to the main repository. Pull requests should include at least one .sql file, with no database creation or editing instructions.