---
title: "Why Terraform is not the best tool for database lifecycle management (under some circumstances)"
date: 2021-06-10T21:09:08-05:00
draft: true
---

Terraform is the most commonly used IaaC tool. While it is very useful for managing lifecycles for resources, it fails at managing databases at scale. Now, what is unique about databases versus resources like VMs and load balancers? Databases are stateful. While a VM can be replaced by another VM behind a load-balancer, a database change generally needs careful coordination to minimize downtime.

Large companies often have hundreds of databases, hence it becomes necessary to put Terraform behind some sort of a workflow. This can be a Jenkins job, or a Github action or Atlantis.

> Disclaimer: if you (the reader) is happy with using Terraform for manageing your RDS databases, feel free. Everyone's use-case is different.

Here is the central claim I am presenting: Terraform (and other IaaC tools) are a bad fit for managing database lifecycle if there is need for minimizing downtime and automating Terraform runs at scale.

### An example: RDS major version upgrade

Test

### So, what works then?

Test
