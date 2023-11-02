# 1	Understand infrastructure as code (IaC) concepts

<details><summary><h2>1a	Explain what IaC is</h2></summary>
  HashiCorp Terraform is an infrastructure as code tool that lets you define both cloud and on-prem resources in human-readable configuration files that you can version, reuse, and share. You can then use a consistent workflow to provision and manage all of your infrastructure throughout its lifecycle. Terraform can manage low-level components like compute, storage, and networking resources, as well as high-level components like DNS entries and SaaS features.

  How does Terraform work?
Terraform creates and manages resources on cloud platforms and other services through their application programming interfaces (APIs). Providers enable Terraform to work with virtually any platform or service with an accessible API.
Terraform creates and manages resources on cloud platforms and other services through their application programming interfaces (APIs). Providers enable Terraform to work with virtually any platform or service with an accessible API.
<br>
Terraform creates and manages cloud platforms and services through their APIs

HashiCorp and the Terraform community have already written thousands of providers to manage many different types of resources and services. You can find all publicly available providers on the Terraform Registry, including Amazon Web Services (AWS), Azure, Google Cloud Platform (GCP), Kubernetes, Helm, GitHub, Splunk, DataDog, and many more.

The core Terraform workflow consists of three stages:

Write: You define resources, which may be across multiple cloud providers and services. For example, you might create a configuration to deploy an application on virtual machines in a Virtual Private Cloud (VPC) network with security groups and a load balancer.
Plan: Terraform creates an execution plan describing the infrastructure it will create, update, or destroy based on the existing infrastructure and your configuration.
Apply: On approval, Terraform performs the proposed operations in the correct order, respecting any resource dependencies. For example, if you update the properties of a VPC and change the number of virtual machines in that VPC, Terraform will recreate the VPC before scaling the virtual machines.
Why Terraform?
HashiCorp co-founder and CTO Armon Dadgar explains how Terraform solves infrastructure challenges.


Manage any infrastructure
Find providers for many of the platforms and services you already use in the Terraform Registry. You can also write your own. Terraform takes an immutable approach to infrastructure, reducing the complexity of upgrading or modifying your services and infrastructure.

Track your infrastructure
Terraform generates a plan and prompts you for your approval before modifying your infrastructure. It also keeps track of your real infrastructure in a state file, which acts as a source of truth for your environment. Terraform uses the state file to determine the changes to make to your infrastructure so that it will match your configuration.

Automate changes
Terraform configuration files are declarative, meaning that they describe the end state of your infrastructure. You do not need to write step-by-step instructions to create resources because Terraform handles the underlying logic. Terraform builds a resource graph to determine resource dependencies and creates or modifies non-dependent resources in parallel. This allows Terraform to provision resources efficiently.

Standardize configurations
Terraform supports reusable configuration components called modules that define configurable collections of infrastructure, saving time and encouraging best practices. You can use publicly available modules from the Terraform Registry, or write your own.

Collaborate
Since your configuration is written in a file, you can commit it to a Version Control System (VCS) and use Terraform Cloud to efficiently manage Terraform workflows across teams. Terraform Cloud runs Terraform in a consistent, reliable environment and provides secure access to shared state and secret data, role-based access controls, a private registry for sharing both modules and providers, and more.


</details>
<details><summary><h2>1b	Describe advantages of IaC patterns</h2></summary>
  Infrastructure as Code in a Private or Public Cloud
JAN 23 2020
LARRY EICHENBAUM, AHMED BELGANA
As technology advances, our tools change. But because most people resist change it often takes some type of failure—a system outage, a failed disaster recovery event, etc.—to get us to change our governance practices.

For example, as companies move their operations to the cloud they tend to manage their cloud infrastructure the same way they managed their on-premise physical hardware, by logging into their virtual infrastructure’s web interface, or directly onto a system and applying changes via GUI or CLI. These users haven’t adopted the use of infrastructure as code (IaC) through the use of tools like HashiCorp Terraform.

What is IaC? It is infrastructure (CPUs, memory, disk, firewalls, etc.) defined as code within definition files. But why change how we define and build infrastructure?

Virtual compute enabled us to build and apply configuration changes to infrastructure via software commands. While these commands were often scripted, they were still hard for humans to read. More modern tools accepted code that was both human and machine readable, and provided additional benefits. They simplified code testing, could apply and track the changes between iterations, and most importantly they enabled teams to reuse components (e.g. modules) of code across different projects. It’s no wonder that IaC has developed such a significant following and adoption.



