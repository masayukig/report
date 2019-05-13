Denver Summit OpenStack QA Summray for Forum and PTG
====================================================

I attended the OpenSt^H^H Infrastructure summit and OpenStack PTG. So, I
wanted to share about the Denver summit summary from QA perspective.

And I've also attached the summary mail[0] from Ghanshyam Mann who is
the OpenStack QA PTL. I think this is a good summary of the upstream QA
at the summit/PTG.

[0] http://lists.openstack.org/pipermail/openstack-discuss/2019-May/005872.html

Forum
-----

We gave the project update[1], onboarding[2] and QA tools/plugins[3] for
OpenStack QA.

At the "Users/Operators adoption of QA tools/plugins" session, some
interesting tools and ideas were shared like following[4].

 * Harbinger - High availability testing framework: https://etherpad.openstack.org/p/new-qa-project-harbinger
 * Python hardware module for bare metal detailed hardware inspection & anomaly detection
   https://github.com/redhat-cip/hardware
 * tobiko - Workload testing: https://opendev.org/x/tobiko/
 * Adding plugin feature for openstack-health dashboard: See the PTG
   discussion

[1] https://www.openstack.org/summit/denver-2019/summit-schedule/events/23703/openstack-qa-project-update
[2] https://www.openstack.org/summit/denver-2019/summit-schedule/events/23728/openstack-qa-project-onboarding
[3] https://www.openstack.org/summit/denver-2019/summit-schedule/events/23660/users-operators-adoption-of-qa-tools-plugins
[4] https://etherpad.openstack.org/p/Den-forum-qa-ops-user-feedback

PTG
---

We had good discussions and got some good improvement ideas about gate
stability and openstack-health dashboard, etc.[5] So, I've picked up
some interesting topics here.

[5] https://etherpad.openstack.org/p/qa-train-ptg

* Topic: new whitebox plugin for tempest
Currently, this tool does ssh into a VM and fetch the XML for further
verification etc. I think we'll be able to use this when this is
implemented in the future.
For the next step, a spec will be submitted and discussed.

* Topic: OpenStack-Health Improvement
Doug from AT&T has some improvement ideas for the openstack-health
dashboard such as "Test Grouping", "compare 2 runs", "Adding some other
reports to subunit2sql database". We think these can be done by
introducing plugin approach.

I think the plugin mechanism should be great for the our(SUSE)
development because we'd like to extend the openstack-health dashboard
internally sometimes, but we don't need it in the upstream development.
In this case, I think the plugin mechanism would work really well
because we can create plugins as we want.
