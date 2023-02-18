---
layout: post
title: My experience with Linux Foundation Mentorship Program
---
Greetings, I'm Raj Das, working as a Software Engineer at MayaData Inc. and also serve as a Core-Contributor to the <a href="https://litmuschaos.io/">LitmusChaos project</a>. Recently, I successfully graduated from the Linux Foundation Mentorship program with <a href="https://keptn.sh/">Keptn</a>. In this blog post, I intend to share my experiences as a mentee.


<img src="https://github.com/imrajdas/imrajdas/raw/main/images/lfx-1.png">

Linux Foundation Mentorship program is an initiative by the Linux Foundation to help developers with the necessary skills and encourage them to participate. This program held at the start of each quarter and taken part by many open source organizations like CNCF, OpenJS Foundation, etc. Any student or working professional can take part as a mentee where they have to work for a term of 3 months.

<img src="https://github.com/imrajdas/imrajdas/raw/main/images/lfx-2.png"/>
I became aware of this program during my tenure as a GSoC student last year and have been keeping up with its latest updates ever since. As an active contributor to several CNCF projects, I decided to participate exclusively in the CNCF projects.

Although I applied for the program last quarter, I was unfortunately not selected. Undeterred, I submitted a fresh application this year, this time for a CNCF sandbox project known as Keptn, and am pleased to announce that my application was accepted.


>To apply, follow this link- https://mentorship.lfx.linuxfoundation.org/#projects

### Keptn Project
Keptn is a control-plane for DevOps automation of cloud-native applications. In a nutshell, Keptn provides a Declarative Approach to Automate Delivery & Operations Use Cases:
* Automated SLO-based Quality Gates
* Automated Performance & Chaos Testing
* Automated Multi-Stage and Multi-Target Delivery
* Automated Auto-Remediation

<img src="https://github.com/imrajdas/imrajdas/raw/main/images/lfx-3.png"/>

I heard about the Keptn project from my colleagues at MayaData where we have integrated Keptn with another CNCF project called LitmusChaos. When the keptn announced their participation for this issue- <a href="https://mentorship.lfx.linuxfoundation.org/project/54adaade-8537-4150-b4ea-988454615ed7">Improve Prometheus integration and exposure of Prometheus metrics</a>, I became thrilled as I possessed the necessary core skills, including Golang, Kubernetes, and Prometheus. Following the announcement, I spent several weeks researching the project and was ultimately accepted into the program. I found that Keptn's documentation and tutorials were written in an easily understandable manner, making the learning process seamless and without obstacles.

### My Experience
I had a productive experience collaborating with my mentors Jürgen Etzlstorfer, Johannes Bräuer, and Florian Bacher during the mentorship program. We held weekly sync-up calls to discuss the project's progress and any obstacles encountered. My primary objective was to rewrite Keptn's Prometheus service to eliminate its dependence on the Prometheus installation. I accomplished this task within a month and proceeded to tackle another complex task of adding keptn’s SLI service functionalities into keptn Prometheus service.

Throughout the mentorship program, I was able to complete my remaining tasks before the program concluded. Toward the end of the program, I refactored the documentation and tutorial regarding the code change in Keptn.

>Major Pull Requests
* https://github.com/keptn-contrib/prometheus-service/pull/117
* https://github.com/keptn-contrib/prometheus-service/pull/132

> A few more PRs got merged for docs, tutorials, and bug fixes, along with the above pull requests.

### Community
Upon the successful merging of my pull request(s), I was presented with the opportunity to showcase my work to the Keptn community. The demo of my contributions can be found on the Keptn Community & Developer Meeting — June 10th, 2021

<img src="https://github.com/imrajdas/imrajdas/raw/main/images/lfx-4.png"/>

### Conclusion

I am grateful to have had the opportunity to work with a remarkable open-source project and contribute to the FOSS culture. Participating in an open-source project not only benefits the community but also allows developers to gain valuable experience working in a collaborative environment.

The LFX Mentorship program is an excellent platform for students and professionals to work on meaningful projects that foster personal and professional growth. Working on the Keptn project through the LFX Mentorship program enabled me to develop my skills in Go, Kubernetes, and Prometheus while contributing to a real-world use case.

I strongly recommend the LFX Mentorship program to anyone who is passionate about the open-source culture and wants to contribute to a project with a meaningful impact. Finally, I would like to express my sincere gratitude to my mentors, Jürgen Etzlstorfer, Johannes Bräuer, and Florian Bacher, for their invaluable guidance throughout the program.
-x-