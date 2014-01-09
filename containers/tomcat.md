---
layout: default
title: Cloud Foundry Java Buildpack Tomcat Container
component_id: tomcat
repo_root: tomcat
detection_criteria:
  - Existence of a `WEB-INF/` folder in the application directory and [Java Main](java_main.html) not detected
tags:
  - tomcat=<version>
  - tomcat-buildpack-support=<version>
---

# Tomcat Container
The Tomcat Container allows servlet 2 and 3 web applications to be run.  These applications are run as the root web application in a Tomcat container.

{% include component_metadata.html %}
{% include container_spring_profiles.md %}
{% include component_configuration.md %}

## Supporting Functionality
Additional supporting functionality can be found in the [`java-buildpack-support`][s] Git repository.

[s]: https://github.com/cloudfoundry/java-buildpack-support
