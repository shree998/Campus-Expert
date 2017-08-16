<p align="center">
  <img src="http://imgur.com/iQU8c9L.png"/>
  <h4 align="center">RAISe</h4>
  <p align="center">
    <img src="https://img.shields.io/badge/platform-macOS%20%7C%20Linux%20%7C%20Windows-lightgrey.svg"/>
  </p>
</p>


[![Github All Releases](https://img.shields.io/github/downloads/uiot/raise/total.svg)](https://github.com/uiot/raise/releases) [![Packagist](https://img.shields.io/packagist/v/uiot/raise.svg)](https://packagist.org/packages/uiot/raise) [![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0) [![Code Climate](https://codeclimate.com/github/UIoT/RAISe/badges/gpa.svg)](https://codeclimate.com/github/UIoT/RAISe) [![Style CI](https://styleci.io/repos/34536644/shield?style=flat)](https://styleci.io/repos/34536644/) [![Scrutinizer Code Quality](https://scrutinizer-ci.com/g/UIoT/RAISe/badges/quality-score.png?b=sbr)](https://scrutinizer-ci.com/g/UIoT/RAISe/?branch=sbr) [![codecov](https://codecov.io/gh/uiot/RAISe/branch/sbr/graph/badge.svg)](https://codecov.io/gh/uiot/RAISe)
-------------

<b>Builds</b>

Version | Windows | Linux | macOS |Artifacts |
--------|---------|-------|-------|----------|
Latest  | [![Build status](https://ci.appveyor.com/api/projects/status/jjwmx9moinqrha2n?svg=true)](https://ci.appveyor.com/project/sant0ro/raise-askjk)   | [![Build Status](https://travis-ci.org/uiot/raise.svg?branch=sbr)](https://travis-ci.org/uiot/raise) | None Yet | [Artifacts](https://ci.appveyor.com/project/sant0ro/raise-askjk/branch/sbr/artifacts) |

<b>Core Features</b>

| Feature  |  Coded?       | Description  |
|----------|:-------------:|:-------------|
| Home Page | &#10004; | Ability of accessing the main route of **RAISe** to check the status of the middleware. |
| Not Found Route | &#10004; | Ability of accessing a non-existent route and receive a response of the route doesn't exists. |
| Register a Client | &#10004; | Ability of Registering a Client within RAISe. |
| Revalidate a Client | &#10004; | Ability of Revalidating a Client when the Token expires. |
| Register a Service | &#10004; | Ability of Registering a Service or multiple Services in one time within RAISe. |
| Send Data | &#10004; | Ability of Sending Data froma  Service+Client within RAISe. |
| List a Client or Clients | &#10004; | Ability to Get a Client or multiple Clients, list and filter the parameters for the Response. |
| List a Service or Services | &#10004; | Ability to Get a Service or multiple Services, list and filter the parameters for the Response. |
| List and filter Data | &#10004; | Ability to get Data, filter it with multiple simple parameters and advanced parameters like time interval. |
| List and filter Data Values | &#10004; | Ability to list the Values of Data Sets, filter it with multiple simple parameters and advanced parameters like time interval. |

<b>Social Features</b>

| Feature  |  Coded?       | Description  |
|----------|:-------------:|:-------------|
| Create a Permission | &#10008; | Ability to create a new type of Permission on RAISe |
| Edit a Permission | &#10008; | Ability to Edit Permissions on RAISe |
| Remove a Permission | &#10008; | Ability to Remove Permissions from RAISe |
| Create a Relationship | &#10008; | Ability to manually specify relationships between services and/or clients from different groups. |
| Edit a Relationship | &#10008; | Ability to update the members of a specific Relationship |
| Remove a Relationship | &#10008; | Ability to Remove existent Relationships from RAISe |
| Create a Profile/Group | &#10008; | Ability to create a Profile. Defining Permissions and Entities (Relations) |
| Edit a Profile/Group | &#10008; | Ability to edit the members and/or permissions from a Profile |
| Remove a Profile/Group | &#10008; | Ability to Remove Profiles from RAISe |

<b>Management Features</b>

| Feature  |  Coded?       | Description  |
|----------|:-------------:|:-------------|
| Show Logs | &#10008; | Ability to list and show RAISe Logs |
| Show Audit | &#10008; | Ability to list and show RAISe Audit (Logs Inference) |

<b>Data Visualization System</b>

| Feature  |  Coded?       | Description  |
|----------|:-------------:|:-------------|
| Show RAISe Environment Settings | &#10004; | View that displays the actual environment settings and alerts. |
| Search Feature | &#10004; | Feature to explore (search) for clients and services, by name or tag. |
| Home Page | &#10004; | View to list Clients and Logs (last registered).  |
| Hook a Client | &#10004; | View to see detailed data about a Client (map location, description, graphs and it services)  |
| Hook a Client Service | &#10004; | View to see detailed info about a specific service and list last 100 data entries.  |

<b>RAISe IntelliX</b> (Algorithms)

| Feature  |  Coded?       | Description  |
|----------|:-------------:|:-------------|
| Data Clustering | &#10008; | Ability to cluster data by dimensional criteria, like, time, space, tags and social relationships. |
| Data Behaviour Analysis | &#10008; | Ability to scan and determine if a specific set of data has strange behaviour |
| Data Confiability | &#10008; | Ability to scan and determine if a specific set of data it's fair or not |
| Social Relationships | &#10008; | Ability to create social relationships and group relationships |

UIoT RAISe
----------

**RAISe** is an *Internet of Things* open middleware. Made to handle and store knowledge and be a restful service layer for IoT applications, clients and devices.

**RAISe** is open source, and maintained by the [Universal Internet of Things](https://uiot.org) open source project and the [University of Brasília](http://www.unb.br).

### What the word means?

> **RAISe** is an acronym for *RESTful API for Internet of Things Services*. In terms, RAISe it's abstract and generic and can handle data, knowledge and information for any type of architecture that you may use, require, create or contribute.

### Go deep!

> In fact, **RAISe** it's a knowledge layer, in other words, a middleware for the *Internet of Things*, we can actually call it as an surface too.
> The *API's* of **RAISe** are really simple, you can search more about what each *actor*, *component*, *api* and *entities* of **RAISe** on our [wiki](wiki). You also can read the papers related to the **RAISe** architecture and approaches, our went to our [academics repository](https://github.com/uiot/academics) and learn/read more about the **UIoT** architecture, papers, power-points and other related academic stuff.

Installing
----------

You can install <b>RAISe</b> by easily going on our [Wiki](wiki) and check the Installation Pages.

Any troubles that you may/have, check our [Contributing/Reporting Guide](CONTRIBUTING.md).

You can also check the [Table of Contents of the RAISe Installer](wiki/installer-reference).

Contributing
------------

You can <b>Contribute</b> on RAISe! <b>RAISe</b> is open source, and everyone can contribute on it.

Check the [Contributing Guide](CONTRIBUTING.md).

Documentation
-------------

You can learn more about the <b>RAISe</b> architecture by checking our [Wiki](wiki)

<b>You also may read those scientific papers</b> that explain about the <b>UIoT</b> architecture and the key features, and lot more about <b>RAISe</b>
* [Design and Evaluation of a Services Interface for the Internet of Things](http://dl.acm.org/citation.cfm?id=3023305)
* Other papers being added on the list.

You can also **fetch** the [API Documentation](docs/) and check it **online** by using [Swagger UI](http://docs.uiot.org/raise/).

<br>
<br>
<img align="right" src="http://imgur.com/l5hOjj4.gif">
