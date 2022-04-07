---
layout: post
title:  "Gaia-X Hackathon #3 from the SCS perspective"
category: tech
author:
  - "Felix Kronlage-Dammers"
  - "Kurt Garloff"
  - "Tim Beermann"
avatar:
  - "/assets/images/fkr.jpg"
  - "/assets/images/kgarloff.jpg"
  - "/assets/images/avatar-23technologies.jpg"
---

## Gaia-X Hackathon #3

On March 28th and 29th the [third Gaia-X Hackathon](https://hackathon.minimal-gaia-x.eu) took place. 
Aside from providing clusters for the development sessions the SCS project took actively part in one
of the streams: ACME. In the ACME track we covered three overall topics:

- Confidential Computing based on Intel SGX
- Gaia-x Selfdescriptions
- Blackbox Monitoring via Rally

## Confidential Computing

## Gaia-X Selfdescriptions

## Rally Hackfest

One of the tools that exists in the SCS ecosystem is the
[OpenStack Health Monitor](https://github.com/SovereignCloudStack/openstack-health-monitor) which is a 
gigantic shell script that Kurt developed and which monitors OpenStack clouds through the api by 
creating certain assets on the cloud and tearing them down again. While the Shellscript does its job
really well it is fairly hard to maintain for anyone *but* Kurt. As such we've already evaluated
how to replace it during the R2 cycle. 
For the hackathon we decided in the SIG Monitoring that we should spend two days hacking on
[rally](https://opendev.org/openstack/rally) to see whether rally is the proper tool to be the
successor for the shell script.
While we got good test cases working, we're still not convinced that rally is the way to go. Rally
brings a lot of benefits to the table, such as metrics for all test cases run as well as a ton of
pre-defined tests that can easily be adopted. However due to the nature of rally each test case
is run on a clean slate and it is everything but trivial to build testcases that build on top of
each other.
We documented our progress in [a repo](https://github.com/sovereignCloudStack/rally-foo) to make sure,
we don't run into the same pitfalls each and every time.

Aside from the technical work on rally I really enjoyed the nice atmosphere of two days of hacking
with Andre, Ralf and Mathias and finally have a proper `.gitconfig` - thanks to Ralf!


