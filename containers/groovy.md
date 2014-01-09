---
layout: default
title: Cloud Foundry Java Buildpack Groovy Container
component_id: groovy
repo_root: groovy
detection_criteria:
  - A `.groovy` file exists which has a `main()` method, or
  - A `.groovy` file exists which is not a POGO (a POGO contains one or more classes), or
  - A `.groovy` file exists which has a shebang (`#!`) declaration, and
  - No `.class` files exist
tags:
  - groovy=<version>
---

# Groovy Container
The Groovy Container allows uncompiled Groovy files (i.e. `*.groovy`) to be run.

{% include component_metadata.html %}
{% include component_configuration.md %}
