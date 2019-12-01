ps-guitar-db
============

A Basic Spring JPA app with an H2 DB

Prerequisites
-------------
You will need to following tools in order to work with this project and code

* git (http://git-scm.com/)
* JDK 1.8+ (http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
* Maven 3.x+ (http://maven.apache.org/)
* An IDE of your choice.  (Eclipse, IntelliJ, Spring STS, Netbeans, etc.)

Getting Started
---------------
To run this project locally, perform the following steps.

* Clone project to your machine using git - "git clone https://github.com/dlbunker/ps-guitar-db.git"
* Import the project into your IDE using the maven pom.xml.  In spring STS suite this is done by importing an existing maven project
* Run the JUnit tests in the src/test/java folder.  If all pass you are good to go.

Original https://github.com/dlbunker/ps-guitar-db
Fixes to get initial tests running
----------------------------------
1) Copy POM from https://github.com/Wiktorl4z/SpringJPA
2) comment out spring-data-jpa dependency
3) Add jaxb dependencies:
https://stackoverflow.com/questions/57548038/error-creating-bean-with-name-entitymanagerfactory-not-fixed-by-javaxb-or-hibe
4) Change Model classes as follows
	@GeneratedValue(strategy=GenerationType.AUTO)
	To
	@GeneratedValue(strategy=GenerationType.IDENTITY)