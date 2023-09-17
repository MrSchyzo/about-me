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

I am working in [Trade Republic GmbH](https://traderepublic.com) as an Engineer II on backend. I started as part of the 
recommendations team that owns a non-trivial amount of the `wealth` screen, where a user can inspect their portfolio chart,
look for instruments, and look at the portfolio composition.
Recommendations was owner of features such as the search bar, "top movers", "trending searches", "trending stocks", and "top savers".
Now the team has been merged into the `browse & insights` team while keeping the ownership of the aforementioned features.

In `browse & insights`, I:
- (currently) contribute to the enhancement of the users' portfolio chart
- help in shaping such enhancement by writing RFCs describing the obtainable state given the time
- own the `instrument-search` µservice, and as owner I am the point of contact in case any engineer needs support in modifying
  such µservice

Depending on the company needs, I also happen to join other teams to help with their projects' development like the `timeline` team, in
which I helped with the platformisation of Trade Republic timeline. This platformisation allows us to launch new products more easily
while avoiding external teams to depend on `timeline` team for new features.

This is my first experience in an international English-speaking company 
and it is where my knowledge of cloud-native development grew further. I've also had opportunities to transition into 
a T-shaped engineer able to tackle problems with a bit more breadth, not only focusing on coding, but also actively contributing to 
make choices in the architecture while shipping medium-sized features.
Also, here is where I made use of GH Actions for the first time.

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
- help recruiting, in particular:
    - assessing take-home tasks
    - discussing solutions to the take-home tasks with the candidates
    - participating in the live coding interview

## Involved technologies

In Trade Republic backends we commonly use:
- JVM 17+ - as the runtime
- Spring Boot - as the go-to framework
- Kotlin - as the go-to programming language
- Vert.x - as a backend reactive library
- RabbitMQ - as the messaging system
- EKS - as the container orchestration
- ArgoCD - as the kubernetes' objects synchronisation mechanism
- GitHub - as the VCS and CI solution
- Terraform - as the IaC synchronisation mechanism
- DataDog - as the go-to tool for observability
- Snyk - as the security static analysis tool
- SonarQube - as the code's static analysis tool

In particular, for `browse & insights`, we also use:
- AWS S3 - to store and retrieve files from Data Analysis pipelines
- Airflow - to define the DAG of such pipelines
- AWS OpenSearch - to provide text-search capabilities for the search bar
- ScyllaDB - to store every user portfolio valuation evolution over time

Other technologies I sometimes use by contributing to other projects:
- GH Actions - for defining the CI
- AWS RDS - as the go-to RDBMS
- Flyway - as the migration tool for JVM applications
