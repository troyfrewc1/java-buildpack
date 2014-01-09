---
layout: default
title: Cloud Foundry Java Buildpack Java Main Container
detection_criteria:
  - "`Main-Class` attribute set in `META-INF/MANIFEST.MF`, or"
  - "`java_main_class` set in `config/java_main.yml`"
tags:
  - java-main
---

# Java Main Container
The Java Main Container allows an application that provides a class with a `main()` method to be run.  The application is executed with a command of the form:

```bash
<JAVA_HOME>/bin/java -cp . com.gopivotal.SampleClass
```

Command line arguments may optionally be configured.

{% include component_metadata.html %}

## Spring Boot
If the main class is Spring Boot's `JarLauncher`, `PropertiesLauncher` or `WarLauncher`, the Java Main Container adds a `--server.port` argument to the command so that the application uses the correct port.

{% include container_spring_profiles.md %}

## Configuration
For general information on configuring the buildpack, refer to [Configuration and Extension][ce].

The component can be configured by modifying the `config/java_main.yml` file.

| Name | Description
| ---- | -----------
| `arguments` | Optional command line arguments to be passed to the Java main class. The arguments are specified as a single YAML scalar in plain style or enclosed in single or double quotes.
| `java_main_class` | The Java class name to run. Values containing whitespace are rejected with an error, but all others values appear without modification on the Java command line.  If not specified, the Java Manifest value of `Main-Class` is used.

[ce]: ../index.html#Configuration-and-Extension
