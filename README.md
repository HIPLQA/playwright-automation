# Playwright Automation Framework

Enterprise-grade UI automation framework built using Playwright + Java + TestNG with support for cross-browser execution, retry mechanisms, reporting, CI/CD integration, and data-driven testing.

---

## 🚀 Tech Stack

- Playwright
- Java
- TestNG
- Maven
- GitHub Actions
- Extent Reports
- Log4j2
- Apache POI (Excel Data Handling)

---

## 📌 Framework Features

- Cross-browser testing
- Parallel execution support
- Retry mechanism for flaky tests
- Screenshot capture on failure
- Extent reporting integration
- Data-driven testing using Excel
- Page Object Model (POM)
- Maven-based execution
- Config-driven framework
- GitHub Actions CI integration
- Reusable utility classes
- TestNG suite management

---

# 📂 Project Structure


playwright-learn-automation
│
├── .github
│   └── workflows
│       └── ci.yml
│
├── src
│   ├── main
│   │   └── java/com/playwright/qa
│   │       ├── base
│   │       │   ├── BaseTest.java
│   │       │   └── ConfigReader.java
│   │       │
│   │       ├── listener
│   │       │   ├── ExtentListener.java
│   │       │   ├── ExtentManager.java
│   │       │   ├── RetryAnalyzer.java
│   │       │   └── RetryListener.java
│   │       │
│   │       ├── pages
│   │       │   ├── CartPage.java
│   │       │   ├── DashboardPage.java
│   │       │   ├── LandingPage.java
│   │       │   ├── LoginPage.java
│   │       │   ├── ManageCoursesPage.java
│   │       │   └── SignUpPage.java
│   │       │
│   │       └── utils
│   │           ├── AssertUtil.java
│   │           ├── ExcelUtil.java
│   │           └── TestDataProvider.java
│   │
│   └── test
│       ├── java/com/playwright/qa/test
│       │   ├── CartPageTest.java
│       │   ├── DashboardPageTest.java
│       │   ├── LandingPageTest.java
│       │   ├── LoginTest.java
│       │   ├── ManageCoursesTest.java
│       │   └── NewUserSignUpTest.java
│       │
│       └── resources
│           ├── config.properties
│           ├── testData.xlsx
│           ├── smoke-suite.xml
│           ├── regression-suite.xml
│           ├── full-suite.xml
│           ├── crossbrowser-testing.xml
│           └── testng.xml




# ⚙️ Setup Instructions

## Clone Repository

bash
git clone https://github.com/NPrad1/playwright-automation.git
cd playwright-automation




## Install Dependencies

bash
mvn clean install




## Install Playwright Browsers

bash
playwright install




# ▶️ Test Execution

## Run Complete Test Suite

bash
mvn test




## Run Smoke Suite

bash
mvn test -DsuiteXmlFile=src/test/resources/smoke-suite.xml




## Run Regression Suite

bash
mvn test -DsuiteXmlFile=src/test/resources/regression-suite.xml




## Run Full Suite

bash
mvn test -DsuiteXmlFile=src/test/resources/full-suite.xml




## Run Cross Browser Suite

bash
mvn test -DsuiteXmlFile=src/test/resources/crossbrowser-testing.xml




# 🌐 Cross Browser Testing

Framework supports execution on:

- Chromium
- Firefox
- WebKit

Cross-browser execution is managed using TestNG suite XML configuration.



# 🔄 Retry Mechanism

Framework includes automatic retry handling for flaky test failures using:

- RetryAnalyzer
- RetryListener

Failed tests are automatically re-executed based on retry configuration.



# 📊 Reporting

Framework generates:

- Extent Reports
- TestNG Reports
- Screenshots on failure
- Surefire reports

---

## Extent Report Location

text
test-output/ExtentReport.html




## Surefire Report Location

text
target/surefire-reports/




# 📸 Screenshot Capture

Screenshots are automatically captured for failed test cases.

Example location:

text
test-output/screenshots/



# 📑 Data Driven Testing

Framework supports Excel-based data-driven execution using:

- ExcelUtil.java
- TestDataProvider.java

Test data source:

text
src/test/resources/testData.xlsx



# ⚡ Parallel Execution

Framework supports parallel execution using TestNG XML configuration.

Example:

xml
<suite name="Suite" parallel="tests" thread-count="3">


# 🔔 Logging

Framework uses Log4j2 for centralized logging.

Configuration file:

```text
src/test/resources/log4j2.xml
```

---

# 🔧 Configuration Management

Framework supports configuration-driven execution using:
text
config.properties


Example:

properties
browser=chromium
headless=true
baseUrl=https://freelance-learn-automation.vercel.app/login


---

# 🧪 CI/CD Integration

Framework is integrated with GitHub Actions for Continuous Integration.

CI workflow file:

text
.github/workflows/ci.yml


Features:
- Automated test execution
- Maven build validation
- Browser setup
- CI pipeline execution


# 🧱 Design Patterns Used

- Page Object Model (POM)
- Utility-Based Reusability
- Listener Pattern
- Data Provider Pattern



# 📈 Future Enhancements

- REST Assured API integration
- Docker support
- Allure reporting
- Database validation
- Accessibility testing
- Visual testing
- Environment profiles
- Cloud execution support

---


# 👨‍💻 Author

Pradeep Kumar

GitHub:
https://github.com/NPrad1


# ⭐ Repository Goals

This project is continuously evolving to simulate enterprise-level automation architecture with focus on:

- Scalability
- Maintainability
- Stability
- Reusability
- CI/CD maturity
- Framework engineering best practices
