---
layout: post
title: Architecture Microservices References
categories: [architecture]
tags: [microservices]
description: the collection of Architecture Microservices relate articles.
---

* 2016
  * [Challenges of Microservices Deployments](https://www.infoq.com/news/2016/04/msa-deployment-challenges)
  * [Locating Common Micro Service Performance Anti-Patterns](https://www.infoq.com/articles/Diagnose-Microservice-Performance-Anti-Patterns)
  * Video [Microservices Antipatterns](https://www.infoq.com/presentations/cloud-anti-patterns)
  * Video [The Seven Deadly Sins of Microservices](https://www.infoq.com/presentations/7-sins-microservices)
  * [Microservices in the Real World](https://www.infoq.com/articles/microservices-real-world)
  * [Breaking a Monolithic API into Microservices at Uber](https://www.infoq.com/news/2016/07/uber-microservices)
  * [Scaling Microservices at Gilt with Scala, Docker and AWS](https://www.infoq.com/news/2015/04/scaling-microservices-gilt)
  * [Challenges of Microservices Deployments](https://www.infoq.com/news/2016/04/msa-deployment-challenges)
    > * Microservices require a lot of infrastructure to develop and deploy, so use a platform. "Kubernetes, Swarm, Mesos and their ilk will get you lot of the way there but you still need to unify your monitoring, debugging, continuous pipelines and service discovery mechanisms."
    > * To ensure repeatability and reliable automation, don't let anything in your system be defined by human processes. "Everything must be defined in code, testable and repeatable. For example, your server/VM setup should be orchestrated using docker-machine, puppet, ansible etc."
    > * Develop or use centalised monitoring, logging and alerting. "While a monolithic service is like a beloved pet, you know all of its quirks and habits, micro-services are like cattle; you need all of them to be more or less identical, and managed as a generic herd rather than an individual."
    > * Enforce backwards and forwards compatibility.
    > * Visualise large microservices deployments as a network. "Monitoring and managing a large micro-services deployment is very similar to managing a network system."
  * [The Microservices and DevOps Journey](https://www.infoq.com/presentations/wix-microservices-devops)
  * [Chaos Testing of Microservices](https://www.infoq.com/news/2016/03/chaos-testing-microservices)
* 2015
  * [Microservice Design Patterns](https://dzone.com/articles/microservice-design-patterns)
  * [Seven Microservices Anti-patterns](https://www.infoq.com/articles/seven-uservices-antipatterns)
    > 2) Not taking Automation Seriously:
    We didn't have a strategy for automated deployment and ops monitoring of services (runtime QoS metrics). It obviously increased operational expenses and manual errors during deployment. Several times production deployments caused outages due to configuration errors. The services were always deployed in HA mode and so the number of containers was 3x to the total number of services. The operations team was unable to handle the configuration for each service manually. After a certain time, ops started to complain that the architecture was inefficient as they were not able to handle the increased number of containers. 
    What is the vaccine for this? The recipe has multiple ingredients.  Continuous deployment, if you have not done so, is a must investment and a cultural change that every enterprise should aim for. At least, if you don't have a way to automatically test and deploy – do not do micro-services. Microservices are aiming to drive agility, with the speed we need to change; quality assurance involves each service having automated unit, functional, security and performance testing. Service Virtualization is another powerful concept when we develop services that are integrated with services outside of our control.
    > 5) Manual Configurations Management:
    As we started to do a larger number of services (and the inevitable sprawl due to lack of service lifecycle governance manifested itself) managing the configurations for each service went out of control. Most of our production deployment was not smooth because of configuration failures like the bad password, wrong URL, incorrect values. It became harder and harder to manage these manually. If we had only used application configuration management tools as part of a PaaS or CD…but we didn’t.
    > 6) Versioning Avoidance:
    Naively, we thought it would be only need one version of the service. Then we started to add major, minor versions to accommodate multiple consumers and frequent changes. Eventually, every release had to be a major release since the services were relying on consumer sign off. As a result, the number of containers increased very fast and it became a huge pain to manage them. Lack of runtime governance was another aspect that contributed to this issue. Some enterprises foolishly try to avoid versioning. Services need to be architected assuming that change is inevitable.  Have a strategy to manage the forward compatible service changes and allow your consumers to upgrade gracefully. Otherwise, it will lead to having consumers tightly bound to a service version and break when there is a change.
    The complexity grows as the number of services grows which the microservices world expects. Have a versioning strategy that can allow the consumers a graceful migration and assure providers can transparently deploy changes without affecting anyone. Limit the number of side-by-side major versions in the production and govern them.
  * [Coupling Versus Autonomy in Microservices](https://www.voxxed.com/blog/2015/04/coupling-versus-autonomy-in-microservices/)

## Transactions

* [Transactions in Micro services architecture](http://blog.naturalint.com/transactions-in-micro-services-architecture/)
* [Distributed Transaction Management in a Microservices Architecture](http://www.devx.com/blog/dev_issues/distributed-transaction-management-in-a-microservices-architecture.html)
* [What is the most accepted transaction strategy for microservices](http://programmers.stackexchange.com/a/290952)
