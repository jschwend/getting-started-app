# Where to host this basic application

* Status: proposed
* Deciders: Marcelo Tourne, Roberto Pioli, Frederic Jambusewaran
* Date: 2024-04-23

Technical Story: We need SSL, load balancing, fail over, persistent storage, auto CI/CD

## Context and Problem Statement

This application must be secure but still accessible by both McK colleagues and external users.
All non-functional aspects must be considered and implemented if possible.

## Decision Drivers

* Ease of use
* Little skills needed
* Reliable
* Secure
* Recoverable

## Considered Options

* Heroku
* AWS Beanstalk
* Azure Web App
* Render

## Decision Outcome

Chosen option: "Azure Web App", because comes out best when considering enterprise needs and minimal support resources.

### Positive Consequences

* Speed to market
* Foster trial-and-error innovation
* Reduces cost of ownership

### Negative Consequences

* None found

## Pros and Cons of the Options

### Heroku

Owned and operated by SalesForce

* Good, because Oldest PaaS provider
* Bad, because Expensive
* Bad, because New purchase
* Bad, because Lack of in-house experience

### AWS Beanstalk

Amazon's forray into PaaS

* Good, because Existing vendor
* Good, because Scriptable with TFE
* Good, because In-House knowledge
* Bad, because No GitHub interaction
* Bad, because No auto CI/CD
* Bad, because We still maintain and support low level components

### Azure Web App

Microsoft offering

* Good, because Easy to setup
* Good, because Scriptable with TFE
* Good, because CLI, API, Console, & VS Code integrations
* Good, because GitHub intgration with auto CI/CD
* Good, because Dev->Stg->Prod lifecycle environments and promotion
* Good, because Existing vendor, no new purchase
* Good, because In-house knowledge and experience
* Good, because Docker container support
* Good, because Log aggregation with Splunk/DynaTrace
* Bad, because None

### Render

New player in the PaaS space

* Good, because Single purpose driven
* Good, because Ease of use and setup
* Good, because Full GitHub integration & CI/CD automation
* Good, because Docker container support
* Bad, because Not fully enterprise mature
* Bad, because Lacks log aggregation with Splunk/DynaTrace
