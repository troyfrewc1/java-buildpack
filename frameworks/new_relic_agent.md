---
layout: default
title: Cloud Foundry Java Buildpack New Relic Agent Framework
component_id: new_relic_agent
repo_root: new-relic
detection_criteria:
  - Existence of a single bound New Relic service<br />
    _Existence of an New Relic service defined by the [`VCAP_SERVICES`](http://docs.cloudfoundry.com/docs/using/deploying-apps/environment-variable.html#VCAP_SERVICES) payload containing a service name, label or tag with `newrelic` as a substring_
tags:
  - new-relic-agent=<version>
---

# New Relic Agent Framework
The New Relic Agent Framework causes an application to be automatically configured to work with a bound [New Relic Service][].

{% include component_metadata.html %}

## User-Provided Service (Optional)
Users may optionally provide their own New Relic service. A user-provided New Relic service must have a name or tag with `newrelic` in it so that the New Relic Agent Framework will automatically configure the application to work with the service.

The credential payload of the service may contain the following entries:

| Name | Description
| ---- | -----------
| `licenseKey` | The license key to use when authenticating

{% include component_configuration.md %}

[s]: https://newrelic.com
