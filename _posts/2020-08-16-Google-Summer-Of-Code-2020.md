---
layout: post
title: Google Summer Of Code 2020 Report
---
Greetings everyone, I'm pleased to share my GSoC 2020 report with CNCF. During the program, I contributed to the <a href="https://github.com/prometheus/test-infra">prometheus/test-infra</a> and <a href="https://prombench.prometheus.io">prombench.prometheus.io</a>. My work and contributions are available for viewing, and I plan to continue my contributions beyond the GSoC period.

I would like to express my heartfelt gratitude to my mentor for their unwavering guidance and support throughout this amazing journey.


### Links:
* My Evaluations: 
   - <a href="https://github.com/imrajdas/gsoc-2020-cncf/blob/master/evaluations/eval1.png">First Evaluation</a>
   - <a href="https://github.com/imrajdas/gsoc-2020-cncf/blob/master/evaluations/eval2.png">Second Evaluation</a>
   - <a href="https://github.com/imrajdas/gsoc-2020-cncf/blob/master/evaluations/eval1.png">Final Evaluation</a>
   
* GSoC Project URL <br/>
  https://summerofcode.withgoogle.com/archive/2020/projects/4546170073907200/

* CNCF Blog Post <br/>
  https://www.cncf.io/blog/2020/09/17/16-cncf-interns-graduate-from-summer-of-code-gsoc-2020/

* Certificate <br/>
  <a href="https://github.com/imrajdas/gsoc-2020-cncf/blob/master/evaluations/Completion_2020_0234.pdf">Completion_2020_0234.pdf</a>

* Completion Letter <br/>
   <a href="https://github.com/imrajdas/gsoc-2020-cncf/blob/master/evaluations/Completion_2020_0234.pdf">GSoC 2020 Certificate GSoC20200234.pdf</a>
 
### What did I solve?
  1. Develop prometheus benchmark infrastructure with KIND 
  
	 <b>Description:</b> At present, the deployment of prombench on GKE is quite resource-intensive and time-consuming. To address this issue, we have found a solution that involves utilizing KIND for local/virtual machine deployment of prombench. This approach is considerably faster than deploying on GKE, and provides a convenient way to run prombench locally.
	    * Issue(s): <a href="https://github.com/prometheus/test-infra/issues/333" target="_blank">prometheus/test-infra/issue#333</a> 
        * PR(s): <a href="https://github.com/prometheus/test-infra/pull/390" target="_blank">prometheus/test-infra/pull#390</a>

  2. Refactor prombench infrastructure and manifest deployable for KIND and EKS.
        
     <b>Description:</b> Refactor the infrastructure and deployment manifests of prombench to make it more versatile and suitable for deployment on both EKS and KIND. Currently, prombench is tightly coupled with GKE, which limits its deployment options. By refactoring the infrastructure and manifests, we aim to make it more generic and deployable on a wider range of environments.
	    * Issue(s): <a href="https://github.com/prometheus/test-infra/issues/371" target="_blank">prometheus/test-infra/issue#371</a>
	    * PR(s): 
	      * <a href="https://github.com/prometheus/test-infra/pull/412" target="_blank">prometheus/test-infra/pull#412</a>
	      * <a href="https://github.com/prometheus/test-infra/pull/406" target="_blank">prometheus/test-infra/pull#406</a>
	      * <a href="https://github.com/prometheus/test-infra/pull/391" target="_blank">prometheus/test-infra/pull#391</a>
	      * <a href="https://github.com/prometheus/test-infra/pull/372" target="_blank">prometheus/test-infra/pull#371</a>
	      * <a href="https://github.com/prometheus/test-infra/pull/369" target="_blank">prometheus/test-infra/pull#369</a>
	

  3. Fix Node Exporter to show the metrics related to SSD
  
     <b>Description:</b> To address the issue of Node Exporter not displaying metrics related to SSD, an effective solution is to upgrade the Node Exporter to its latest version and include a new flag in the exporter's configuration called “--path.rootfs”. This flag enables the exporter to collect metrics specifically related to the root file system, which includes the SSD. Implementing these steps enhances the visibility and provides valuable insights into the system's performance.

     * Issue(s): 
        * <a href="https://github.com/prometheus/test-infra/issues/159" target="_blank">prometheus/test-infra/issue#159</a>
        * <a href="https://github.com/prometheus/test-infra/issues/328" target="_blank">prometheus/test-infra/issue#328</a>

	 * PR(s): <a href="https://github.com/prometheus/test-infra/pull/408" target="_blank">prometheus/test-infra/pull#408</a>

  4. Add descriptions to the Grafana dashboard regarding prombench
  
	 <b>Description:</b> In the current Grafana dashboard, there are no descriptions available for prombench, which may pose difficulties for new users in comprehending its functionality. To address this issue, it is necessary to add descriptive text and explanations about prombench to the Grafana dashboard. This will enable new users to better understand the purpose and functionality of prombench and help them effectively navigate the Grafana dashboard.

	 * Issue(s): 
	    * <a href="https://github.com/prometheus/test-infra/issues/328" target="_blank">prometheus/test-infra/issue#328</a>
	    * <a href="https://github.com/prometheus/test-infra/issues/305" target="_blank">prometheus/test-infra/issue#305</a>
	 * Doc(s): <a href="https://docs.google.com/document/d/1FKLUkCcaTgC72Dh-Kz66228PykCwG4zy2Tw7zD_491k">Descriptions for Prombench Graphana Dashboard</a>
	 * PR(s): <a href="https://github.com/prometheus/test-infra/pull/428" target="_blank">prometheus/test-infra/pull#428</a>
	
  5. Increase Retention period of loki to 90 days

     <b>Note:</b> Although not an immediate priority, it has been identified that increasing the retention period of loki to 90 days would be beneficial. While a pull request has been submitted to address this issue, it will be completed after the GSoC period.

     * Issue(s): 
        * <a href="https://github.com/prometheus/test-infra/issues/322" target="_blank">prometheus/test-infra/issue#322</a>
        * <a href="https://github.com/prometheus/test-infra/issues/328" target="_blank">prometheus/test-infra/issue#328</a>
     * PR(s): <a href="https://github.com/prometheus/test-infra/pull/423" target="_blank">prometheus/test-infra/pull#423</a>

## Extra fixes
1. PR: <a href="https://github.com/prometheus/test-infra/pull/432">prometheus/test-infra/pull#432</a>
2. PR: <a href="https://github.com/prometheus/test-infra/pull/433">prometheus/test-infra/pull#433</a>

### What did I learn?
* During my experience, I have developed a comprehensive understanding of the Prometheus monitoring system and its architecture. I have also gained practical experience working with prombench, an important tool used for testing Prometheus.

* I have learned the significance of code maintainability, organization, and documentation. I have gained insights into writing clean and concise code, and creating comprehensive documentation to help others understand and use the codebase.

* I have acquired knowledge of KIND architecture and how it can be used to deploy Kubernetes clusters for testing and development purposes. I have also gained experience with the Go packages used in KIND, which are used to create and manage Kubernetes clusters in a local or cloud environment.

* I have learned that patience is an essential quality during the review process for pull requests. It is important to take the time to carefully review and address comments and suggestions from reviewers, as this can ultimately improve the quality and maintainability of the codebase.

---