IaC and the Infrastructure Lifecycle
So how does IaC fit into the infrastructure lifecycle? IaC can be applied throughout the lifecycle, both on the initial build, as well as throughout the life of the infrastructure. Commonly, these are referred to as Day 0 and Day 1 activities. “Day 0” code provisions and configures your initial infrastructure.

If your infrastructure never changes after the initial build (no OS updates, no patches, no app configurations, etc.) then you may not need tools that support subsequent updates, changes, and expansions. “Day 1” refers to OS and application configurations you apply after you’ve initially built your infrastructure.

IaC makes it easy to provision and apply infrastructure configurations, saving time. It standardizes workflows across different infrastructure providers (e.g., VMware, AWS, Azure, GCP, etc.) by using a common syntax across all of them.

IaC makes it easy to understand the intent of infrastructure changes, because it can span multiple files, allowing human operators to organize the code based on the intent. For example, an operator could create different files to define different infrastructure components, or separate variables definitions from execution blocks without affecting the execution.

Here is an example of code that the IaC tool Terraform would use to provision an Amazon VPC. Notice that the code is both human and machine readable.

resource "aws_vpc" "default" {
  cidr_block = "10.0.0.0/16"
}
Tools like Terraform often include libraries of providers and modules to make it easy to write the code to provision and apply configurations. With Terraform, especially when the need is Day 0 only, it is common to apply initial configurations like the ones below which install and start a web server:

provisioner "remote-exec" {
  inline = [
    "sudo apt-get -y update",
    "sudo apt-get -y install nginx",
    "sudo service nginx start"
    ]
}
If it is necessary to apply Day 1 through Day N configurations, the code might leverage a tool like Chef, Ansible, Docker, etc.

provider "chef" {
  server_url = "https://api.chef.io/organization/example"
  run_list = [ "recipe[example]" ]
}
You can find a more complex example of Terraform IaC that provisions a two-tier application in this Hashicorp Learn tutorial: Deploy Federated Multi-Cloud Kubernetes Clusters.

IaC Makes Infrastructure More Reliable
IaC makes changes idempotent, consistent, repeatable, and predictable. Without IaC, scaling up infrastructure to meet increased demand may require an operator to remotely connect to each machine and then manually provision and configure many servers by executing a series of commands/scripts. They might open multiple sessions and move between screens, which often results in skipped steps or slight variations between how work is completed, necessitating rollbacks. Perhaps a command was run incorrectly on one instance and reverted before being re-run correctly.

These process inconsistencies can result in slight differences between servers that compound over time and could impact their performance, usability, or security. If a large team is applying changes, the risks increase because individuals don’t always follow the same instructions identically.

With IaC, we can test the code and review the results before the code is applied to our target environments. Should a result not align to our expectations, we iterate on the code until the results pass our tests and align to our expectations. Following this pattern allows for the outcome to be predicted before the code is applied to a production environment. Once ready for use, we can then apply that code via automation, at scale, ensuring consistency and repeatability in how it is applied.

Since code is checked into version control systems such as GitHub, GitLab, BitBucket, etc., it is possible to review how the infrastructure evolves over time. The idempotent characteristic provided by IaC tools ensures that, even if the same code is applied multiple times, the result remains the same.

IaC Makes Infrastructure More Manageable
Leveraging HashiCorp Terraform IaC provides benefits that enable mutation, when necessary, via code. Consider an environment has been provisioned that contains a couple servers and a load balancer. To address increased load, additional servers are needed. The IaC can be revised, with minimal changes, to bring new servers online using the previously defined configuration.

During execution, Terraform will examine the state of the currently running infrastructure, determine what differences exist between the current state and the revised desired state, and indicate the necessary changes that must be applied. When approved to proceed, only the necessary changes will be applied, leaving existing, valid infrastructure untouched.

IaC Makes Sense
Successfully managing the lifecycle of infrastructure is hard, and the impact of poor management decisions can be significant, ranging from financial and reputational losses to even loss of life when considering government and military dependencies on infrastructure. Adopting the use of an IaC tool such as HashiCorp Terraform, in conjunction with related and established tools, processes, and workflows, is a necessary step in mitigating these risks.

To learn more about Terraform and HashiCorp’s other infrastructure tools, visit the Terraform documentation and check out our learning tracks on HashiCorp Learn.
</details>

