# Report Portal Automation Tests

## Overview
This project contains automated UI and API tests for Report Portal using Selenium WebDriver, RestAssured, and Allure for reporting. The tests are implemented in Java, following the Page Object Model (POM) pattern, and use Maven as the build tool.

## Prerequisites
- Java 11 or higher
- Maven 3.6.0 or higher
- Chrome Browser (for UI tests)
- Allure command-line tool (for report generation)
- Report Portal API key (manually generated from the Report Portal UI)

## Setup
1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd report-portal-tests
   ```
2. Update `src/test/resources/config.properties` with your manually generated API key:
   ```
   api.key=YOUR_API_KEY_HERE
   ```
3. Install dependencies:
   ```bash
   mvn clean install
   ```

## Running Tests
- Run all tests:
  ```bash
  mvn test
  ```
- Run specific test:
  ```bash
  mvn test -Dtest=WidgetTest
  ```

## Generating Allure Reports
1. Run tests to generate Allure results:
   ```bash
   mvn test
   ```
2. Generate and view Allure report:
   ```bash
   allure serve target/allure-results
   ```
