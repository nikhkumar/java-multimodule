# java-multimodule

This is multi-module java project.

## Modules:
1. mm-common
1. mm-module1 	- _depends upon mm-common_  
1. mm-module2	- _depends upon mm-common_
1. packing-module - _packing module for single jar_

## Useful Commands

* $ password 
* $ password <-- password-md5
* $ password <-- password-sha
* $ web <-- (password-md5 | password-sha) <-- password

Some commands to a build a multi-module project, for examples :

* $ mvn -pl password compile		# compile password module only	
* $ mvn -pl password-sha compile	# compile password-sha module, also dependency - password
* $ mvn -pl web compile			# compile web module only	
* $ mvn -am -pl web compile		# compile web module, also dependency - password-sha or password-md5, password
* $ mvn -pl web jetty:run 			# run web module with Jetty
* $ mvn compile 					# compile everything


## Table

| Left columns  | Right columns |
| ------------- |:-------------:|
| left foo      | right foo     |
| left bar      | right bar     |
| left baz      | right baz     |

## Blocks of code

```
let message = 'Hello world';
alert(message);
```
## References:

* Guide to Working with Multiple Modules [Link](https://maven.apache.org/guides/mini/guide-multiple-modules.html)

* Creating Production Artifacts in multi-module maven [Link](https://everyday.codes/java/creating-production-artifacts-in-a-multi-module-maven-project/)

* Mkyong [Link](https://mkyong.com/maven/maven-how-to-create-a-multi-module-project/)


    