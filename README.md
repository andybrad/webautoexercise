# Web Automation Exercise
A UI test automation solution using Java, Maven, CucumberJVM, and Selenium

![Automation image](http://res.cloudinary.com/dzrosr2sg/image/upload/v1536577935/Automation-2_bheqmp.png)

## Project Brief

**Web Automation Exercise**

Develop a Web test solution that automates a few simple tests, composed as BDD scenarios.
The target for the test is the dummy web site: http://automationpractice.com
NOTE: you can use these credentials: someone@example.com\Password123

- **Scenario 1**: Order T-Shirt (and Verify in Order History)
- **Scenario 2**: Update Personal Information (First Name) in My Account

**Candidate Requirements**:
- Build a test project that includes automation of the 2 scenario above.
- Solution to be coded in Java and driven using a BDD tool (see potential solution components below)
- Share code in a public GitHub repository for review. Include execution instructions.
- Share further improvements that could be considered to develop the framework (Optional)

**Potential Solution Components**<br>
The following suggested tools and libraries (or similar substitutes) should be used:
- CucumberJVM
- WebDriver
- Maven

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Installing

- [JAVA SE 8](http://www.oracle.com/technetwork/java/javase/downloads/index-jsp-138363.html) (Java 9 is not yet supported by Cucumber) 
- [Maven](https://maven.apache.org/index.html) - version 3.3.1 or higher
- [IntelliJ IDEA](https://www.jetbrains.com/idea/) (community edition is free)
	- [IntelliJ IDEA Cucumber for Java plugin](https://plugins.jetbrains.com/plugin/7212-cucumber-for-java)
- [Chrome](https://www.google.co.uk/chrome/?brand=CHBD&gclid=EAIaIQobChMI8fKl0aqw3QIVTb7tCh0lLgBWEAAYASABEgK5W_D_BwE&gclsrc=aw.ds&dclid=CPPZrNiqsN0CFUQs4AodO8EIZQ)

## Running the tests

There are 2 way to run the tests:
1. Open the project in IntelliJ, click the green triangle button in the top right, or in the project directory navigate to src > test > resources to find the feature files, right click and select Run tests.

2. Open a command/terminal window, CD to the directory where the project is located and run the following:

```
mvn test
```

The tests are set up to run in Google Chrome on either Windows or Mac OS (no extra configuration should be needed).

### Test Description

In the feature file "OrderWorkflow" there is one scenario called "Customer is able to order an item and verify the purchase in order history". This aims to test Scenario 1 in the project brief.<br> 
In the feature file "MyAccount" there is one scenario called "Customer is able to change their first name". This aims to test Scenario 2 in the project brief. 


## Improvements
Currently username and password test data sits in the TestBase class. A better test data strategy is required which could include:
- Use the code of the application to create a test data factory which generates user data from scratch, per test, per run.
- Move the username and password to a properties/config file and reference in code
- Move the username and password to another data source like excel and reference in code

The tests could be run as part of a continous integration build using tool like Jenkins.<br>
The tests could also be run on differenet browsers/platforms. This would require downloading more drivers e.g. IEDriverServer to test on IE.<br>
The tests could also be run on differenet browsers/platforms via a cloud testing service such as Browser Stack or Sauce Labs.

## Acknowledgments

* This is the first time I have done anything in JAVA and its related tooling. After a few tutorials from different sources, I found setting up the Maven project using the archetype created by the Cucumber team the best option.
* Thanks to Joe for making sure I hadn't done antyhing stupid!

