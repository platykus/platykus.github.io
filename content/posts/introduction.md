---
title: "Introduction"
date: 2022-07-15T16:16:20-05:00
draft: true
---

Welcome to Platykus, my laboratory for exploring platform engineering on
Kubernetes clusters in public clouds.

## Who am I?

I love learning new things and building interesting and useful stuff with
that knowledge, as well as sharing it with other like-minded people.

I'm an experienced polyglot programmer with a background in full-lifecycle
systems development, primarily of highly-available and scalable distributed
systems including commercial massively-multiplayer online games and big data
processing and storage systems.

My career has brought me in contact with many other disciplines than just
programming, however, including:

- software design and quality engineering
- requirements capture and management
- configuration and change management
- systems design and engineering
- network design and engineering
- database design and implementation
- docker images and containers
- administration of fleets of Linux hosts on bare-metal and virtual machines
- management of containers at scale on Kubernetes clusters
- application and infrastructure security

I've learned much over the years from these, and have become a DevSecOps guy.

I do have one admission to make, however.

I'm lazy and hate manual labor, but much like a symphonic score needs an
orchestra to be performed, my software systems needs a platform to run on.

I bet yours does too.

## What is a Platform?

For my purposes, a Platform is a service that enables application developers to
productively build, run, debug, and manage their applications hosted on the
platform, without having to know details of its infrastructure resources or
their management and operations.

A shared-responsibility model is used to allow both application developers and
Platform operators to better understand the scope and limits of their own
responsibilities, as well as any service level agreements between them.

One of the earliest and most popular examples of a commercial Platform as a
Service (_PaaS_) is [Heroku](https://www.heroku.com/).

## Why build a Platform?

While convenient, commercial platforms have some disadvantages with respect to:

- __affordability__ - services may be cost-prohibitive, especially at scale
- __capability__ - services may not fit your system requirements
- __reliability__ - outages are outside your control and may be catastrophic
- __stability__ - languages, services and toolchains may not be stable over time
- __portability__ - systems and their data may not be easily moved to another
  platform to enjoy better affordability, reliability or suitability

What if we could have the benefits of an affordable, capable, reliable, stable,
and portable custom Platform capable of being deployed simply in any public
cloud, or locally on a developer workstation? What would it take to build such
a beast?

With the availability of public clouds and Infrastructure as a Service (_IaaS_)
it can be done. Multiple cloud vendors provide _IaaS_ suitable for providing
necessary infrastructure resources. However, each cloud vendor provides different
APIs and tooling for management of their resources, so this still presents
portability challenges. Containers provide a portable, immutable image format,
and Kubernetes provides a higher-level, portable resource abstraction for
management of containers on underlying IaaW cloud resources invisibly, at least
from a developer point of view. Many cloud vendors, including the big three,
all provide managed Kubernetes services suitable for hosting multi-tenant
application and platform services.

Lastly, doing so is a valuable learning experience for me, and documenting my
Platform Engineering journey ensures that I fully understand that learning,
and allows me to share it with others interested in platform engineering.

I've named my example platform _Platykus_. Why?

- it has `plat` in the title, implying _Platform_
- it has `y` in the title, the Spanish word for the English word "and"
- it has `kus` in the title, loosely suggesting _Kubernetes_
- "Platform and Kubernetes" is an appropriate description
- it is pronounceable
- it is uniquely searchable on the web
- platypuses are cool

Yeah. It's a stretch.

Finally, all of this effort is intended to provide an example of how a custom,
productive Platform can be built and used, but not as a directly reusable
software component. Pick and choose what works for your needs, and if this
effort helps you get further down the road, I will be pleased to have helped.

## What is its scope?

I'm looking for a Platykus offering the following core features:

- multi-tenancy with application isolation enforced by RBAC
- on-demand, automatic scaling, up and down, of application and platform
  compute resources
- on-demand provisioning of network resources such as load balancers, DNS
  records, and TLS certificates
- on-demand provision of storage resources such as block storage volumes and
  object storage
- application and platform monitoring/observability stack
- application and platform secrets management services
- application and platform resource quotas and budgets
- application and platform usage/cost analysis and reporting

In addition, it would be nice to offer some other highly used services:

- key-value data services such as Redis
- relational databases such as PostgreSQL and MySQL
- streaming data services such as Kafka

I also want Platykus to be portable to public and private clouds, as well
as local Kubernetes clusters running on developer workstations and in build
pipelines.

## Where do we go from here?

All of my professional and personal work is currently running in AWS, so my
first effort will be towards creating Platykus on AWS and its EKS managed
Kubernetes cluster service.

My next steps will be the initial design and implementation of Platykus on EKS
with AWS as the hosting cloud vendor.

Thus begins Platykus. I hope you will join me for the journey and enjoy the ride!
