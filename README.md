atlas-appcenter
=================

[![Gradle Plugin ID](https://img.shields.io/badge/gradle-net.wooga.build--unity-brightgreen.svg?style=flat-square)](https://plugins.gradle.org/plugin/net.wooga.build-unity)
[![Build Status](https://wooga-shields.herokuapp.com/jenkins/s/https/atlas-jenkins.wooga.com/job/atlas-plugins/job/atlas-appcenter/job/master.svg?style=flat-square)]()
[![Build Status](https://img.shields.io/travis/wooga/atlas-appcenter/master.svg?style=flat-square)](https://travis-ci.org/wooga/atlas-appcenter)
[![Coveralls Status](https://img.shields.io/coveralls/wooga/atlas-appcenter/master.svg?style=flat-square)](https://coveralls.io/github/wooga/atlas-appcenter?branch=master)
[![Apache 2.0](https://img.shields.io/badge/license-Apache%202-blue.svg?style=flat-square)](https://raw.githubusercontent.com/wooga/atlas-appcenter/master/LICENSE)
[![GitHub tag](https://img.shields.io/github/tag/wooga/atlas-appcenter.svg?style=flat-square)]()
[![GitHub release](https://img.shields.io/github/release/wooga/atlas-appcenter.svg?style=flat-square)]()

This plugin is work in progress.

# Applying the plugin

**build.gradle**
```groovy
plugins {
    id 'net.wooga.appcenter' version '1.0.0'
}
```

AppCenter extension
-------------------

The extension allows to set the basic properties for appcenter

```groovy
appCenter {
   apiToken = ""
   owner = ""
   applicationIdentifier = ""
   defaultDestinations = ["", ""]
   publishEnabled = false
}
```

The properties are by default looked up in the gradle properties and/or environment.

| property              | gradle property name              | environment variable                |
| --------------------- | --------------------------------- | ----------------------------------- |
| apiToken              | `appCenter.apiToken`              | `APP_CENTER_API_TOKEN`              |
| owner                 | `appCenter.owner`                 | `APP_CENTER_OWNER`                  |
| applicationIdentifier | `appCenter.applicationIdentifier` | `APP_CENTER_APPLICATION_IDENTIFIER` |
| defaultDestinations   | `appCenter.defaultDestinations`   | `APP_CENTER_DEFAULT_DESTINATIONS`   |
| publishEnabled        | `appCenter.publishEnabled`        | `APP_CENTER_PUBLISH_ENABLED`        |

Development
===========

[Code of Conduct](docs/Code-of-conduct.md)

Gradle and Java Compatibility
=============================

Built with Oracle JDK7
Tested with Oracle JDK8

| Gradle Version  | Works  |
| :-------------: | :----: |
| < 5.0           | ![no]  |
| 5.0             | ![no]  |
| 5.1             | ![yes] |
| 5.2             | ![yes] |
| 5.3             | ![yes] |
| 5.4             | ![yes] |
| 5.5             | ![yes] |
| 5.6             | ![yes] |
| 5.6             | ![yes] |
| 6.0             | ![yes] |
| 6.1             | ![yes] |
| 6.2             | ![yes] |
| 6.3             | ![yes] |
| 6.4             | ![yes] |
| 6.5             | ![yes] |
| 6.6             | ![yes] |
| 6.6             | ![yes] |
| 6.7             | ![yes] |
| 6.8             | ![yes] |
| 7.0             | ![yes] |

> (*) Setting multiple distribution groups via the extionsion `defaultDestination` or in the publish task `destination` is not supported.
> Either use the setter `setDefaultDestination`/`setDestination` or invoke `defaultDestination`/`destination` multiple times with a single group

LICENSE
=======

Copyright 2018-2021 Wooga GmbH

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

<http://www.apache.org/licenses/LICENSE-2.0>

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

<!-- Links -->
[gradle]:               https://gradle.org/ "Gradle"
[gradle_finalizedBy]:   https://docs.gradle.org/3.5/dsl/org.gradle.api.Task.html#org.gradle.api.Task:finalizedBy
[gradle_dependsOn]:     https://docs.gradle.org/3.5/dsl/org.gradle.api.Task.html#org.gradle.api.Task:dependsOn

[yes]:                  https://resources.atlas.wooga.com/icons/icon_check.svg "yes"
[no]:                   https://resources.atlas.wooga.com/icons/icon_uncheck.svg "no"

