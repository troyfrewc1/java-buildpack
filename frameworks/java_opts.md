---
layout: default
title: Cloud Foundry Java Buildpack Java Options Framework
detection_criteria:
  - "`java_opts` set in the `config/java_opts.yml` file"
tags:
  - java-opts
---

# Java Options Framework
The Java Options Framework contributes arbitrary Java options to the application at runtime.

**NOTE:** passing Java options using a `JAVA_OPTS` environment variable is not supported and will not work.

{% include component_metadata.html %}

## Configuration
For general information on configuring the buildpack, refer to [Configuration and Extension][ce].

The component can be configured by modifying the `config/java_opts.yml` file.

| Name | Description
| ---- | -----------
| `java_opts` | The Java options to use when running the application.  All values are used without modification when invoking the JVM. The options are specified as a single YAML scalar in plain style or enclosed in single or double quotes.

[ce]: ../index.html#Configuration-and-Extension