# 2	Understand the purpose of Terraform (vs other IaC)
<details><summary>2a	Explain multi-cloud and provider-agnostic benefits</summary>
  Use Cases
HashiCorp Terraform is an infrastructure as code tool that lets you define infrastructure resources in human-readable configuration files that you can version, reuse, and share. You can then use a consistent workflow to safely and efficiently provision and manage your infrastructure throughout its lifecycle.

This page describes popular Terraform use cases and provides related resources that you can use to create Terraform configurations and workflows.

Multi-Cloud Deployment
Provisioning infrastructure across multiple clouds increases fault-tolerance, allowing for more graceful recovery from cloud provider outages. However, multi-cloud deployments add complexity because each provider has its own interfaces, tools, and workflows. Terraform lets you use the same workflow to manage multiple providers and handle cross-cloud dependencies. This simplifies management and orchestration for large-scale, multi-cloud infrastructures.

Resources
Try our Deploy Federated Multi-Cloud Kubernetes Clusters tutorial to provision Kubernetes clusters in both Azure and AWS environments, configure Consul federation with mesh gateways across the two clusters, and deploy microservices across the two clusters to verify federation.
Browse the Terraform Registry to find thousands of publicly available providers.
Application Infrastructure Deployment, Scaling, and Monitoring Tools
You can use Terraform to efficiently deploy, release, scale, and monitor infrastructure for multi-tier applications. N-tier application architecture lets you scale application components independently and provides a separation of concerns. An application could consist of a pool of web servers that use a database tier, with additional tiers for API servers, caching servers, and routing meshes. Terraform allows you to manage the resources in each tier together, and automatically handles dependencies between tiers. For example, Terraform will deploy a database tier before provisioning the web servers that depend on it.

Resources
Try our Automate Monitoring with the Terraform Datadog Provider tutorial to deploy a demo Nginx application to a Kubernetes cluster with Helm and install the Datadog agent across the cluster. The Datadog agent reports the cluster health back to your Datadog dashboard.
Try our Use Application Load Balancers for Blue-Green and Canary Deployments tutorial. You will provision the blue and green environments, add feature toggles to your Terraform configuration to define a list of potential deployment strategies, conduct a canary test, and incrementally promote your green environment.
Self-Service Clusters
At a large organization, your centralized operations team may get many repetitive infrastructure requests. You can use Terraform to build a "self-serve" infrastructure model that lets product teams manage their own infrastructure independently. You can create and use Terraform modules that codify the standards for deploying and managing services in your organization, allowing teams to efficiently deploy services in compliance with your organization’s practices. Terraform Cloud can also integrate with ticketing systems like ServiceNow to automatically generate new infrastructure requests.

Resources
Try the Use Modules from the Registry tutorial to get started using public modules in your Terraform configuration. Try the Build and Use a Local Module tutorial to create a module to manage AWS S3 buckets.
Follow these ServiceNow Service Catalog Integration Setup Instructions to connect ServiceNow to Terraform Cloud.
Policy Compliance and Management
Terraform can help you enforce policies on the types of resources teams can provision and use. Ticket-based review processes are a bottleneck that can slow down development. Instead, you can use Sentinel, a policy-as-code framework, to automatically enforce compliance and governance policies before Terraform makes infrastructure changes. Sentinel policies are available in Terraform Enterprise and Terraform Cloud.

Resources
Try the Control Costs with Policies tutorial to estimate the cost of infrastructure changes and define policy to limit it.

The Sentinel documentation provides more in-depth information and a list of example policies that you can adapt for your use cases.

PaaS Application Setup
Platform as a Service (PaaS) vendors like Heroku allow you to create web applications and attach add-ons, such as databases or email providers. Heroku can elastically scale the number of dynos or workers, but most non-trivial applications need many add-ons and external services. You can use Terraform to codify the setup required for a Heroku application, configure a DNSimple to set a CNAME, and set up Cloudflare as a Content Delivery Network (CDN) for the app. Terraform can quickly and consistently do all of this without a web interface.

Resources
Try the Deploy, Manage, and Scale an Application on Heroku tutorial to manage an application’s lifecycle with Terraform.

Software Defined Networking
Terraform can interact with Software Defined Networks (SDNs) to automatically configure the network according to the needs of the applications running in it. This lets you move from a ticket-based workflow to an automated one, reducing deployment times.

For example, when a service registers with HashiCorp Consul, Consul-Terraform-Sync can automatically generate Terraform configuration to expose appropriate ports and adjust network settings for any SDN that has an associated Terraform provider. Network Infrastructure Automation (NIA) allows you to safely approve the changes that your applications require without having to manually translate tickets from developers into the changes you think their applications need.

