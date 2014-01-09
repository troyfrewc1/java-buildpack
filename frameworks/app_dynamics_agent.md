---
layout: default
title: Cloud Foundry Java Buildpack AppDynamics Agent Framework
component_id: app_dynamics_agent
repo_root: app-dynamics
detection_criteria:
  - Existence of a single bound AppDynamics service<br />
    _Existence of an AppDynamics service defined by the [`VCAP_SERVICES`](http://docs.cloudfoundry.com/docs/using/deploying-apps/environment-variable.html#VCAP_SERVICES) payload containing a service name, label or tag with `app-dynamics` as a substring_
tags:
  - app-dynamics-agent=<version>
---

# AppDynamics Agent Framework
The AppDynamics Agent Framework causes an application to be automatically configured to work with a bound [AppDynamics Service][s].

{% include component_metadata.html %}

## User-Provided Service
When binding AppDynamics using a user-provided service, it must have name or tag with `app-dynamics` in it.  The credential payload can contain the following entries:

| Name | Description
| ---- | -----------
| `account-access-key` | (Optional) The account access key to use when authenticating with the controller
| `account-name` | (Optional) The account name to use when authenticating with the controller
| `host-name` | The controller host name
| `port` | (Optional) The controller port
| `ssl-enabled` | (Optional) Whether or not to use an SSL connection to the controller

{% include component_configuration.md %}

[s]: http://www.appdynamics.com
