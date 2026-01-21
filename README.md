# Intelligent Registration System - Automation

This folder contains a Selenium WebDriver automation script written in Java. It tests the Registration Form by executing three key scenarios:
1.  **Flow A (Negative)**: Submitting with missing data to verify error handling.
2.  **Flow B (Positive)**: Submitting valid data to verify success state.
3.  **Flow C (Logic)**: verifying dynamic dropdowns and password validation.

## Prerequisites
- Java JDK 11 or higher
- Maven (for dependency management)
- Google Chrome browser installed

## Project Structure
- `pom.xml`: Maven configuration file (dependencies).
- `src/test/java/...`: Contains the `RegistrationAutomation.java` script.

## How to Run
We have set up a local version of Maven in the `tools` folder for you.

1.  **Open Command Prompt** or Terminal in this folder (`automation`).
2.  **Run the script** using the local Maven:
    ```powershell
    & "tools\apache-maven-3.9.6\bin\mvn.cmd" clean test-compile exec:java "-Dexec.mainClass=com.frugal.testing.RegistrationAutomation" "-Dexec.classpathScope=test"
    ```

3.  **Check Results**:
    - Console output will show the test progress (PASS/FAIL logs).
    - **Screenshots** (`error-state.png`, `success-state.png`) will be saved in this folder.

## Troubleshooting
- **Chrome Version**: If the browser doesn't start, ensure your Chrome browser is up to date. The script uses `WebDriverManager` to attempt to match your installed version.
- **Path Issues**: If the page fails to load, verify the path printed in the console `Target: file://...`.