Resources
Try the Network Infrastructure Automation with Consul-Terraform-Sync Intro tutorial to install Consul-Terraform-Sync on a node. You will then configure it to communicate with a Consul datacenter, react to service changes, and execute an example task.
Try the Consul-Terraform-Sync and Terraform Enterprise/Cloud Integration tutorial to configure Consul-Terraform-Sync to interact with Terraform Enterprise and Terraform Cloud.
Kubernetes
Kubernetes is an open-source workload scheduler for containerized applications. Terraform lets you both deploy a Kubernetes cluster and manage its resources (e.g., pods, deployments, services, etc.). You can also use the Kubernetes Operator for Terraform to manage cloud and on-prem infrastructure through a Kubernetes Custom Resource Definition (CRD) and Terraform Cloud.

Resources
Try the Manage Kubernetes Resources via Terraform tutorial. You will use Terraform to schedule and expose a NGINX deployment on a Kubernetes cluster.
Try the Deploy Infrastructure with the Terraform Cloud Operator for Kubernetes tutorial. You will configure and deploy the Operator to a Kubernetes cluster and use it to create a Terraform Cloud workspace and provision a message queue for an example application.
Parallel Environments
You may have staging or QA environments that you use to test new applications before releasing them in production. As the production environment grows larger and more complex, it can be increasingly difficult to maintain an up-to-date environment for each stage of the development process. Terraform lets you rapidly spin up and decommission infrastructure for development, test, QA, and production. Using Terraform to create disposable environments as needed is more cost-efficient than maintaining each one indefinitely.

Software Demos
You can use Terraform to create, provision, and bootstrap a demo on various cloud providers. This lets end users easily try the software on their own infrastructure and even enables them to adjust parameters like cluster size to more rigorously test tools at any scale.
</details>
<details><summary>2b	Explain the benefits of state</summary>
  Purpose of Terraform State
State is a necessary requirement for Terraform to function. It is often asked if it is possible for Terraform to work without state, or for Terraform to not use state and just inspect cloud resources on every run. This page will help explain why Terraform state is required.

As you'll see from the reasons below, state is required. And in the scenarios where Terraform may be able to get away without state, doing so would require shifting massive amounts of complexity from one place (state) to another place (the replacement concept).

Mapping to the Real World
Terraform requires some sort of database to map Terraform config to the real world. When you have a resource resource "aws_instance" "foo" in your configuration, Terraform uses this map to know that instance i-abcd1234 is represented by that resource.

For some providers like AWS, Terraform could theoretically use something like AWS tags. Early prototypes of Terraform actually had no state files and used this method. However, we quickly ran into problems. The first major issue was a simple one: not all resources support tags, and not all cloud providers support tags.

Therefore, for mapping configuration to resources in the real world, Terraform uses its own state structure.

Terraform expects that each remote object is bound to only one resource instance, which is normally guaranteed by Terraform being responsible for creating the objects and recording their identities in the state. If you instead import objects that were created outside of Terraform, you'll need to check yourself that each distinct object is imported to only one resource instance.

If one remote object is bound to two or more resource instances then Terraform may take unexpected actions against those objects, because the mapping from configuration to the remote object state has become ambiguous.

Metadata
Alongside the mappings between resources and remote objects, Terraform must also track metadata such as resource dependencies.

Terraform typically uses the configuration to determine dependency order. However, when you delete a resource from a Terraform configuration, Terraform must know how to delete that resource. Terraform can see that a mapping exists for a resource not in your configuration and plan to destroy. However, since the configuration no longer exists, the order cannot be determined from the configuration alone.

To ensure correct operation, Terraform retains a copy of the most recent set of dependencies within the state. Now Terraform can still determine the correct order for destruction from the state when you delete one or more items from the configuration.

One way to avoid this would be for Terraform to know a required ordering between resource types. For example, Terraform could know that servers must be deleted before the subnets they are a part of. The complexity for this approach quickly explodes, however: in addition to Terraform having to understand the ordering semantics of every resource for every cloud, Terraform must also understand the ordering across providers.

Terraform also stores other metadata for similar reasons, such as a pointer to the provider configuration that was most recently used with the resource in situations where multiple aliased providers are present.

Performance
In addition to basic mapping, Terraform stores a cache of the attribute values for all resources in the state. This is the most optional feature of Terraform state and is done only as a performance improvement.

