# rest-assured-bug-buster

## Table of Contents
* [Introduction](#Introduction)
* [Tools and Technologies](#Tools-and-Technologies)
* [Framework](#Framework)
* [Struture of Project](#Struture-of-Project)
* [Reporting](#Reporting)

## Introduction:
* LMS is the Learning Mnagement System.LMS contains modules like Program Module,Program Batch Module,User Module,Assignment Module and Assignement Submission Module.

## Tools and Technologies:
* This project is created with,
#### * Maven- Dependency Management
#### * Java- Programming Language
#### * Selenium Webdriver
#### * Cucumber with Pagefactory-BDD approach
#### * log4j - Logging
#### * Allure Report
#### * Extent Report

## Framework
```mermaid
flowchart TD
    src-->test
    test-->runner
    test-->stepDefinition
    test-->utilities
    test-->base
    src-->resources
    resources-->config
    resources-->Exceldata
    resources-->features
    features-->program
    features-->batch
    features-->user
    features-->assignment
    features-->assignment submission
    resources-->log4j
 ```
 ## Struture of Project
 
 ### Feature Files
 A feature file is a file that lets you describe software’s behavior without detailing how that behavior is implemented. Feature files are written using the
 Gherkin language and must live in a folder named features within the root of your project.For Ex:
 ```
# ./features/Programpost.feature

Feature: Creating the User Using BDD 

  Scenario: Creation of a program with valid endpoint and request body using Data Driven
    Given User sends request for Program module with valid request body
    When  User sends POST request data from "<SheetName>" and "<Testcase>"
    Then  User sucessfully receives status code "201" with reponse body
```
 ### Step Definition
 Step definitions act as the glue between features files and the actual system under test.When Cucumber executes a Gherkin step in a scenario, it will look for a matching step definition to execute. So, now when Cucumber executes a step of the scenario mentioned in the feature file, it scans the step definition file and figures out which function is to be called.
 
 ### Testrunner
 This LMS project is run by Testrunner file. The test runner file should contain the path of the feature file and step definition file that we want to execute.
 Right click the feature file and select "Run" or "Debug" to start the test.
Features will run in order :
1. PostProgram.feature
2. PostBatch.feature
3. PostUser.feature
4. PostAssignment.feature
5. PostAssignmentSubmit.feature
6. GetProgram.feature
7. GetProgram.feature
8. GetBatch.feature
9. GetUser.feature
10. GetAssignment.feature
11. Getassignmentsubmit.feature
12. GetUser.feature
13. Putprogram.feature
14. Putbatch.feature
15. PutUser.feature
16. Delassignsubmit.feature
17. Delassignment.feayure
18. Del_user.feature
19. Delbatch.feature
20. DelProgram.feature

       
       

## Reporting
Once tests complete run reports are generated. This framework uses different types of test reporters to communicate pass/failure.

**Allure Report**: 

Report will be generated into temp folder. Web server with results will start appearing in your default browser.it provides a good representation of test execution output and is designed to create reports that are clear to everyone by creating graphs regarding test execution time, overall test result overviews, test result history, etc. Web server with results will start appearing in your default browser.
```
$ cd <Project Directory>

$ allure serve allure-results
```

**HTML Report:**

To open an HTML report, from the Code Coverage Results view, right-click a result, and select Open as > HTML Report

**Log4j**
Log4j in selenium is one such logging framework that helps in gathering information in the form of logs or log files.In our project we used 3 main component of logger,appenders and layouts.Once execution is completed refresh the project where you see the log folder and it automatically contains the logs of your project

## Develop automation scripts using BDD approach - Cucumber-Java :
Tests are written in the Cucumber framework using the Gherkin Syntax. More about Gherkin & Cucumber can be found at [https://cucumber.io/docs/reference] 


## Data Driven Selenium Cucumber:
In our project we used Data driven methodology.Data driven testing means passing data with the help of  external sources like xls,xlsx,csv files., etc. In this we are taking inputs from external source.
 
