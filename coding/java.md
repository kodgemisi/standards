---
title: Java coding standards
description: Standarts every developer should follow when writing Java code
---

This document outlines the standards for writing projects in Java.

## Tooling

* Use JetBrains _IntelliJ IDEA Community Edition_ installed via [Toolbox App](https://www.jetbrains.com/toolbox/app/). **Don't install IDEA independently.**
  - Enable `Update Toolbox App automatically` and `Update all tools automatically` options from settings of Toolbox App.
  - You can enable `Keep only the latest version` option to save disk space. This one is optional but highly recommended.
* Use Maven unless it's an Android project or the framework explicitly propose to use another building tool.

## Coding style

* For any Java project you should import IDE settings which includes coding style, license templates etc.
* Format all **your** code before commiting. Don't format other's code.
* Never use `System.out` and `System.err`.
  - If you somehow have to, clearly document inline. Remember that it have to have a very plausable reason.

## Maven

* Use parametric versions for every dependency. I.e. keep versions in `<properties>` tag.
* In dependencies sections, declare your dependencies in following order:
  - _Although the declaration order of dependencies does not matter in Maven, it matters for developers (readability, maintainability)._
  1. Provided dependencies
  2. Framework dependencies
  3. 3rd party dependencies with implicit versioning (I.e. versions coming from parent pom)
  4. 3rd party dependencies with explicit versioning 
  5. Framework's development dependencies 
  6. 3rd party development dependencies
  7. Test dependencies
* Have following three properties in every `pom.xml`.

```xml
<properties>
	<project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>
	<project.reporting.outputEncoding>UTF-8</project.reporting.outputEncoding>
	<java.version>the-version</java.version>
</properties>
```

* Use following pattern for version parameters in `pom.xml`:<br>
`the-library-name-in-artifact-id.version`
  - If the artifactId is too vague then use groupId + artifactId