When running a terraform plan, Terraform must know the current state of resources in order to effectively determine the changes that it needs to make to reach your desired configuration.

For small infrastructures, Terraform can query your providers and sync the latest attributes from all your resources. This is the default behavior of Terraform: for every plan and apply, Terraform will sync all resources in your state.

For larger infrastructures, querying every resource is too slow. Many cloud providers do not provide APIs to query multiple resources at once, and the round trip time for each resource is hundreds of milliseconds. On top of this, cloud providers almost always have API rate limiting so Terraform can only request a certain number of resources in a period of time. Larger users of Terraform make heavy use of the -refresh=false flag as well as the -target flag in order to work around this. In these scenarios, the cached state is treated as the record of truth.

Syncing
In the default configuration, Terraform stores the state in a file in the current working directory where Terraform was run. This is okay for getting started, but when using Terraform in a team it is important for everyone to be working with the same state so that operations will be applied to the same remote objects.

Remote state is the recommended solution to this problem. With a fully-featured state backend, Terraform can use remote locking as a measure to avoid two or more different users accidentally running Terraform at the same time, and thus ensure that each Terraform run begins with the most recent updated state.
</details>

# 3	Understand Terraform basics
<details><summary>3a	Install and version Terraform providers</summary>
</details>
<details><summary>3b	Describe plugin-based architecture</summary>
</details>
<details><summary>3c	Write Terraform configuration using multiple providers</summary>
</details>
<details><summary>3d	Describe how Terraform finds and fetches providers</summary>
</details>

# 4	Use Terraform outside of core workflow
<details><summary>4a	Describe when to use terraform import to import existing infrastructure into your Terraform state</summary>
</details>
<details><summary>4b	Use terraform state to view Terraform state</summary>
</details>
<details><summary>4c	Describe when to enable verbose logging and what the outcome/value is</summary>
</details>

# 5	Interact with Terraform modules
<details><summary>5a	Contrast and use different module source options including the public Terraform Module Registry</summary>
</details>
<details><summary>5b	Interact with module inputs and outputs</summary>
</details>
<details><summary>5c	Describe variable scope within modules/child modules</summary>
</details>
<details><summary>5d	Set module version</summary>
</details>

# 6	Use the core Terraform workflow
<details><summary>6a	Describe Terraform workflow ( Write -> Plan -> Create )</summary>
</details>
<details><summary>6b	Initialize a Terraform working directory (terraform init)</summary>
</details>
<details><summary>6c	Validate a Terraform configuration (terraform validate)</summary>
</details>
<details><summary>6d	Generate and review an execution plan for Terraform (terraform plan)</summary>
</details>
<details><summary>6e	Execute changes to infrastructure with Terraform (terraform apply)</summary>
</details>
<details><summary>6f	Destroy Terraform managed infrastructure (terraform destroy)</summary>
</details>
<details><summary>6g	Apply formatting and style adjustments to a configuration (terraform fmt)</summary>
</details>

# 7	Implement and maintain state
<details><summary>7a	Describe default local backend</summary>
</details>
<details><summary>7b	Describe state locking</summary>
</details>
<details><summary>7c	Handle backend and cloud integration authentication methods</summary>
</details>
<details><summary>7d	Differentiate remote state back end options</summary>
</details>
<details><summary>7e	Manage resource drift and Terraform state</summary>
</details>
<details><summary>7f	Describe backend block and cloud integration in configuration</summary>
</details>
<details><summary>7g	Understand secret management in state files</summary>
</details>

# 8	Read, generate, and modify configuration
<details><summary>8a	Demonstrate use of variables and outputs</summary>
</details>
<details><summary>8b	Describe secure secret injection best practice</summary>
</details>
<details><summary>8c	Understand the use of collection and structural types</summary>
</details>
<details><summary>8d	Create and differentiate resource and data configuration</summary>
</details>
<details><summary>8e	Use resource addressing and resource parameters to connect resources together</summary>
</details>
<details><summary>8f	Use HCL and Terraform functions to write configuration</summary>
</details>
<details><summary>8g	Describe built-in dependency management (order of execution based)</summary>
</details>

# 9	Understand Terraform Cloud capabilities
<details><summary>9a	Explain how Terraform Cloud helps to manage infrastructure</summary>
</details>
<details><summary>9b	Describe how Terraform Cloud enables collaboration and governance</summary>
</details>
