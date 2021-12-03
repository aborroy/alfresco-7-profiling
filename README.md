# Alfresco 7 Profiling with Docker

This project includes different **profiling** methods when using Docker Compose deployments with Alfresco Community 7.x

* [visual-vm](/visual-vm) is profiling Alfresco Repository, Alfresco Search Services and Alfresco Transform Service using [VisualVM](https://visualvm.github.io)
* [jfr](/jfr) is profiling Alfresco Repository, Alfresco Search Services and Alfresco Transform Service using [JDK Mission Control](https://www.oracle.com/java/technologies/javase/products-jmc8-downloads.html)
* [yourkit](/yourkit) is profiling Alfresco Search Services using [YourKit Java Profiler](https://www.yourkit.com/download/). This product requires using a paid license.

These configurations are **not** intended to be used in production systems, as they have impact in performance.

## VisualVM

```
$ cd visual-vm
$ docker-compose up --build --force-recreate
```

JMX Endpoints:

* http://127.0.0.1:9000 - alfresco
* http://127.0.0.1:9001 - transform
* http://127.0.0.1:9002 - search

## Java Flight Recording with JDK Mission Control

```
$ cd jfr
$ docker-compose up --build --force-recreate
```

JMX Endpoints:

* http://127.0.0.1:9000 - alfresco
* http://127.0.0.1:9001 - transform
* http://127.0.0.1:9002 - search

## YourKit

```
$ cd yourkit
$ docker-compose up --build --force-recreate
```

YourKit endpoint:

* http://127.0.0.1:10001 - search
