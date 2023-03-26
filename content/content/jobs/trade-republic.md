+++
title = "Working in Trade Republic"
description = "Working in Trade Republic"
date = "2023-03-26"
author = "Mr.Schyzo"
+++

# Some bureaucratic details
- company: Trade Republic GmbH
- contract: Italian NCLA, full time
- place: full-remote in Pistoia, PT
- start: May 2022

# As an Engineer II (05/2022 - current)

## Summary

I am working in [Trade Republic GmbH](https://traderepublic.com) as an Engineer II on backend. I am part of the 
recommendations team that owns a non-trivial amount of the screens of the Trade Republic app, in particular the `discover`
screen.
Recommendations offers features such as the search bar, "top movers", "trending searches", "trending stocks", and "top savers".
In general our team's scope is anything that has to relate to exploring and discovering instruments.
Depending on the company needs, I also happen to join other teams to help with their projects' development.

## Role & Responsibilities

As a mid-level engineer, my responsibilities mainly revolve around being an owner of the teams' project and having an impact
even in other teams. To give a non-exhaustive list, an Engineer II has to:
- develop and maintain teams' µservices
- develop and contributing to other teams' µservices
- interact with other functional teams (data, SRE, platform engineers)
- participating in the team's discussions around what to develop and provide technical insights
- interact with external teams when an integration is needed
- onboard newcomers and mentoring more junior engineers
- complying and contributing to the technical best practices
- (I've yet to do this) participate in recruiting

## Involved technologies

In Trade Republic backends we commonly use:
- JVM 17+ - as the runtime
- Spring Boot - as the go-to framework
- Kotlin - as the go-to programming language
- RabbitMQ - as the messaging system
- EKS - as the container orchestration
- ArgoCD - as the kubernetes' objects synchronisation mechanism
- GitHub - as the VCS and CI solution
- Terraform - as the IaC synchronisation mechanism
- DataDog - as the go-to tool for observability
- Snyk - as the security static analysis tool
- SonarQube - as the code's static analysis tool

In particular, for Recommendations, we also use:
- AWS S3 - to store and retrieve files from Data Analysis pipelines
- Airflow - to define the DAG of such pipelines
- AWS OpenSearch - to provide text-search capabilities for the search bar

Other technologies I sometimes use by contributing to other projects:
- GH Actions - for defining the CI
- AWS RDS - as the go-to RDBMS
- Flyway - as the migration tool for JVM applications
