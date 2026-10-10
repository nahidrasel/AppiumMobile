# Appium Mobile Automation

This repository contains Java mobile automation examples using Appium, Selenium, and TestNG. The Maven project is located in `MobileAutomation/` and includes sample Android application packages, page objects, test classes, and a TestNG suite file.

## Prerequisites

- JDK 17
- Maven
- Node.js and Appium Server installed and configured for your environment
- Android SDK and an Android emulator or connected device
- The required Appium driver (for example, UiAutomator2) installed in your Appium setup

## Build and run

From the repository root:

```bash
cd MobileAutomation
mvn test
```

The project includes `testng.xml`; use it to review which tests are grouped into the suite. If your IDE or Maven setup does not automatically select the intended suite, configure TestNG to run that file explicitly.

## Project structure

```text
MobileAutomation/
  pom.xml                         Maven dependencies and Java 17 compiler target
  testng.xml                      TestNG suite configuration
  src/AppiumFramework/            Appium test support and sample app
  src/MobileAutomation/           mobile automation examples
  src/pageObjects/                page-object examples
```

## Device and application configuration

Review `src/AppiumFramework/global.properties` and the relevant test setup classes before running. The current properties refer to a device named `Nahid2`; replace this with the device or emulator name configured in your local environment. The repository includes sample APK files, so verify which APK each test launches before changing application capabilities.

## Troubleshooting

- Confirm the Appium server is running and reachable.
- Confirm the Android device is visible to the Android Debug Bridge (`adb devices`).
- Check that the installed Appium driver matches your Appium server version.
- Do not commit personal device details, access tokens, or credentials.
