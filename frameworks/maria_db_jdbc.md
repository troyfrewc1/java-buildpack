---
layout: default
title: Cloud Foundry Java Buildpack MariaDB JDBC Framework
component_id: maria_db_jdbc
repo_root: mariadb-jdbc
detection_criteria:
  - Existence of a single bound MariaDB or MySQL service<br />
    _Existence of a MariaDB service is defined as the [`VCAP_SERVICES`](http://docs.cloudfoundry.com/docs/using/deploying-apps/environment-variable.html#VCAP_SERVICES) payload containing a service who's name, label or tag has `mariadb` as a substring_<br />
    _Existence of a MySQL service is defined as the [`VCAP_SERVICES`](http://docs.cloudfoundry.com/docs/using/deploying-apps/environment-variable.html#VCAP_SERVICES) payload containing a service who's name, label or tag has `mysql` as a substring_
  - No existing MariaDB or MySQL JDBC JAR<br />
    _Existence of a MariaDB JDBC JAR is defined as the application containing a JAR who's name matches `mariadb-java-client*.jar`_<br />
    _Existence of a MySQL JDBC JAR is defined as the application containing a JAR who's name matches `mysql-connector-java*.jar`_
tags:
  - maria-db-jdbc=<version>
---

# MariaDB JDBC Framework
The MariaDB JDBC Framework causes a JDBC driver JAR to be automatically downloaded and placed on a classpath to work with a bound [MariaDB][ma] or [MySQL][my] service.  This JAR will not be downloaded if the application provides a MariaDB or MySQL JDBC JAR itself.

{% include component_metadata.html %}

## User-Provided Service (Optional)
Users may optionally provide their own MariaDB or MySQL service. A user-provided MariaDB or MySQL service must have a name or tag with `mariadb` or `mysql` in it so that the MariaDB JDBC Framework will automatically download the JDBC driver JAR and place it on the classpath.

{% include component_configuration.md %}

[ma]: https://mariadb.com
[my]: http://www.mysql.org
