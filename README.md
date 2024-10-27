# Risevest-Test
QA Engineer Test
# Risevest Web Application Test Suite
## Overview
This repository contains automated test scripts for the Risevest Investment Web App. The tests are implemented using Selenium with Java and TestNG, following the Page Object Model (POM) design pattern to ensure modularity and maintainability. The test suite covers essential user flows, including login, viewing wallet balance, showing/hiding balance, viewing investment plans, and creating a new plan.

# Prerequisites
Java Development Kit (JDK): Ensure JDK 8 or later is installed. You can download it from Oracle's website.
Maven: Maven is used for dependency management. Download and install from Maven's website.
WebDriver: This project uses ChromeDriver, but it is configured to run with other browsers like Firefox and Edge. Ensure that the WebDriver binaries are available in your system PATH or specify the path directly in the code if needed.
Project Setup
Clone the Repository:

bash
Copy code
git clone https://github.com/Arydunnu/Risevest-Test.git
cd Risevest-Test
Install Dependencies: Ensure that dependencies specified in pom.xml are installed. Run:

bash
Copy code
mvn clean install
Project Structure
src/main/java/pages: Contains Page Object classes for each webpage component (e.g., LoginPage, WalletPage, PlansPage).
src/test/java/tests: Contains TestNG test classes for each user flow (e.g., LoginTest, WalletTest).
src/test/resources: Contains any external test data files (e.g., Excel files for data-driven testing).
pom.xml: Maven project file, which manages dependencies and build configuration.
Running Tests
1. Run All Tests
To execute all tests, use the following Maven command:

bash
Copy code
mvn test
2. Run a Specific Test Class
To run a specific test class (e.g., LoginPage), use:

bash
Copy code
mvn -Dtest=LoginTest test

### java
Copy code
// For Chrome
WebDriver driver = new ChromeDriver();

# Reporting with Allure 
To enable reporting with Allure:

## Add the Allure Maven dependency to pom.xml.
Run tests with Allure reporting enabled:
bash
Copy code
mvn clean test
mvn allure:report
## View the report in your browser:
bash
Copy code
allure serve target/allure-results

# Additional Notes
Ensure the test environment has stable network connectivity, as these tests interact with a live web application.
Keep WebDriver versions up to date for optimal cross-browser compatibility.
If testing in a CI/CD pipeline, configure the WebDriver paths appropriately.

# Troubleshooting
WebDriver Version Issues: Update WebDriver binaries if you encounter browser compatibility issues.
Test Failures Due to Element Loading: If elements load slowly, consider adding WebDriver wait times.
Running on Different Browsers: Ensure the correct WebDriver executable is available or added to the PATH for each browser.
Contributing
Contributions are welcome! Please fork the repository and create a pull request for any bug fixes or enhancements.

License
This project is licensed under the MIT License. See LICENSE for details.