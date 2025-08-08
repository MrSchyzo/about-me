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

I am working in [Trade Republic GmbH](https://traderepublic.com) as a backend Software Enginner. I started as part of the 
discovery and insights team that used to own a non-trivial amount of the `wealth` screen, where a user can inspect their portfolio chart,
look for instruments, and look at the portfolio composition.
Recommendations was owner of features such as the search bar, "top movers", "trending searches", "trending stocks", and "top savers".
After a couple of team reshufflings, the teams I've been part of are:
- `Discovery & Insights`, 2022 - 2023
- `Timeline`, 2023
- `Recommendations`, 2023
- `Casual Trading`, 2023 - 2024
- `Trading Experience`, 2024 - 2025
- `Brokerage`, 2025
- `Web Trading`, 2025 - ongoing

## Contributions

### Discovery & Insights

The main focus of this vertical business unit was to make the discovery of instruments as seamless as possible for the users.
This includes contributions like implementing new ranked lists like "top movers", "trending stocks", or "top savers". These lists 
were updated periodically through Airflow DAGs that tap into our Data Warehouse to generate these rankings.
This lead to an increase in the search-to-trade ratio by around 10%, according to our AB tests results based on correlating backend events and
frontend events.

Since this was a user-facing vertical, I worked with mobile engineers closely, supporting them by implementing what they needed to
ship the UX they were aiming for.

In this timeframe I've quickly become the go-to person for Instrument-Search in both development, maintenance, and troubleshooting while gaining
a tiny bit of exposure to our data pipelines.

### Timeline

In order to prepare the company to the upcoming debit card, making Trade Republic an actual bank, I've been borrowed by the timeline team to
rework the old timeline event system into a flexible platform that other teams could've used in self-service to generate events - like card payments - 
that would be visible to the customer in a dedicated `cash` tab within the app.
In this brief timeframe, I helped Senior Engineers designing this platform and its architecture, from designing the data model to laying out the foundations
of the new internal document generation platform. Coding was of course the main part of my day-to-day job.
There are no KPIs about the platform itself, but the `card` team have been used this system since then.

This timeframe hasn't made me gain full ownership of another system, but this allowed me to expand my knowledge of Trade Republic systems quite a bit,
seeing how different teams within the company choose different technologies and patterns.

### Recommendations

Going back to `discovery & insights`, now split into `recommendations` (I was here) and `insights`, we started re-designing the user's portfolio chart system.
The reason of this re-design was to separate cash from invested wealth, since we were going to introduce a debit card that would've made the old chart oscillate a lot 
due to card transactions.
I've been one of the main contributors of the new chart system that is still (as of Sept 2025) powering our portfolio chart UI in our applications. This includes both
discovering which storage technology to use to store millions of timeseries in different resolutions, defining which components to implement and code, and shipping
the feature to our applications. We ended up with a big stateful application that computes all users' portfolio once every 10 minutes, and such big state has brought
interesting challenges in both resource usage and consistency while guaranteeing a fast enough system.

The portfolio-chart project became my second system in which I've been recognised as the go-to person for maintenance, evolutions, and development.
This project was also the one that pushed the adoption of ScyllaDB, a C++ replacement for Apache Cassandra.

### Casual Trading

At the end of 2023, the `recommendations` team have been mashed together with other teams within the same business vertical, giving birth to the `casual trading` team.
The most notable project I've been part on was introducing the new appropriateness testing that allows Trade Republic to be compliant with the regulation about assessing
user knowledge and experience, and show customers the according warnings in case they lack the requirements.

This was also another project in which mobile developers have worked closely with backend, since showing and preparing the appropriateness tests was a non-trivial UX concern
to balance ease of use and regulation compliance. This feature was an example of pragmatism over purism, in which we needed to come up with a quick solution fulfilled
the requirements.

During the start of 2024 I've also helped experimenting with a new Browse screen experience, in particular I've laid out a new source for News feeds and a dedicated
BFF for this new screen. This project has then been paused for one year, before coming back to life.

Another notable project, although not as impactful as appropriateness testing, is the crypto position statements feature. I've been put in charge of this to deliver the feature
end-to-end: from architecture to coding. These statements are still working without any issue since then.

### Trading Experience

At the half of 2024, the `Casual Trading` team has changed its naming into `Trading Experience`, making its mission the customer funnelling from login to trade.
In other words, our mission was to improve guiding the users from wandering around the app to actually becoming an active user, investing their money within our ecosystem.

During this period I've kept contributing in portfolio chart system in order to integrate CFD trading and the Plan d'Épargne en Actions (PEA) in it. Since the last quarter of
2024 I've become the only developer working on portfolio chart. Solidifying my position as the go-to person for this system in all its aspects.

Another notable initiative I've played a significant role in was to make the portfolio chart seamless even in case of a branch migration.
This migration implies a new distinct portfolio would be created for the user, where all their position will be move, and this was a challenge to rise up to in terms of UX:
how to show the user a single portfolio chart as if no migration happened? I've come up with a solution that minimised the needed effort while checking any possible edge case 
during the migration. The solution was rather simple: take the old portfolio history, and merge it with the new portfolio history. In case of partial migration in one data point, 
sum the two portfolios together.

We haven't witnessed any worrying increase in CPU usage or latency, although getting two portfolios history instead of one is clearly more data and work to do for our
system.

At this point in time, I was fully owning the following systems:
- portfolio chart
- instruments search
- appropriateness testing

Everything involving these three systems was involving me too, giving insights and proposing solutions to swiftly integrate new products within these three systems.

### Brokerage

At the start of 2025, there have been a big project under the leadership of our new tech lead: introducing the Spanish mutual funds.
I've been contributing to this big initiative since the beginning and helped shipping it from its inception to its production deployment, although in this case I've been
more on the coding side rather than driving the design and the features.

Regardless of that, this was the biggest project I've been involved with in terms of amount of simultaneous contributors and it was also extremely impactful for the
Spanish market penetration, increasing our Spanish weekly onboardings by 2x.

### Web Trading

At the end of the Spanish Mutual Funds, a new team reshuffle happened. I now work for the web trading team, developing a new upcoming product to attract new type of customers
that are unlike the passive or the casual investor.

In this very moment I'm helping with creating the backend for the new Web UI, and creating an RFC to fetch technical data about instruments, such as SMA, RSI, VWAP, etc.

## Role & Responsibilities

As a software engineer, my responsibilities mainly revolve around being an owner of the teams' project, develop new systems within my vertical, and having an impact in other teams. To give a non-exhaustive list, I have to:
- develop and maintain teams' µservices
- develop and contributing to other teams' µservices
- interact with other functional teams (data, SRE, platform engineers)
- participating in the team's discussions around what to develop and provide technical insights
- interact with external teams when an integration is needed
- onboard newcomers and mentoring more junior engineers
- complying and contributing to the technical best practices
- (used to) help recruiting, in particular:
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
- Kafka - for event sourcing and messaging
- EKS - as the container orchestration
- ArgoCD - as the kubernetes' objects synchronisation mechanism
- GitHub - as the VCS and CI solution
- Terraform - as the IaC synchronisation mechanism
- LGTM - as the go-to stack for observability
- Snyk - as the security static analysis tool
- SonarQube - as the code's static analysis tool

In particular, for my specific team history, I also used:
- AWS S3 - to store and retrieve files from Data Analysis pipelines
- Airflow - to define the DAG of such pipelines
- AWS OpenSearch - to provide text-search capabilities for the search bar
- ScyllaDB - to store every user portfolio valuation time series
- GH Actions - for defining the CI
- AWS RDS - as the go-to RDBMS
- Flyway - as the migration tool for JVM applications
