---
title: Spring Framework coding standards
description: Rules and conventions to follow when developing Spring apps
---

This document outlines the standards for writing projects in Spring Framework (including Spring Boot).
Remember that everything in [Java standards page](/coding/java.html) is also applicable and binding for Spring Framework projects. 

## Coding style

* Use short forms of `@RequestMapping` like `@GetMapping`, `@PutMapping` etc.
* Use constructor injection.
* Use `@lombok.RequiredArgsConstructor` if constructor doesn't have `@Value`.
* Keep naming consistent.
  - If they prefer naming things in plural before you keep it that way and vice-versa.
  - If you are starting a new project prefer plurals when make sense. (E.g. `templates/users` but not `templates/securities`)

## Dependencies

* Use dev-tools, Lombok, h2db by default.
* Use Logback as logging implementation.
* Don't use version for any dependency which is already defined in 
<a href="https://github.com/spring-projects/spring-boot/blob/master/spring-boot-project/spring-boot-dependencies/pom.xml" target="_blank">Spring Boots's parent pom</a>


## Configuration

* Use `.yml` files for configuration.
* Group all custom configuration under `app` namespace. For example,

```
app:
	notification-email:
		smtp: smtp.example.com
		port: 25
	retry-timeout: 10s
	facebook:
		api-key: 123123
		secret: qweasd
```

* Have h2db configured for dev mode. See
<a href="https://kodgemisi.atlassian.net/wiki/spaces/SDS/pages/605913382/Configure+h2db+for+Spring+Boot" target="_blank">
	Configure h2db for Spring Boot
</a>
page for config details.
* Prefer environment variables to configure the app in all environments, but declare everything in .yml explicitly 
and use placeholders (i.e. ${SOME_PLACEHOLDER}) which will be overriden by environment variables.
  - Provide usable defaults for **development environment** in `application-dev.yml`. Put all config values necessary for application except
  any credentials in development configuration.
* Don't use hardcoded config values in configuration for any credentials including usernames, passwords, API keys etc.
See <a href="https://docs.spring.io/spring-boot/docs/current/reference/html/boot-features-external-config.html" target="_blank">externalized configuration</a> for more information of Spring Boot's config.