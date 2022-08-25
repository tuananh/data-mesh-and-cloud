# data-mesh-and-cloud

One of the principle of data mesh architecture is having a self-serving platform.

Because the responsibility is now decentralized to each domain team, so are the abilities to build, deploy, monitor a data product.

## Infrastructure

Each domain team will then need to be able to provisioning infrastructure by their own, but this is hard to replicated to each domain team.

Eventually, we see the need for a self-serving infrastructure as a platform in order to enable those domain teams, giving them full autonomy in term of infrastructure and everything. Cloud is the perfect match for this.

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
