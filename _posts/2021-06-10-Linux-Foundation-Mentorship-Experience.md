---
layout: post
title: My experience with Linux Foundation Mentorship Program
---

Hello everyone 👋, I’m Raj Babu Das, working as a Software Engineer at MayaData Inc. and a Core-Contributor to the LitmusChaos project. I have successfully graduated from the Linux Foundation Mentorship program with Keptn. In this blog, I’m going to share my experience as a mentee.

<img src="https://github.com/rajdas98/rajdas98/raw/main/images/lfx-1.png">

Linux Foundation Mentorship program is an initiative by the Linux Foundation to help developers with the necessary skills and encourage them to participate. This program held at the start of each quarter and taken part by many open source organizations like CNCF, OpenJS Foundation, etc. Any student or working professional can take part as a mentee where they have to work for a term of 3 months.

<img src="https://github.com/rajdas98/rajdas98/raw/main/images/lfx-2.png"/>

I heard about this program while I was working as a GSoC student last year. Since then, I continuously followed all the updates for the program. As an active contributor to other CNCF projects, I planned to participate only in the CNCF projects. Last quarter, I applied for this program but, I didn’t get through it. I thought to participate again this year for a CNCF sandbox project called Keptn, and finally, my application got accepted this time.
To apply, follow this link- https://mentorship.lfx.linuxfoundation.org/#projects

### Keptn Project
Keptn is a control-plane for DevOps automation of cloud-native applications. In a nutshell, Keptn provides a Declarative Approach to Automate Delivery & Operations Use Cases:
* Automated SLO-based Quality Gates
* Automated Performance & Chaos Testing
* Automated Multi-Stage and Multi-Target Delivery
* Automated Auto-Remediation

<img src="https://github.com/rajdas98/rajdas98/raw/main/images/lfx-3.png"/>

I heard about the Keptn project from my colleagues at MayaData where we have integrated Keptn with another CNCF project called LitmusChaos. When the keptn project announced their participation for this issue- “Improve Prometheus integration and exposure of Prometheus metrics”, I got excited because I know the core skills required for it i.e. Golang, Kubernetes and Prometheus. Immediately, I started learning about this project, and after a few weeks, I finally got selected for this program.
Keptn have written the documentation and tutorials so nicely that any naïve user can easily understand it. I didn’t face any struggle while learning it.

### My Experience
I really enjoyed working with my mentors Jürgen Etzlstorfer, Johannes Bräuer and Florian Bacher. We used to have weekly sync up calls where we discussed the project status and blockers.
My primary task is to rewrite the keptn’s Prometheus service to make it independent of the Prometheus installation. I completed this task within a month, and I started working on an additional issue that is Adding keptn’s SLI service functionalities into keptn Prometheus service, which itself a big and complicated task for me. Finally, I was able to complete my remaining tasks within the mentorship period, and at last, I did the refactor of the Keptn’s documentation and tutorial regarding the code change.
Major Pull Requests
https://github.com/keptn-contrib/prometheus-service/pull/117
https://github.com/keptn-contrib/prometheus-service/pull/132
A few more PRs got merged for docs, tutorials, and bug fixes, along with the above pull requests.

### Community
After my PR(s) got merged. I got a chance to present my work to the Keptn community. You can find the demo here- Keptn Community & Developer Meeting — June 10th, 2021
<img src="https://github.com/rajdas98/rajdas98/raw/main/images/lfx-4.png"/>

### Conclusion
I am glad that I got this opportunity to work with such a great Open Source project. Open source projects are the backbone of the FOSS culture, which promotes free and open-source software, encourages sharing and collaboration.
LFX Mentorship is a great place for a student and a working professional to work on a project that motivates and exponentially increases the ability of a developer to work in a large team. I would strongly recommend it to anyone who has a passion for the open-source culture to apply for LFX Mentorship whenever they announced it.


I want to thank my mentors Jürgen Etzlstorfer, Johannes Bräuer, Florian Bacher for the guidance provided during this program.

-x-