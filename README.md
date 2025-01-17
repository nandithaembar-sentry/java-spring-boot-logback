# sentry-demos/java-spring-boot-logback

## Overview

This example shows how to integrate Sentry into a Java Spring Boot project
integrating with logback.

Demonstrates the following features:
- SDK integration
- Configuration
- Releases/Commits
- Event management
- Tags, MDC, additional data

**Official Sentry documentation** found here: 
https://docs.sentry.io/platforms/java/guides/logback/

## Setup
#### Versions

 dependency    | version
| ------------- |:-------------:|
| sentry-logback | 4.1.1 |
| sentry-spring-boot-starter | 4.1.1 |
| Gson | 2.8.6 |
| Spring Boot | 4.17.1 |
| java | 1.8 |

## First-time Setup
1. Update the Sentry DSN to your project's DSN in application.properties
2. Ensure that `SENTRY_AUTH_TOKEN` is set in your ENV variables

## Run
Execute the project by running 
```
$ make
```

Hit the various APIs via another demo (e.g. https://github.com/sentry-demos/react) or tool that calls API (e.g. localhost:8080/handled) such as Postman, Curl, etc.

## Technical Notes or Troubleshooting
You can change the log level for events in the `application.properties` file.
The minimum event level is set to `info` by default which is probably
too verbose. 

## Primary files
`Application.java` - this has the main code for the application and shows
how to add tags and extra data via Sentry.configureScope as well as add
MDC data
`application.properties` - include the Sentry project properties here, as well
as set the log levels to send to Sentry
`pom.xml` - including the required libraries for the project

# GIF
![Alt Text](express-js-demo.gif)

## Sentry Documentation
https://docs.sentry.io/platforms/java/guides/logback/