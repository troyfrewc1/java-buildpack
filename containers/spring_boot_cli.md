---
layout: default
title: Cloud Foundry Java Buildpack Spring Boot CLI Container
component_id: spring_boot_cli
repo_root: spring-boot-cli
detection_criteria:
  - The application has one or more `.groovy` files in the root directory, and
  - All the application's `.groovy` files in the root directory are POGOs (a POGO contains one or more classes), and
  - None of the application's `.groovy` files in the root directory contain a `main` method, and
  - None of the application's `.groovy` files in the root directory contain a shebang (`#!`) declaration, and
  - The application does not have a <tt>WEB-INF</tt> subdirectory of its root directory.
tags:
  - spring-boot-cli=<version>
---

# Spring Boot CLI Container
The Spring Boot CLI Container runs one or more Groovy (i.e. `*.groovy`) files using Spring Boot CLI.

{% include component_metadata.html %}
{% include container_spring_profiles.md %}
{% include component_configuration.md %}
