# data-mesh-and-cloud

> My thought dump on data mesh and cloud

One of the principle of data mesh architecture is having a self-serving platform.

Because the responsibility is now decentralized to each domain team, so are the abilities to build, deploy, monitor a data product.

## Infrastructure

Each domain team will then need to be able to provisioning infrastructure by their own, but this is hard to replicated to each domain team.

Eventually, we see the need for a self-serving infrastructure as a platform in order to enable those domain teams, giving them full autonomy in term of infrastructure and everything.

## Data infrastructure as platform

Cloud is the perfect match for this. They have been building those kind of self-service infrastructure platform for quite awhile now.

We don't want to duplicate those effort. We want to focus on how to help domain teams to "build new data products quickly" (more on that later in success metrics later).

One of the common pitfalls of this is turning data infrastructure platform into a data platform. You have to start treating domain knowledge like second-class citizen now. Once you need a domain specific knowledge to solve a problem, you have to step back because you're probably on the track back to monolith data platform.

Back to why cloud is perfect fit for this? It's because things on cloud are just logical distribution. It's easy to take a S3 bucket from one domain team and add it to your central infrastructure layer. Note that it's still centralized, in the sense of management only.

The infrastructure is also still centralized but we can provide Spark cluster without configuring & managing it. The cloud is even better when you're not happy with the offering from data infrastructure as platform team. You can just go spun up a EMR cluster for processing yourselves. (Only if you must because of interopability, etc..)

## The tech stack 

We will also need to new kind of problems araise when adopting data mesh: interopability and interconnectivity.

Team A might use k8s and team B might be using Spark on Databricks cluster for example.

We didn't have this kind of problem before as everything used to be centralized.

For data mesh to be widely adopted, we need to agree on the data infrastructure stack to be converged: let's say Spark on K8s for example.

All of this may sound very familiar with DevOps principles, whereas we need to make all the data infrastructure and whatnot, available to generalist developers.

We need to abstract tooling to support domain teams creating, running and maintaining workflows.

## A great data platform

To make a succcessful data platform, we need to provide the following:

1. An unified, easy-to-use data pipeline declaration and orchestration (E.g: Apache Beam with Spark as runner?!)
1. Data product schema.
1. Data product versioning.
1. Unified access control/logging.
1. Data product monitoring/logging/alerting.
1. Data product discovery.
1. Federated identity management (that goes without saying).

## Success metrics

Same as [DevOps success metrics](https://www.atlassian.com/devops/frameworks/devops-metrics), a success data platform will enable domain teams to do "create a new data product" faster.
