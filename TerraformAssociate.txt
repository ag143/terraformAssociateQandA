1)	Running terraform fmt without any flags in a directory with Terraform configuration files will check the formatting of those files without changing their contents.
12/26/2022 – by Mod_GuideK0 
Running terraform fmt without any flags in a directory with Terraform configuration files will check the formatting of those files without changing their contents.
A. True
B. False
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
The terraform fmt command is used to rewrite Terraform configuration files to a canonical format and style.

2)	Terraform variable names are saved in the state file.
12/26/2022 – by Mod_GuideK1 
Terraform variable names are saved in the state file.
A. True
B. False
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
Terraform stores information about your infrastructure in a state file. This state file keeps track of resources created by your configuration and maps them to real-world resources.
https://learn.hashicorp.com/tutorials/terraform/state-cli

3)	Terra form installs its providers during which phase?
12/26/2022 – by Mod_GuideK0 
Terra form installs its providers during which phase?
A. Man
B. Init
C. Refresh
D. All of the above
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
Providers are installed in the init phase

4)	A terraform apply can not___________infrastructure.
12/26/2022 – by Mod_GuideK0 
A terraform apply can not___________infrastructure.
A. import
B. provision
C. destroy
D. change
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
5)	Terraform plan updates your state file.
12/26/2022 – by Mod_GuideK0 
Terraform plan updates your state file.
A. True
B. False
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
The terraform plan command creates an execution plan, which lets you preview the changes that Terraform plans to make to your infrastructure. The plan command alone will not actually carry out the proposed changes, and so you can use this command to check whether the proposed changes match what you expected before you apply the changes or share your changes with your team for broader review. Source: https://www.terraform.io/cli/commands/plan
6)	Which task does teraform init not perform?
12/26/2022 – by Mod_GuideK0 
Which task does teraform init not perform?
A. Sources any modules and copies the configuration locally
B. Validates all required variables are present
C. Connects to the backend
D. Sources all providers present in the configuration and ensures they are downloaded and available locally
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
7)	You have to initialize a Terraform backend before it can be configured.
12/26/2022 – by Mod_GuideK0 
You have to initialize a Terraform backend before it can be configured.
A. True
B. False
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
Initialization
Whenever a configuration’s backend changes, you must run terraform init again to validate and configure the backend before you can perform any plans, applies, or state operations.
When changing backends, Terraform will give you the option to migrate your state to the new backend. This lets you adopt backends without losing any existing state.
To be extra careful, we always recommend manually backing up your state as well. You can do this by simply copying your terraform.tfstate file to another location. The initialization process should create a backup as well, but it never hurts to be safe!
https://www.terraform.io/language/settings/backends/configuration
8)	What does terraform refresh modify?
12/26/2022 – by Mod_GuideK0 
What does terraform refresh modify?
A. Your cloud infrastructure
B. Your Terraform plan
C. Your state file
D. Your Terraform configuration
HIDE ANSWERS
Correct Answer: C
Explanation/Reference:
Explanation:
9)	Which environment variables must be configured to make Terraform’s logging more verbose?
12/26/2022 – by Mod_GuideK0 
While attempting to deploy resources into your cloud provider using Terraform. you begin to see some odd behavior and experience sluggish responses. In order to troubleshoot you decide to turn on Terraform debugging. Which environment variables must be configured to make Terraform’s logging more verbose?
A. TF_10G_PATM
B. TF_LOG
C. TF_10G_LEVEL
D. TF.LOG.FUE
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
https://www.terraform.io/internals/debugging
10)	The Terraform CLI will print output values from a child module after running terraform apply.
12/26/2022 – by Mod_GuideK0 
The Terraform CLI will print output values from a child module after running terraform apply.
A. True
B. False
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
11)	which provisioned is best to use in your Terraform code?
12/26/2022 – by Mod_GuideK0 
As a member of the operations team, you need to run a script on a virtual machine created by Terraform. Which provisioned is best to use in your Terraform code?
A. local-exec
B. file
C. null-exec
D. remote-exec
HIDE ANSWERS
Correct Answer: D
Explanation/Reference:
Explanation:
https://www.terraform.io/language/resources/provisioners/remote-exec
12)	 Which of the following scenarios poses a challenge for this team?
12/26/2022 – by Mod_GuideK0 
If a DevOps team adopts AWS Cloud Formation as their standardized method for provisioning public cloud resources, which of the following scenarios poses a challenge for this team?
A. The team is asked to manage a new application stack built on AWS-natrve services
B. The organization decides to expand into Azure and wishes to deploy new infrastructure using their existing codebase
C. The team is asked to build a reusable code base that can deploy resources into any AWS region
D. The DevOps team is tasked with automating a manual provisioning process
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
13)	Which parameters does terraform import require?
12/26/2022 – by Mod_GuideK0 
Which parameters does terraform import require? Choose two correct answers.
A. Provider
B. Path
C. Resource address
D. Resource ID
HIDE ANSWERS
Correct Answer: CD
Explanation/Reference:
Explanation:
https://www.terraform.io/cli/commands/import#usage

14)	What will happen when you terraform apply upon returning to your desk?
12/26/2022 – by Mod_GuideK0 
You have been working in a Cloud provider account that is shared with other team members. You previously used Terraform to create a load balancer that is listening on port 80. After some application changes, you updated the Terraform code to change the port to 443.
You run terraform plan and see that the execution plan shows the port changing from 80 to 443 like you intended, and step away to grab some coffee.
In the meantime, another team member manually changes the load balancer port to 443 through the Cloud provider console before you get back to your desk.
What will happen when you terraform apply upon returning to your desk?
A. Terraform will not make any changes to the Load Balancer and will update the state file to reflect any changes made.
B. Terraform will change the port back to 80 in your code
C. Terraform will change the load balancer port to 80, and) then change it back to 443
D. Terraform will fail with in error because the state file is no longer accurate
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:

15) In a Terraform Cloud workspace linked to a version control repository, speculative plan runs start automatically when you merge or commit changes to version control.
12/26/2022 – by Mod_GuideK0 
In a Terraform Cloud workspace linked to a version control repository, speculative plan runs start automatically when you merge or commit changes to version control.
A. True
B. False
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
16)	When using multiple configurations of the same Terraform provider, what meta-argument must be included in any non-default provider configurations?
12/26/2022 – by Mod_GuideK0 
When using multiple configurations of the same Terraform provider, what meta-argument must be included in any non-default provider configurations?
A. name
B. alias
C. depends_on
D. id
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:

17)	What is a key benefit of the Terraform state file?
12/26/2022 – by Mod_GuideK1 
What is a key benefit of the Terraform state file?
A. A state file represents a source of truth for resources provisioned with a public cloud console
B. A state file represents a source of truth for resources provisioned with Terraform
C. A state file represents the desired state expressed by the Terraform code files D A state file can be used to schedule recurring infrastructure tasks
HIDE ANSWERS
Correct Answer: C
Explanation/Reference:
Explanation:
18)	When you use a remote backend that needs authentication.
12/26/2022 – by Mod_GuideK0 
When you use a remote backend that needs authentication. HashrCorp recommends that you:
A. Push your Tefraform configuration to an encrypted git repository
B. Write the authentication credentials in the Terraform configuration files
C. Use partial configuration to load the authentication credentials outside of the Terraform code
D. Keep the Terraform configuration files in a secret store
HIDE ANSWERS
Correct Answer: C
Explanation/Reference:
Explanation:
We recommend omitting the token from the configuration, and instead using terraform login or manually configuring credentials in the CLI config file. Reference:
https://www.terraform.io/language/settings/backends/remote
19)	Which of the following statements about local modules is incorrect:
12/26/2022 – by Mod_GuideK0 
Which of the following statements about local modules is incorrect:
A. Local modules are not cached by terraform init command
B. Local modules are sourced from a directory on disk
C. Local modules support versions
D. All of the above (all statements above are incorrect
E. None of the above (all statements above are correct)
HIDE ANSWERS
Correct Answer: C
Explanation/Reference:
Explanation:
Version constraints are supported only for modules installed from a module registry, such as the public Terraform Registry or Terraform Cloud’s private module registry. Other module sources can provide their own versioning mechanisms within the source string itself, or might not support versions at all. In particular, modules sourced from local file paths do not support version; since they’re loaded from the same source repository, they always share the same version as their caller.
https://www.terraform.io/language/modules/syntax

20)	Which of the following is not a benefit of adopting infrastructure as code?
12/26/2022 – by Mod_GuideK0 
Which of the following is not a benefit of adopting infrastructure as code?
A. Automation
B. Versioning
C. Reusability of code
D. Interpolation
HIDE ANSWERS
Correct Answer: D
Explanation/Reference:
Explanation:

21)	What Terraform feature would help you define the blocks using the values in a variable?
12/26/2022 – by Mod_GuideK0 
You want to define multiple data disks as nested blocks inside the resource block for a virtual machine. What Terraform feature would help you define the blocks using the values in a variable?
A. Local values
B. Dynamic blocks
C. Count arguments
D. Collection functions
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:

22)	Terraform apply will fail if you have not run terraform plan first to update the plan output.
12/26/2022 – by Mod_GuideK0 
terraform apply will fail if you have not run terraform plan first to update the plan output.
A. True
B. False
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:

23)	Which argument(s) are required when declaring a Terraform variable?
12/26/2022 – by Mod_GuideK0 
Which argument(s) are required when declaring a Terraform variable?
A. type
B. default
C. description
D. All of the above
E. None of the above
HIDE ANSWERS
Correct Answer: E
Explanation/Reference:
Explanation:
Terraform CLI defines the following OPTIONAL arguments for variable declarations: default – A default value which then makes the variable optional. type – This argument specifies what value types are accepted for the variable. description
– This specifies the input variable’s documentation. validation – A block to define validation rules, usually in addition to type constraints. sensitive – Limits Terraform UI output when the variable is used in configuration. nullable – Specify if the variable can be null within the module.
https://www.terraform.io/language/values/variables#arguments


24)	Where can Terraform not load a provider from?
12/26/2022 – by Mod_GuideK0 
Where can Terraform not load a provider from?
A. Plugins directory
B. Provider plugin cache
C. Official HashrCorp distribution on releases, hashicorp.com
D. Source code
HIDE ANSWERS
Correct Answer: D
Explanation/Reference:
Explanation:

25)	What feature of Terraform Cloud and/or Terraform Enterprise can you publish and maintain a set of custom modules which can be used within your organization?
12/26/2022 – by Mod_GuideK0 
What feature of Terraform Cloud and/or Terraform Enterprise can you publish and maintain a set of custom modules which can be used within your organization?
A. Terraform registry
B. custom VCS integration
C. private module registry
D. remote runs
HIDE ANSWERS
Correct Answer: C
Explanation/Reference:
Explanation:

26)	When using providers that require the retrieval of data, such as the HashiCorp Vault provider, in what phase does Terraform actually retrieve the data required?
12/26/2022 – by Mod_GuideK0 
When using providers that require the retrieval of data, such as the HashiCorp Vault provider, in what phase does Terraform actually retrieve the data required?
A. terraform delete
B. terraform plan
C. terraform init
D. terraform apply
HIDE ANSWERS
Correct Answer: C
Explanation/Reference:
Explanation:

27)	When Terraform needs to be installed in a location where it does not have internet access to download the installer and upgrades, the installation is generally known as to be __________.
12/26/2022 – by Mod_GuideK0 
When Terraform needs to be installed in a location where it does not have internet access to download the installer and upgrades, the installation is generally known as to be __________.
A. a private install
B. disconnected
C. air-gapped
D. non-traditional
HIDE ANSWERS
Correct Answer: D
Explanation/Reference:
Explanation:
A Terraform Enterprise install that is provisioned on a network that does not have Internet access is generally known as an air-gapped install. These types of installs require you to pull updates, providers, etc. from external sources vs. being able to download them directly.

28)	Terraform Enterprise (also referred to as pTFE) requires what type of backend database for a clustered deployment?
12/26/2022 – by Mod_GuideK0 
Terraform Enterprise (also referred to as pTFE) requires what type of backend database for a clustered deployment?
A. PostgreSQL
B. Cassandra
C. MySQL
D. MSSQL
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
External Services mode stores the majority of the stateful data used by the instance in an external PostgreSQL database and an external S3-compatible endpoint or Azure blob storage. There is still critical data stored on the instance that must be managed with snapshots. Be sure to check the PostgreSQL Requirements for information that needs to be present for Terraform Enterprise to work.
This option is best for users with expertise managing PostgreSQL or users that have access to managed PostgreSQL offerings like AWS RDS.


29)	Terraform Cloud is more powerful when you integrate it with your version control system (VCS) provider.
12/26/2022 – by Mod_GuideK0 
Terraform Cloud is more powerful when you integrate it with your version control system (VCS) provider. Select all the supported VCS providers from the answers below. (select four)
A. GitHub
B. CVS Version Control
C. Azure DevOps Server
D. Bitbucket Cloud
E. GitHub Enterprise
HIDE ANSWERS
Correct Answer: ACDE
Explanation/Reference:
Explanation:
Terraform Cloud supports the following VCS providers:
– https://www.terraform.io/docs/cloud/vcs/github.html
– https://www.terraform.io/docs/cloud/vcs/github.html
– https://www.terraform.io/docs/cloud/vcs/github-enterprise.html
– https://www.terraform.io/docs/cloud/vcs/gitlab-com.html
– https://www.terraform.io/docs/cloud/vcs/gitlab-eece.html
– https://www.terraform.io/docs/cloud/vcs/bitbucket-cloud.html
– https://www.terraform.io/docs/cloud/vcs/bitbucket-server.html
– https://www.terraform.io/docs/cloud/vcs/azure-devops-server.html
– https://www.terraform.io/docs/cloud/vcs/azure-devops-services.html
https://www.terraform.io/docs/cloud/vcs/index.html#supported-vcs-providers

30)	From the code below, identify the implicit dependency:
12/26/2022 – by Mod_GuideK0 
From the code below, identify the implicit dependency:
A. The EIP with an id of ami-2757f631
B. The AMI used for the EC2 instance
C. The EC2 instance labeled web_server
D. The S3 bucket labeled company_data
HIDE ANSWERS
Correct Answer: C
Explanation/Reference:
Explanation:
31)	Which of the following statements describes best how terraform resource dependencies are handled?
12/26/2022 – by Mod_GuideK0 
In terraform, most resource dependencies are handled automatically. Which of the following statements describes best how terraform resource dependencies are handled?
A. Resource dependencies are identified and maintained in a file called resource.dependencies. Each terraform provider is required to maintain a list of all resource dependencies for the provider and it’s included with the plugin during initialization when terraform init is executed. The file is located in the terraform.d folder.
B. The terraform binary contains a built-in reference map of all defined Terraform resource dependencies. Updates to this dependency map are reflected in terraform versions. To ensure you are working with the latest resource dependency map you much be running the latest version of Terraform.
C. Resource dependencies are handled automatically by the depends_on meta_argument, which is set to true by default.
D. Terraform analyses any expressions within a resource block to find references to other objects, and treats those references as implicit ordering requirements when creating, updating, or destroying resources.
HIDE ANSWERS
Correct Answer: D
Explanation/Reference:
Explanation:
https://www.terraform.io/docs/configuration/resources.html


32)	What is the result of the following terraform function call?
12/26/2022 – by Mod_GuideK0 
What is the result of the following terraform function call?
A. hello
B. what?
C. goodbye
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
https://www.terraform.io/docs/configuration/functions/lookup.html


33)	Which statements best describes what the local variable assignment is doing in the following code snippet:
12/26/2022 – by Mod_GuideK1 
Which statements best describes what the local variable assignment is doing in the following code snippet:
A. Create a distinct list of route table name objects
B. Create a map of route table names to subnet names
C. Create a map of route table names from a list of subnet names
D. Create a list of route table names eliminating duplicates
HIDE ANSWERS
Correct Answer: D
Explanation/Reference:
Explanation:

34)	In the following code snippet, the block type is identified by which string?
12/26/2022 – by Mod_GuideK0 
In the following code snippet, the block type is identified by which string?
A. “aws_instance”
B. resource
C. “db”
D. instance_type
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:

35)	Which of the following is an invalid variable name?
12/26/2022 – by Mod_GuideK0 
Which of the following is an invalid variable name?
A. count
B. web
C. var1
D. instance_name
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
https://www.terraform.io/intro/examples/count.html


36)	A user runs terraform init on their RHEL based server and per the output, two provider plugins are downloaded: $ terraform init Initializing the backend.
12/26/2022 – by Mod_GuideK0 
A user runs terraform init on their RHEL based server and per the output, two provider plugins are downloaded: $ terraform init Initializing the backend…
Initializing provider plugins…
– Checking for available provider plugins…
– Downloading plugin for provider “aws” (hashicorp/aws) 2.44.0…
– Downloading plugin for provider “random” (hashicorp/random) 2.2.1…
:
Terraform has been successfully initialized! Where are these plugins downloaded to?
A. The .terraform.plugins directory in the directory terraform init was executed in.
B. The .terraform/plugins directory in the directory terraform init was executed in.
C. /etc/terraform/plugins
D. The .terraform.d directory in the directory terraform init was executed in.
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:

37) Anyone can publish and share modules on the Terraform Public Module Registry, and meeting the requirements for publishing a module is extremely easy.
12/26/2022 – by Mod_GuideK0 
Anyone can publish and share modules on the Terraform Public Module Registry, and meeting the requirements for publishing a module is extremely easy. Select from the following list all valid requirements. (select three)
A. The module must be PCI/HIPPA compliant.
B. Module repositories must use this three-part name format, terraform– .
C. The registry uses tags to identify module versions.
D. Release tag names must be for the format x.y.z, and can optionally be prefixed with a v .
E. The module must be on GitHub and must be a public repo.
HIDE ANSWERS
Correct Answer: CDE
Explanation/Reference:
Explanation:
https://www.terraform.io/docs/registry/modules/publish.html#requirements

38)	Why might a user opt to include the following snippet in their configuration file?
12/26/2022 – by Mod_GuideK0 
Why might a user opt to include the following snippet in their configuration file?
A. Terraform 0.12 introduced substantial changes to the syntax used to write Terraform configuration
B. The user wants to ensure that the application being deployed is a minimum version of 0.12
C. this ensures that all Terraform providers are above a certain version to match the application being deployed
D. versions before Terraform 0.12 were not approved by HashiCorp to be used in production
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:


39)	True or False?
12/26/2022 – by Mod_GuideK0 
True or False? When using the Terraform provider for Vault, the tight integration between these HashiCorp tools provides the ability to mask secrets in the terraform plan and state files.
A. False
B. True
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
Currently, Terraform has no mechanism to redact or protect secrets that are returned via data sources, so secrets read via this provider will be persisted into the Terraform state, into any plan files, and in some cases in the console output produced while planning and applying. These artifacts must, therefore, all be protected accordingly.


40)	Which of the following statements best describes the Terraform list(…) type?
12/26/2022 – by Mod_GuideK0 
Which of the following statements best describes the Terraform list(…) type?
A. a collection of values where each is identified by a string label.
B. a sequence of values identified by consecutive whole numbers starting with zero.
C. a collection of unique values that do not have any secondary identifiers or ordering.
D. a collection of named attributes that each have their own type.
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
A terraform list is a sequence of values identified by consecutive whole numbers starting with zero.
https://www.terraform.io/docs/configuration/types.html#structural-types

41)	Which of the following is not a valid Terraform string function?
12/26/2022 – by Mod_GuideK1 
Which of the following is not a valid Terraform string function?
A. replace
B. format
C. join
D. tostring
HIDE ANSWERS
Correct Answer: D
Explanation/Reference:
Explanation:
https://www.terraform.io/docs/configuration/functions/tostring.html


42)	What happens to the resource?
12/26/2022 – by Mod_GuideK0 
During a terraform plan, a resource is successfully created but eventually fails during provisioning.
What happens to the resource?
A. Terraform attempts to provision the resource up to three times before exiting with an error
B. the terraform plan is rolled back and all provisioned resources are removed
C. it is automatically deleted
D. the resource is marked as tainted
HIDE ANSWERS
Correct Answer: D
Explanation/Reference:
Explanation:
If a resource successfully creates but fails during provisioning, Terraform will error and mark the resource as “tainted”. A resource that is tainted has been physically created, but can’t be considered safe to use since provisioning failed.
Terraform also does not automatically roll back and destroy the resource during the apply when the failure happens, because that would go against the execution plan: the execution plan would’ve said a resource will be created, but does not say it will ever be deleted.

43)	Which of the following commands will launch the Interactive console for Terraform interpolations?
12/26/2022 – by Mod_GuideK1 
Which of the following commands will launch the Interactive console for Terraform interpolations?
A. terraform console
B. terraform cli
C. terraform
D. terraform cmdline
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
https://www.terraform.io/docs/commands/console.html

44)	Select all Operating Systems that Terraform is available for.
12/26/2022 – by Mod_GuideK0 
Select all Operating Systems that Terraform is available for. (select five)
A. Linux
B. macOS
C. Unix
D. Solaris
E. Windows
F. FreeBSD
HIDE ANSWERS
Correct Answer: ABDEF
Explanation/Reference:
Explanation:
Terraform is available for macOS, FreeBSD, OpenBSD, Linux, Solaris, Windows
https://www.terraform.io/downloads.html


45)	Which of the following commands will the user run to switch to the dev workspace?
12/26/2022 – by Mod_GuideK0 
A user creates three workspaces from the command line – prod, dev, and test. Which of the following commands will the user run to switch to the dev workspace?
A. terraform workspace dev
B. terraform workspace select dev
C. terraform workspace -switch dev
D. terraform workspace switch dev
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
The terraform workspace select command is used to choose a different workspace to use for further operations. https://www.terraform.io/docs/commands/workspace/select.html


46)	Select the most accurate statement to describe the Terraform language from the following list.
12/26/2022 – by Mod_GuideK0 
Select the most accurate statement to describe the Terraform language from the following list.
A. Terraform is an immutable, declarative, Infrastructure as Code provisioning language based on Hashicorp Configuration Language, or optionally JSON.
B. Terraform is a mutable, declarative, Infrastructure as Code configuration management language based on Hashicorp Configuration Language, or optionally JSON.
C. Terraform is an immutable, procedural, Infrastructure as Code configuration management language based on Hashicorp Configuration Language, or optionally JSON.
D. Terraform is a mutable, procedural, Infrastructure as Code provisioning language based on Hashicorp Configuration Language, or optionally YAML.
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
Terraform is not a configuration management tool –
https://www.terraform.io/intro/vs/chefpuppet.htmlTerraform is a declarative language – https://www.terraform.io/docs/configuration/index.htmlTerraform supports a syntax that is JSON compatible –
https://www.terraform.io/docs/configuration/syntax-json.htmlTerraform is primarily designed on immutable infrastructure principles –
https://www.hashicorp.com/resources/what-is-mutable-vs-immutable-infrastructure

47)True or False?
12/26/2022 – by Mod_GuideK0 
True or False? By default, Terraform destroy will prompt for confirmation before proceeding.
A. False
B. True
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
48)	True or False?
12/26/2022 – by Mod_GuideK0 
True or False? Each Terraform workspace uses its own state file to manage the infrastructure associated with that particular workspace.
A. False
B. True
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
The persistent data stored in the backend belongs to a workspace. Initially, the backend has only one workspace, called “default”, and thus there is only one Terraform state associated with that configuration.

49)	True or False.
12/26/2022 – by Mod_GuideK0 
True or False. The terraform refresh command is used to reconcile the state Terraform knows about (via its state file) with the real-world infrastructure. If drift is detected between the real-world infrastructure and the last known-state, it will modify the infrastructure to correct the drift.
A. False
B. True
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
https://www.terraform.io/docs/commands/refresh.html

50)	When validated, results in the following error:
12/26/2022 – by Mod_GuideK0 
The following is a snippet from a Terraform configuration file:
Which, when validated, results in the following error:
Fill in the blank in the error message with the correct string from the list below.
A. version
B. multi
C. label
D. alias
HIDE ANSWERS
Correct Answer: D
Explanation/Reference:
Explanation:
https://www.terraform.io/docs/configuration/providers.html#alias-multiple-providerinstances

51)	Complete the following sentence:
12/26/2022 – by Mod_GuideK0 
Complete the following sentence:
The terraform state command can be used to ____
A. modify state
B. view state
C. refresh state
D. There is no such command
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
https://www.terraform.io/docs/commands/state/index.html


52)	Provider dependencies are created in several different ways.
12/26/2022 – by Mod_GuideK0 
Provider dependencies are created in several different ways. Select the valid provider dependencies from the following list: (select three)
A. Explicit use of a provider block in configuration, optionally including a version constraint.
B. Use of any resource belonging to a particular provider in a resource or data block in configuration.
C. Existence of any resource instance belonging to a particular provider in the current state.
D. Existence of any provider plugins found locally in the working directory.
HIDE ANSWERS
Correct Answer: ABC
Explanation/Reference:
Explanation:
The existence of a provider plugin found locally in the working directory does not itself create a provider dependency. The plugin can exist without any reference to it in the terraform configuration.
https://www.terraform.io/docs/commands/providers.html

53)	In order to reduce the time it takes to provision resources, Terraform uses parallelism. By default, how many resources will Terraform provision concurrently?
12/26/2022 – by Mod_GuideK0 
In order to reduce the time it takes to provision resources, Terraform uses parallelism. By default, how many resources will Terraform provision concurrently?
A. 5
B. 50
C. 10
D. 20
HIDE ANSWERS
Correct Answer: C
Explanation/Reference:
Explanation:

54)	Select the operating systems which are supported for a clustered Terraform Enterprise: (select four)
12/26/2022 – by Mod_GuideK0 
Select the operating systems which are supported for a clustered Terraform Enterprise: (select four)
A. Unix
B. Red Hat
C. CentOS
D. Amazon Linux
E. Ubuntu
HIDE ANSWERS
Correct Answer: BCDE
Explanation/Reference:
Explanation:
https://www.terraform.io/docs/enterprise/before-installing/index.html#operatingsystemrequirements

55)	What other syntax can Terraform are expressed in?
12/26/2022 – by Mod_GuideK0 
While Terraform is generally written using the HashiCorp Configuration Language (HCL), what other syntax can Terraform are expressed in?
A. JSON
B. YAML
C. TypeScript
D. XML
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
The constructs in the Terraform language can also be expressed in JSON syntax, which is harder for humans to read and edit but easier to generate and parse programmatically.

56)	What is the result of the following terraform function call?
12/26/2022 – by Mod_GuideK0 
What is the result of the following terraform function call?
A. True
B. False
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
https://www.terraform.io/docs/configuration/functions/index.html

57)	In the example below, the depends_on argument creates what type of dependency?
12/26/2022 – by Mod_GuideK0 
In the example below, the depends_on argument creates what type of dependency?
A. implicit dependency
B. internal dependency
C. explicit dependency
D. non-dependency resource
HIDE ANSWERS
Correct Answer: C
Explanation/Reference:
Explanation:

58)	Which of the following lines would be required in a module configuration block in terraform to select tagged version v1.0.4?
12/26/2022 – by Mod_GuideK0 
A user has created a module called “my_test_module” and committed it to GitHub. Over time, several commits have been made with updates to the module, each tagged in GitHub with an incremental version number. Which of the following lines would be required in a module configuration block in terraform to select tagged version v1.0.4?
A. source = “git::https://example.com/my_test_module.git@tag=v1.0.4”
B. source = “git::https://example.com/my_test_module.git&ref=v1.0.4”
C. source = “git::https://example.com/my_test_module.git#tag=v1.0.4”
D. source = “git::https://example.com/my_test_module.git?ref=v1.0.4”
HIDE ANSWERS
Correct Answer: D
Explanation/Reference:
Explanation:
https://www.terraform.io/docs/modules/sources.html#selecting-a-revision

59)	Which of the following terraform subcommands could be used to remove the lock on the state for the current configuration?
12/26/2022 – by Mod_GuideK0 
Which of the following terraform subcommands could be used to remove the lock on the state for the current configuration?
A. Unlock
B. force-unlock
C. Removing the lock on a state file is not possible
D. state-unlock
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
https://www.terraform.io/docs/commands/force-unlock.html


60)	 True or False?
12/26/2022 – by Mod_GuideK1 
True or False? terraform init cannot automatically download Community providers.
A. False
B. True
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:



61)	True or False: Workspaces provide identical functionality in the open-source, Terraform Cloud, and Enterprise versions of Terraform.
12/26/2022 – by Mod_GuideK0 
True or False: Workspaces provide identical functionality in the open-source, Terraform Cloud, and Enterprise versions of Terraform.
A. True
B. False
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
https://www.terraform.io/docs/cloud/workspaces/index.html
https://www.terraform.io/docs/state/workspaces.html


62)	What is the best and easiest way for Terraform to read and write secrets from HashiCorp Vault?
12/26/2022 – by Mod_GuideK0 
What is the best and easiest way for Terraform to read and write secrets from HashiCorp Vault?
A. Vault provider
B. API access using the AppRole auth method
C. integration with a tool like Jenkins
D. CLI access from the same machine running Terraform
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:

63)	What are some of the problems of how infrastructure was traditionally managed before Infrastructure as Code?
12/26/2022 – by Mod_GuideK0 
What are some of the problems of how infrastructure was traditionally managed before Infrastructure as Code? (select three)
A. Requests for infrastructure or hardware required a ticket, increasing the time required to deploy applications
B. Traditional deployment methods are not able to meet the demands of the modern business where resources tend to live days to weeks, rather than months to years
C. Traditionally managed infrastructure can’t keep up with cyclic or elastic applications
D. Pointing and clicking in a management console is a scalable approach and reduces human error as businesses are moving to a multi-cloud deployment model
HIDE ANSWERS
Correct Answer: ABC
Explanation/Reference:
Explanation:
Businesses are making a transition where traditionally-managed infrastructure can no longer meet the demands of today’s businesses. IT organizations are quickly adopting the public cloud, which is predominantly API-driven. To meet customer demands and save costs, application teams are architecting their applications to support a much higher level of elasticity, supporting technology like containers and public cloud resources. These resources may only live for a matter of hours; therefore the traditional method of raising a ticket to request resources is no longer a viable option Pointing and clicking in a management console is NOT scale and increases the change of human error.


64)	What are the benefits of using Infrastructure as Code?
12/26/2022 – by Mod_GuideK0 
What are the benefits of using Infrastructure as Code? (select five)
A. Infrastructure as Code is relatively simple to learn and write, regardless of a user’s prior experience with developing code
B. Infrastructure as Code provides configuration consistency and standardization among deployments
C. Infrastructure as Code is easily repeatable, allowing the user to reuse code to deploy similar, yet different resources
D. Infrastructure as Code gives the user the ability to recreate an application’s infrastructure for disaster recovery scenarios
E. Infrastructure as Code easily replaces development languages such as Go and .Net for application development
F. Infrastructure as Code allows a user to turn a manual task into a simple, automated deployment
(Correct)
HIDE ANSWERS
Correct Answer: ACDF
Explanation/Reference:
Explanation:
If you are new to infrastructure as code as a concept, it is the process of managing infrastructure in a file or files rather than manually configuring resources in a user interface.
A resource in this instance is any piece of infrastructure in a given environment, such as a virtual machine, security group, network interface, etc. At a high level, Terraform allows operators to use HCL to author files containing definitions of their desired resources on almost any provider (AWS, GCP, GitHub, Docker, etc) and automates the creation of those resources at the time of application.



65)	Which of the following Terraform features are only available in the Enterprise edition?
12/26/2022 – by Mod_GuideK1 
HashiCorp offers multiple versions of Terraform, including Terraform open-source, Terraform Cloud, and Terraform Enterprise. Which of the following Terraform features are only available in the Enterprise edition? (select four)
A. SAML/SSO
B. Sentinel
C. Audit Logs
D. Clustering
E. Private Module Registry
F. Private Network Connectivity
HIDE ANSWERS
Correct Answer: ACF
Explanation/Reference:
Explanation:
While there are a ton of features that are available to open source users, many features that are part of the Enterprise offering are geared towards larger teams and enterprise functionality. To see what specific features are part of Terraform Cloud and Terraform Enterprise, check out this link.
https://www.hashicorp.com/products/terraform/pricing/

66)	What Terraform feature is shown in the example below?
12/26/2022 – by Mod_GuideK0 
What Terraform feature is shown in the example below?
A. conditional expression
B. local values
C. dynamic block
D. data source
HIDE ANSWERS
Correct Answer: C
Explanation/Reference:
Explanation:


67)	Select the answer below that completes the following statement: Terraform Cloud can be managed from the CLI but requires __________?
12/26/2022 – by Mod_GuideK0 
Select the answer below that completes the following statement: Terraform Cloud can be managed from the CLI but requires __________?
A. an API token
B. a TOTP token
C. a username and password
D. authentication using MFA
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
API and CLI access are managed with API tokens, which can be generated in the Terraform Cloud UI.
Each user can generate any number of personal API tokens, which allow access with their own identity and permissions. Organizations and teams can also generate tokens for automating tasks that aren’t tied to an individual user.


68)	What Terraform command can be used to inspect the current state file?
12/26/2022 – by Mod_GuideK0 
What Terraform command can be used to inspect the current state file?
A. terraform inspect
B. terraform read
C. terraform show
D. terraform state
HIDE ANSWERS
Correct Answer: C
Explanation/Reference:
Explanation:

69)	What are the ways the remaining configuration can be added to Terraform so it can initialize and communicate with the backend?
12/26/2022 – by Mod_GuideK0 
When configuring a remote backend in Terraform, it might be a good idea to purposely omit some of the required arguments to ensure secrets and other important data aren’t inadvertently shared with others. What are the ways the remaining configuration can be added to Terraform so it can initialize and communicate with the backend? (select three)
A. directly querying HashiCorp Vault for the secrets
B. command-line key/value pairs
C. use the -backend-config=PATH to specify a separate config file
D. interactively on the command line
HIDE ANSWERS
Correct Answer: BCD
Explanation/Reference:
Explanation:
You do not need to specify every required argument in the backend configuration. Omitting certain arguments may be desirable to avoid storing secrets, such as access keys, within the main configuration. When some or all of the arguments are omitted, we call this a partial configuration.
With a partial configuration, the remaining configuration arguments must be provided as part of the initialization process. There are several ways to supply the remaining arguments:
https://www.terraform.io/docs/backends/init.html#backend-initialization


70)	 What are some of the features of Terraform state?
12/26/2022 – by Mod_GuideK1 
What are some of the features of Terraform state? (select three)
A. inspection of cloud resources
B. determining the correct order to destroy resources
C. mapping configuration to real-world resources
D. increased performance
HIDE ANSWERS
Correct Answer: CD
Explanation/Reference:
Explanation:

71)	Where does Terraform store its state file?
12/26/2022 – by Mod_GuideK0 
By default, where does Terraform store its state file?
A. Amazon S3 bucket
B. shared directory
C. remotely using Terraform Cloud
D. current working directory
HIDE ANSWERS
Correct Answer: D
Explanation/Reference:
Explanation:
By default, the state file is stored in a local file named “terraform.tfstate”, but it can also be stored remotely, which works better in a team environment.


72)	Given the Terraform configuration below, in which order will the resources be created?
12/26/2022 – by Mod_GuideK0 
Given the Terraform configuration below, in which order will the resources be created?
A. Larger image
B. resources will be created simultaneously
C. aws_eip will be created first aws_instance will be created second
D. aws_instance will be created first aws_eip will be created second
HIDE ANSWERS
Correct Answer: D
Explanation/Reference:
Explanation:
The aws_instance will be created first, and then aws_eip will be created second due to the aws_eip’s resource dependency of the aws_instance id

73)	Select two answers to complete the following sentence: Before a new provider can be used, it must be ______ and _______.
12/26/2022 – by Mod_GuideK0 
Select two answers to complete the following sentence: Before a new provider can be used, it must be ______ and _______.
A. approved by HashiCorp
B. uploaded to source control
C. declared in the configuration
D. initialized
HIDE ANSWERS
Correct Answer: CD
Explanation/Reference:
Explanation:
Each time a new provider is added to configuration — either explicitly via a provider block or by adding a resource from that provider — Terraform must initialize the provider before it can be used.
Initialization downloads and installs the provider’s plugin so that it can later be executed.


74)	Which of the following value will be accepted for my_var?
12/26/2022 – by Mod_GuideK0 
Which of the following value will be accepted for my_var?
1. variable “my_var”
2. {
3. type = string
4. }
A. 15
B. “15”
C. Both A and B
D. None of the above
HIDE ANSWERS
Correct Answer: C
Explanation/Reference:
Explanation:
The Terraform language will automatically convert number and bool values to string values when needed, and vice-versa as long as the string contains a valid representation of a number or boolean value.
Example
* true converts to “true”, and vice-versa
* false converts to “false”, and vice-versa
* 15 converts to “15”, and vice-versa
Where possible, Terraform automatically converts values from one type to another in order to produce the expected type. If this isn’t possible, Terraform will produce a type mismatch error and you must update the configuration with a more suitable expression.
https://www.terraform.io/docs/configuration/expressions.html#type-conversion


75)	Which of the below backends support state locking?
12/26/2022 – by Mod_GuideK0 
Which of the below backends support state locking?
A. S3
B. consul
C. azurerm
D. artifactory
HIDE ANSWERS
Correct Answer: ABC
Explanation/Reference:
Explanation:


76)	How can you ensure that?
12/26/2022 – by Mod_GuideK0 
resource “aws_s3_bucket” “example” { bucket = “my-test-s3-terraform-bucket” …} resource “aws_iam_role” “test_role” { name = “test_role” …} Due to the way that the application code is written , the s3 bucket must be created before the test role is created , otherwise there will be a problem. How can you ensure that?
A. This will already be taken care of by terraform native implicit dependency. Nothing else needs to be done from your end.
B. Add explicit dependency using depends_on . This will ensure the correct order of resource creation.
C. Create 2 separate terraform config scripts , and run them one by one , 1 for s3 bucket , and another for IAM role , run the S3 bucket script first.
D. This is not possible to control in terraform . Terraform will take care of it in a native way , and create a dependency graph that is best suited for the parallel resource creation.
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
Use the depends_on meta-argument to handle hidden resource dependencies that Terraform can’t automatically infer.
Explicitly specifying a dependency is only necessary when a resource relies on some other resource’s behavior but doesn’t access any of that resource’s data in its arguments.

77)	When using constraint expressions to signify a version of a provider, which of the following are valid provider versions that satisfy the expression found in the following code snippet: (select two) 1.
12/26/2022 – by Mod_GuideK0 
When using constraint expressions to signify a version of a provider, which of the following are valid provider versions that satisfy the expression found in the following code snippet: (select two) 1. terraform 2. { 3. required_providers 4. { 5. aws = “~> 1.2.0” 6. } 7. }
A. 1.3.1
B. 1.2.3
C. 1.2.9
D. 1.3.0
HIDE ANSWERS
Correct Answer: BC
Explanation/Reference:
Explanation:
As your Terraform usage becomes more advanced, there are some cases where you may need to modify the Terraform state. Rather than modify the state directly, the terraform state commands can be used in many cases instead. This command is a nested subcommand, meaning that it has further subcommands.
https://www.terraform.io/docs/commands/state/index.html

78)	Which Terraform command will check and report errors within modules, attribute names, and value types to make sure they are syntactically valid and internally consistent?
12/26/2022 – by Mod_GuideK0 
Which Terraform command will check and report errors within modules, attribute names, and value types to make sure they are syntactically valid and internally consistent?
A. terraform validate
B. terraform format
C. terraform fmt
D. terraform show
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
The terraform validate command validates the configuration files in a directory, referring only to the configuration and not accessing any remote services such as remote state, provider APIs, etc.
Validate runs checks that verify whether a configuration is syntactically valid and internally consistent, regardless of any provided variables or existing state. It is thus primarily useful for general verification of reusable modules, including the correctness of attribute names and value types.
It is safe to run this command automatically, for example as a post-save check in a text editor or as a test step for a re-usable module in a CI system.

79)	In order to make a Terraform configuration file dynamic and/or reusable, static values should be converted to use what?
12/26/2022 – by Mod_GuideK0 
In order to make a Terraform configuration file dynamic and/or reusable, static values should be converted to use what?
A. Input Parameters
B. Module
C. Regular Expressions
D. Output Value
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
Input variables serve as parameters for a Terraform module, allowing aspects of the module to be customized without altering the module’s own source code, and allowing modules to be shared between different configurations.
https://www.terraform.io/docs/configuration/variables.html

80)	What should be your next plan of action?
12/26/2022 – by Mod_GuideK0 
Your company has a lot of workloads in AWS , and Azure that were respectively created using CloudFormation , and AzureRM Templates. However , now your CIO has decided to use Terraform for all new projects , and has asked you to check how to integrate the existing environment with terraform code. What should be your next plan of action?
A. Tell the CIO that this is not possible . Resources created in CloudFormation , and AzureRM templates cannot be tracked using terraform.
B. Use terraform import command to import each resource one by one .
C. This is only possible in Terraform Enterprise , which has the TerraformConverter exe that can take any other template language like AzureRM and convert to Terraform code.
D. Just write the terraform config file for the new resources , and run terraform apply , the state file will automatically be updated with the details of the new resources to be imported.
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:

81)	Terraform will sync all resources in state by default for every plan and apply, hence for larger infrastructures this can slow down terraform plan and terraform apply commands?
12/26/2022 – by Mod_GuideK0 
Terraform will sync all resources in state by default for every plan and apply, hence for larger infrastructures this can slow down terraform plan and terraform apply commands?
A. False
B. True
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
For small infrastructures, Terraform can query your providers and sync the latest attributes from all your resources. This is the default behavior of Terraform: for every plan and apply, Terraform will sync all resources in your state.
For larger infrastructures, querying every resource is too slow. Many cloud providers do not provide APIs to query multiple resources at once, and the round trip time for each resource is hundreds of milliseconds. On top of this, cloud providers almost always have API rate limiting so Terraform can only request a certain number of resources in a period of time. Larger users of Terraform make heavy use of the -refresh=false flag as well as the -target flag in order to work around this. In these scenarios, the cached state is treated as the record of truth.
https://www.terraform.io/docs/state/purpose.html

82)	Which feature of Terraform allows multiple state files for a single configuration file depending upon the environment?
12/26/2022 – by Mod_GuideK0 
Which feature of Terraform allows multiple state files for a single configuration file depending upon the environment?
A. Terraform Modules
B. Terraform Enterprise
C. Terraform Workspaces
D. Terraform Remote Backends
HIDE ANSWERS
Correct Answer: C
Explanation/Reference:
Explanation:

83)	What does the command terraform fmt do?
12/26/2022 – by Mod_GuideK0 
What does the command terraform fmt do?
A. Rewrite Terraform configuration files to a canonical format and style.
B. Deletes the existing configuration file.
C. Updates the font of the configuration file to the official font supported by HashiCorp.
D. Formats the state file in order to ensure the latest state of resources can be obtained.
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
The terraform fmt command is used to rewrite Terraform configuration files to a canonical format and style. This command applies a subset of the Terraform language style conventions, along with other minor adjustments for readability.
Other Terraform commands that generate Terraform configuration will produce configuration files that conform to the style imposed by terraform fmt, so using this style in your own files will ensure consistency.
https://www.terraform.io/docs/commands/fmt.html

84)	Where is the value of the DNS record’s IP address originating from?
12/26/2022 – by Mod_GuideK0 
In the example below, where is the value of the DNS record’s IP address originating from?
1. resource “aws_route53_record” “www”
2. {
3. zone_id = aws_route53_zone.primary.zone_id
4. name = “www.example.com”
5. type = “A”
6. ttl = “300”
7. records = [module.web_server.instance_ip_address]
8. }
A. The regular expression named module.web_server
B. The output of a module named web_server
C. By querying the AWS EC2 API to retrieve the IP address
D. Value of the web_server parameter from the variables.tf file
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
In a parent module, outputs of child modules are available in expressions as module.<MODULE NAME>.<OUTPUT NAME>.
For example, if a child module named web_server declared an output named instance_ip_address, you could access that value as module.web_server.instance_ip_address.
85)	Multiple provider instances blocks for AWS can be part of a single configuration file?
12/26/2022 – by Mod_GuideK0 
Multiple provider instances blocks for AWS can be part of a single configuration file?
A. False
B. True
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
You can optionally define multiple configurations for the same provider, and select which one to use on a per-resource or per-module basis. The primary reason for this is to support multiple regions for a cloud platform; other examples include targeting multiple Docker hosts, multiple Consul hosts, etc.
To include multiple configurations for a given provider, include multiple provider blocks with the same provider name, but set the alias meta-argument to an alias name to use for each additional configuration. For example:
# The default provider configuration provider “aws” { region = “us-east-1”
} # Additional provider configuration for west coast region provider “aws” { alias = “west” region = “us-west-2”
} The provider block without alias set is known as the default provider configuration. When alias is set, it creates an additional provider configuration. For providers that have no required configuration arguments, the implied empty configuration is considered to be the default provider configuration.
https://www.terraform.io/docs/configuration/providers.html#alias-multiple-provider-instances



86)	Which of the following is considered a Terraform plugin?
12/26/2022 – by Mod_GuideK0 
Which of the following is considered a Terraform plugin?
A. Terraform language
B. Terraform tooling
C. Terraform logic
D. Terraform provider
HIDE ANSWERS
Correct Answer: D
Explanation/Reference:
Explanation:
Terraform is built on a plugin-based architecture. All providers and provisioners that are used in Terraform configurations are plugins, even the core types such as AWS and Heroku. Users of Terraform are able to write new plugins in order to support new functionality in Terraform.
https://www.terraform.io/docs/plugins/basics.html

87)	What should you do?
12/26/2022 – by Mod_GuideK0 
Your team has started using terraform OSS in a big way , and now wants to deploy multi region deployments (DR) in aws using the same terraform files . You want to deploy the same infra (VPC,EC2 …) in both us-east-1 ,and us-west-2 using the same script , and then peer the VPCs across both the regions to enable DR traffic. But , when you run your script , all resources are getting created in only the default provider region. What should you do? Your provider setting is as below – # The default provider configuration provider “aws” { region = “us-east-1” }
A. No way to enable this via a single script . Write 2 different scripts with different default providers in the 2 scripts , one for us-east , another for us-west.
B. Create a list of regions , and then use a for-each to iterate over the regions , and create the same resources ,one after the one , over the loop.
C. Use provider alias functionality , and add another provider for us-west region . While creating the resources using the tf script , reference the appropriate provider (using the alias).
D. Manually create the DR region , once the Primary has been created , since you are using terraform OSS , and multi region deployment is only available in Terraform Enterprise.
HIDE ANSWERS
Correct Answer: C
Explanation/Reference:
Explanation:
You can optionally define multiple configurations for the same provider, and select which one to use on a per-resource or per-module basis. The primary reason for this is to support multiple regions for a cloud platform; other examples include targeting multiple Docker hosts, multiple Consul hosts, etc.
To include multiple configurations for a given provider, include multiple provider blocks with the same provider name, but set the alias meta-argument to an alias name to use for each additional configuration. For example:
# The default provider configuration provider “aws” { region = “us-east-1”
} # Additional provider configuration for west coast region provider “aws” { alias = “west” region = “us-west-2”
}
https://www.terraform.io/docs/configuration/providers.html

88)	What are the options for him to resolve this slowness?
12/26/2022 – by Mod_GuideK0 
Talal is a DevOps engineer and he has deployed the production infrastructure using Terraform. He is using a very large configuration file to maintain and update the actual infrastructure. As the infrastructure have grown to a very complex and large, he has started experiencing slowness when he run runs terraform plan. What are the options for him to resolve this slowness?
A. Use -refresh=true flag as well as the -target flag with terraform plan in order to work around this.
B. Run terraform refresh every time before running terraform plan.
C. Break large configurations into several smaller configurations that can each be independently applied.
D. Use -refresh=false flag as well as the -target flag with terraform plan in order to work around this.
HIDE ANSWERS
Correct Answer: CD
Explanation/Reference:
Explanation:
For larger infrastructures, querying every resource is too slow. Many cloud providers do not provide APIs to query multiple resources at once, and the round trip time for each resource is hundreds of milliseconds. On top of this, cloud providers almost always have API rate limiting so Terraform can only request a certain number of resources in a period of time. Larger users of Terraform make heavy use of the -refresh=false flag as well as the -target flag in order to work around this. In these scenarios, the cached state is treated as the record of truth.
Although ‘Use -refresh=false flag as well as the -target flag with terraform plan in order to work around this.’ is a solution, but its not always recommended. Instead of using -target as a means to operate on isolated portions of very large configurations, prefer instead to break large configurations into several smaller configurations that can each be independently applied. Data sources can be used to access information about resources created in other configurations, allowing a complex system architecture to be broken down into more manageable parts that can be updated independently.
Option ‘Run terraform refresh every time before running terraform plan.’ and ‘Use -refresh=true flag as well as the -target flag with terraform plan in order to work around this.’ is not correct because in both the cases terraform will query every resources of the infrastructure.

89)	Named workspaces are not a suitable isolation mechanism for strong separation between staging and production?
12/26/2022 – by Mod_GuideK1 
Named workspaces are not a suitable isolation mechanism for strong separation between staging and production?
A. True
B. False
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
Organizations commonly want to create a strong separation between multiple deployments of the same infrastructure serving different development stages (e.g. staging vs. production) or different internal teams. In this case, the backend used for each deployment often belongs to that deployment, with different credentials and access controls. Named workspaces are not a suitable isolation mechanism for this scenario.
https://www.terraform.io/docs/state/workspaces.html#when-to-use-multiple-workspaces


90)	Select the feature below that best completes the sentence:
12/26/2022 – by Mod_GuideK0 
Select the feature below that best completes the sentence:
The following list represents the different types of __________ available in Terraform.
1. max
2. min
3. join
4. replace
5. list
6. length
7. range
A. Backends
B. Data sources
C. Named values
D. Functions
HIDE ANSWERS
Correct Answer: D
Explanation/Reference:
Explanation:
The Terraform language includes a number of built-in functions that you can call from within expressions to transform and combine values. The Terraform language does not support user-defined functions, and only the functions built into the language are available for use.
https://www.terraform.io/docs/configuration/functions.html

91)	Valarie has created a database instance in AWS and for ease of use is outputting the value of the database password with the following code.
12/26/2022 – by Mod_GuideK0 
Valarie has created a database instance in AWS and for ease of use is outputting the value of the database password with the following code. Valarie wants to hide the output value in the CLI after terraform apply that’s why she has used sensitive parameter.
1. output “db_password” {
2. value = local.db_password
3. sensitive = true
4. }
Since sensitive is set to true, will the value associated with db password be available in plain-text in the state file for everyone to read?
A. Yes
B. No
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
Outputs can be marked as containing sensitive material by setting the sensitive attribute to true, like this: output “sensitive” { sensitive = true value = VALUE
} When outputs are displayed on-screen following a terraform apply or terraform refresh, sensitive outputs are redacted, with <sensitive> displayed in place of their value.
Limitations of Sensitive Outputs
The values of sensitive outputs are still stored in the Terraform state, and available using the terraform output command, so cannot be relied on as a sole means of protecting values.
Sensitivity is not tracked internally, so if the output is interpolated in another module into a resource, the value will be displayed.

92)	Select all features which are exclusive to Terraform Enterprise.
12/26/2022 – by Mod_GuideK2 
Select all features which are exclusive to Terraform Enterprise. (Select Three)
A. Sentinel
B. Cost Estimation
C. Audit Logs
D. Clustering
E. SAML/SSO
HIDE ANSWERS
Correct Answer: CDE
Explanation/Reference:
Explanation:
Sentinel and Cost Estimation are also available in Terraform Cloud
https://www.hashicorp.com/products/terraform/pricing/


93)	Which of the following connection types are supported by the remote-exec provisioner?
12/26/2022 – by Mod_GuideK0 
Which of the following connection types are supported by the remote-exec provisioner? (select two)
A. WinRM
B. UDP
C. SMB
D. RDP
E. ssh
HIDE ANSWERS
Correct Answer: AE
Explanation/Reference:
Explanation:
The remote-exec provisioner invokes a script on a remote resource after it is created. The remoteexec provisioner supports both ssh and winrm type connections. remote-exec connection types – * ssh on Linux * winrm on Windows
https://www.terraform.io/docs/provisioners/remote-exec.html


94)	What can you do to efficiently enforce this?
12/26/2022 – by Mod_GuideK0 
Your team lead does not trust the junior terraform engineers who now have access to the git repo .
So , he wants you to have some sort of a checking layer , whereby , you can ensure that the juniors will not create any non-compliant resources that might lead to a security audit failure in future. What can you do to efficiently enforce this?
A. Create a design /security document (in PDF) and share to the team , and ask them to always follow that document , and never deviate from it.
B. Since your team is using Hashicorp Terraform Enterprise Edition , enable Sentinel , and write Policy-As-Code rules that will check for non-compliant resource provisioning , and prevent/report them.
C. Use Terraform OSS Sentinel Lite version , which will save cost , since there is no charge for OSS , but it can still check for most non-compliant rules using Policy-As-Code.
D. Create a git master branch , and implement PR . Every change needs to be reviewed by you , before being merged to the master branch.
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
Sentinel is an embedded policy-as-code framework integrated with the HashiCorp Enterprise products. It enables fine-grained, logic-based policy decisions, and can be extended to use information from external sources.
https://www.terraform.io/docs/cloud/sentinel/index.html

95)	What will be the datatype of the variable?
12/26/2022 – by Mod_GuideK0 
A variable az has the following default value. What will be the datatype of the variable? az=[“us-west-1a”,”us-east-1a”]
A. Object
B. List
C. Map
D. String
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:

96)	Using multi-cloud and provider-agnostic tools provides which of the following benefits?
12/26/2022 – by Mod_GuideK0 
Using multi-cloud and provider-agnostic tools provides which of the following benefits?
A. Operations teams only need to learn and manage a single tool to manage infrastructure, regardless of where the infrastructure is deployed.
B. Increased risk due to all infrastructure relying on a single tool for management.
C. Can be used across major cloud providers and VM hypervisors.
D. Slower provisioning speed allows the operations team to catch mistakes before they are applied.
HIDE ANSWERS
Correct Answer: AC
Explanation/Reference:
Explanation:
Using a tool like Terraform can be advantageous for organizations deploying workloads across multiple public and private cloud environments. Operations teams only need to learn a single tool, single language, and can use the same tooling to enable a DevOps-like experience and workflows.


97)	What is the correct option/way to do that?
12/26/2022 – by Mod_GuideK0 
Your team uses terraform OSS . You have created a number of resuable modules for important , independent network components that you want to share with your team to enhance consistency .
What is the correct option/way to do that?
A. Terraform modules cannot be shared in OSS version . Each developer needs to maintain their own modules and leverage them in the main tf file.
B. Upload your modules with proper versioning in the terraform public module registry . Terraform OSS is directly integrated with the public module registry , and can reference the modules from the code in the main tf file.
C. Terraform module sharing is only available in Enterprise version via terraform private module registry , so no way to enable it in OSS version.
D. Store your modules in a NAS/ shared file server , and ask your team members to directly reference the code from there. This is the only viable option in terraform OSS ,which is better than individually maintaining module versions for every developer.
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
Software development encourages code reuse through reusable artifacts, such as libraries, packages and modules. Most programming languages enable developers to package and publish these reusable components and make them available on a registry or feed. For example, Python has Python Package Index and PowerShell has PowerShell Gallery.
For Terraform users, the Terraform Registry enables the distribution of Terraform modules, which are reusable configurations. The Terraform Registry acts as a centralized repository for module sharing, making modules easier to discover and reuse.
The Registry is available in two variants:
* Public Registry houses official Terraform providers — which are services that interact with an API to expose and manage a specific resource — and community-contributed modules.
* Private Registry is available as part of the Terraform Cloud, and can host modules internally within an organization.
https://www.terraform.io/docs/registry/index.html



98)	Which one is the right way to import a local module names consul?
12/26/2022 – by Mod_GuideK0 
Which one is the right way to import a local module names consul?
A. module “consul” { source = “consul”}
B. module “consul” { source = “./consul”}
C. module “consul” { source = “../consul”}
D. module “consul” { source = “module/consul”}
HIDE ANSWERS
Correct Answer: BC
Explanation/Reference:
Explanation:
A local path must begin with either ./ or ../ to indicate that a local path is intended, to distinguish from a module registry address. module “consul” { source = “./consul”
}


99)	How will you use it for provisioning infrastructure?
12/26/2022 – by Mod_GuideK0 
You have created a custom variable definition file my_vars.tfvars. How will you use it for provisioning infrastructure?
A. terraform apply -var-state-file =”my_vars.tfvars”
B. terraform apply var-file=”my_vars.tfvars”
C. terraform plan -var-file=”my_vars.tfvar”
D. terraform apply -var-file=”my_vars.tfvars”
HIDE ANSWERS
Correct Answer: D
Explanation/Reference:
Explanation:
To set lots of variables, it is more convenient to specify their values in a variable definitions file (with a filename ending in either .tfvars or .tfvars.json) and then specify that file on the command line with -var-file: terraform apply -varfile=” my_vars.tfvars”
https://www.terraform.io/docs/configuration/variables.html#variable-definitions-tfvars-files



100)	What is a better approach to dealing with this?
12/26/2022 – by Mod_GuideK0 
John is writing a module and within the module, there are multiple places where he has to use the same conditional expression but he wants to avoid repeating the same values or expressions multiple times in a configuration,. What is a better approach to dealing with this?
A. Local Values
B. Expressions
C. Functions
D. Variables
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
A local value assigns a name to an expression, allowing it to be used multiple times within a module without repeating it.
https://www.terraform.io/docs/configuration/locals.html

101-200

101)	Which of the following is not a supported backend type?
12/26/2022 – by Mod_GuideK0 
A “backend” in Terraform determines how state is loaded and how an operation such as apply is executed. Which of the following is not a supported backend type?
A. Terraform enterprise
B. Consul
C. Github
D. S3
E. Artifactory
HIDE ANSWERS
Correct Answer: C
Explanation/Reference:
Explanation:
Github is not a supported backend type.
https://www.terraform.io/docs/backends/types/index.html
102)	A single terraform resource file that defines an aws_instance resource can simple be renamed to azurerm_virtual_machine in order to switch cloud providers
12/26/2022 – by Mod_GuideK0 
A single terraform resource file that defines an aws_instance resource can simple be renamed to azurerm_virtual_machine in order to switch cloud providers
A. True
B. False
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
Providers usually require some configuration of their own to specify endpoint URLs, regions, authentication settings.
Providers Initialization can be done by either explicitly via a provider block or by adding a resource from that provide
https://www.terraform.io/docs/configuration/providers.html

103)	What does this infer?
12/26/2022 – by Mod_GuideK0 
After executing a terraform apply, you notice that a resource has a tilde (~) next to it. What does this infer?
A. The resource will be updated in place.
B. The resource will be created.
C. Terraform can’t determine how to proceed due to a problem with the state file.
D. The resource will be destroyed and recreated.
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
The prefix -/+ means that Terraform will destroy and recreate the resource, rather than updating it inplace.
The prefix ~ means that some attributes and resources can be updated in-place.
$ terraform apply aws_instance.example: Refreshing state… [id=i-0bbf06244e44211d1] An execution plan has been generated and is shown below.
Resource actions are indicated with the following symbols:
-/+ destroy and then create replacement
Terraform will perform the following actions:
# aws_instance.example must be replaced
-/+ resource “aws_instance” “example” {
~ ami = “ami-2757f631” -> “ami-b374d5a5” # forces replacement
~ arn = “arn:aws:ec2:us-east-1:130490850807:instance/i-0bbf06244e44211d1” ->
(known after apply) ~ associate_public_ip_address = true -> (known after apply) ~ availability_zone = “us-east-1c” -> (known after apply) ~ cpu_core_count = 1 -> (known after apply) ~ cpu_threads_per_core = 1 -> (known after apply)
– disable_api_termination = false -> null
– ebs_optimized = false -> null get_password_data = false + host_id = (known after apply) ~ id = “i-0bbf06244e44211d1” -> (known after apply) ~ instance_state = “running” -> (known after apply) instance_type = “t2.micro” ~ ipv6_address_count = 0 -> (known after apply) ~ ipv6_addresses = [] -> (known after apply) + key_name = (known after apply)
– monitoring = false -> null
+ network_interface_id = (known after apply)
+ password_data = (known after apply)
+ placement_group = (known after apply)
~ primary_network_interface_id = “eni-0f1ce5bdae258b015” -> (known after apply) ~ private_dns = “ip-172-31-61-141.ec2.internal” -> (known after apply) ~ private_ip = “172.31.61.141” -> (known after apply) ~ public_dns = “ec2-54-166-19-244.compute-1.amazonaws.com” -> (known after apply) ~ public_ip = “54.166.19.244” -> (known after apply) ~ security_groups = [
– “default”,
] -> (known after apply) source_dest_check = true ~ subnet_id = “subnet-1facdf35” -> (known after apply) ~ tenancy = “default” -> (known after apply) ~ volume_tags = {} -> (known after apply) ~ vpc_security_group_ids = [
– “sg-5255f429”,
] -> (known after apply)
– credit_specification {
– cpu_credits = “standard” -> null
}
+ ebs_block_device {
+ delete_on_termination = (known after apply)
+ device_name = (known after apply)
+ encrypted = (known after apply)
+ iops = (known after apply)
+ snapshot_id = (known after apply)
+ volume_id = (known after apply)
+ volume_size = (known after apply)
+ volume_type = (known after apply)
}
+ ephemeral_block_device {
+ device_name = (known after apply)
+ no_device = (known after apply)
+ virtual_name = (known after apply)
}
+ network_interface {
+ delete_on_termination = (known after apply)
+ device_index = (known after apply)
+ network_interface_id = (known after apply)
}
~ root_block_device {
~ delete_on_termination = true -> (known after apply)
~ iops = 100 -> (known after apply)
~ volume_id = “vol-0079e485d9e28a8e5” -> (known after apply)
~ volume_size = 8 -> (known after apply)
~ volume_type = “gp2” -> (known after apply)
}}
Plan: 1 to add, 0 to change, 1 to destroy.

104)	Given the Terraform configuration below, in which order will the resources be created?
12/26/2022 – by Mod_GuideK0 
Given the Terraform configuration below, in which order will the resources be created?
1. resource “aws_instance” “web_server”
2. {
3. ami = “ami-b374d5a5”
4. instance_type = “t2.micro”
5. }
6. resource “aws_eip” “web_server_ip”
7. {
8. vpc = true instance = aws_instance.web_server.id
9. }
A. aws_eip will be created first aws_instance will be created second
B. aws_eip will be created first aws_instance will be created second
C. Resources will be created simultaneously
D. aws_instance will be created first aws_eip will be created second
HIDE ANSWERS
Correct Answer: D
Explanation/Reference:
Explanation:
Implicit and Explicit Dependencies
By studying the resource attributes used in interpolation expressions, Terraform can automatically infer when one resource depends on another. In the example above, the reference to aws_instance.web_server.id creates an implicit dependency on the aws_instance named web_server.
Terraform uses this dependency information to determine the correct order in which to create the different resources.
# Example of Implicit Dependency resource “aws_instance” “web_server” { ami = “ami-b374d5a5” instance_type = “t2.micro”
} resource “aws_eip” “web_server_ip” { vpc = true instance = aws_instance.web_server.id
}I n the example above, Terraform knows that the aws_instance must be created before the aws_eip.
Implicit dependencies via interpolation expressions are the primary way to inform Terraform about these relationships, and should be used whenever possible.
Sometimes there are dependencies between resources that are not visible to Terraform. The depends_on argument is accepted by any resource and accepts a list of resources to create explicit dependencies for.
For example, perhaps an application we will run on our EC2 instance expects to use a specific Amazon S3 bucket, but that dependency is configured inside the application code and thus not visible to Terraform. In that case, we can use depends_on to explicitly declare the dependency:
# Example of Explicit Dependency
# New resource for the S3 bucket our application will use resource “aws_s3_bucket” “example” { bucket = “terraform-getting-started-guide” acl = “private”
} # Change the aws_instance we declared earlier to now include “depends_on” resource “aws_instance” “example” { ami = “ami-2757f631” instance_type = “t2.micro” # Tells Terraform that this EC2 instance must be created only after the # S3 bucket has been created. depends_on = [aws_s3_bucket.example]
}
https://learn.hashicorp.com/terraform/getting-started/dependencies.html

105)	What can you do to enable this setting?
12/26/2022 – by Mod_GuideK0 
You have written a terraform IaC script which was working till yesterday , but is giving some vague error from today , which you are unable to understand . You want more detailed logs that could potentially help you troubleshoot the issue , and understand the root cause. What can you do to enable this setting? Please note , you are using terraform OSS.
A. Terraform OSS can push all its logs to a syslog endpoint. As such, you have to set up the syslog sink, and enable TF_LOG_PATH env variable to the syslog endpoint and all logs will automatically start streaming.
B. Detailed logs are not available in terraform OSS, except the crash message. You need to upgrade to terraform enterprise for this point.
C. Enable the TF_LOG_PATH to the log sink file location, and logging output will automatically be stored there.
D. Enable TF_LOG to the log level DEBUG, and then set TF_LOG_PATH to the log sink file location.
Terraform debug logs will be dumped to the sink path, even in terraform OSS.
HIDE ANSWERS
Correct Answer: D
Explanation/Reference:
Explanation:
Terraform has detailed logs which can be enabled by setting the TF_LOG environment variable to any value. This will cause detailed logs to appear on stderr.
You can set TF_LOG to one of the log levels TRACE, DEBUG, INFO, WARN or ERROR to change the verbosity of the logs. TRACE is the most verbose and it is the default if TF_LOG is set to something other than a log level name.
To persist logged output you can set TF_LOG_PATH in order to force the log to always be appended to a specific file when logging is enabled. Note that even when TF_LOG_PATH is set, TF_LOG must be set in order for any logging to be enabled.

106)	Why is this happening?
12/26/2022 – by Mod_GuideK0 
You have configured an Auto Scaling group in AWS to automatically scale the number of instances behind a load balancer based on the instances CPU utilization. The instances are configured using a Launch Configuration. You have observed that the Auto Scaling group doesn’t successfully scale when you apply changes that require replacing the Launch Configuration. Why is this happening?
A. You need to configure an explicit dependency for the Auto Scaling group using the depends_on meta-parameter.
B. You need to configure an explicit dependency for the Launch Configuration using the depends_on meta-parameter.
C. You need to configure the Auto Scaling group’s create_before_destroy meta-parameter.
D. You need to configure the Launch Configuration’s create_before_destroy meta-parameter.
HIDE ANSWERS
Correct Answer: D
Explanation/Reference:
Explanation:
https://www.terraform.io/docs/providers/aws/r/launch_configuration.html#using-withautoscalinggroups

107)	When using parent/child modules to deploy infrastructure, how would you export a value from one module to import into another module.
12/26/2022 – by Mod_GuideK0 
When using parent/child modules to deploy infrastructure, how would you export a value from one module to import into another module.
For example, a module dynamically deploys an application instance or virtual machine, and you need the IP address in another module to configure a related DNS record in order to reach the newly deployed application.
A. Export the value using terraform export and input the value using terraform input.
B. Configure the pertinent provider’s configuration with a list of possible IP addresses to use.
C. Configure an output value in the application module in order to use that value for the DNS module.
D. Preconfigure the IP address as a parameter in the DNS module.
HIDE ANSWERS
Correct Answer: C
Explanation/Reference:
Explanation:
Output values are like the return values of a Terraform module, and have several uses:
* A child module can use outputs to expose a subset of its resource attributes to a parent module.
* A root module can use outputs to print certain values in the CLI output after running terraform apply.
* When using remote state, root module outputs can be accessed by other configurations via a terraform_remote_state data source.
https://www.terraform.io/docs/configuration/outputs.html

108)	When writing Terraform code, HashiCorp recommends that you use how many spaces between each nesting level?
12/26/2022 – by Mod_GuideK0 
When writing Terraform code, HashiCorp recommends that you use how many spaces between each nesting level?
A. 0
B. 1
C. 2
D. 4
HIDE ANSWERS
Correct Answer: C
Explanation/Reference:
Explanation:
The Terraform parser allows you some flexibility in how you lay out the elements in your configuration files, but the Terraform language also has some idiomatic style conventions which we recommend users always follow for consistency between files and modules written by different teams. Automatic source code formatting tools may apply these conventions automatically.
Indent two spaces for each nesting level.
When multiple arguments with single-line values appear on consecutive lines at the same nesting level, align their equals signs: ami = “abc123” instance_type = “t2.micro” When both arguments and blocks appear together inside a block body, place all of the arguments together at the top and then place nested blocks below them. Use one blank line to separate the arguments from the blocks.
Use empty lines to separate logical groups of arguments within a block.
For blocks that contain both arguments and “meta-arguments” (as defined by the Terraform language semantics), list meta-arguments first and separate them from other arguments with one blank line. Place meta-argument blocks last and separate them from other blocks with one blank line. resource “aws_instance” “example” { count = 2 # meta-argument first ami = “abc123” instance_type = “t2.micro” network_interface { # …
}l ifecycle { # meta-argument block last create_before_destroy = true
} Top-level blocks should always be separated from one another by one blank line. Nested blocks should also be separated by blank lines, except when grouping together related blocks of the same type (like multiple provisioner blocks in a resource).
Avoid separating multiple blocks of the same type with other blocks of a different type, unless the block types are defined by semantics to form a family. (For example: root_block_device, ebs_block_device and ephemeral_block_device on aws_instance form a family of block types describing AWS block devices, and can therefore be grouped together and mixed.)

109)	What should be done to avoid this?
12/26/2022 – by Mod_GuideK0 
Your developers are facing a lot of problem while writing complex expressions involving difficult interpolations . They have to run the terraform plan every time and check whether there are errors , and also check terraform apply to print the value as a temporary output for debugging purposes.
What should be done to avoid this?
A. Use terraform console command to have an interactive UI with full access to the underlying terraform state to run your interpolations , and debug at real-time.
B. Add a breakpoint in your code, using the watch keyword , and output the value to console for temporary debugging.
C. Use terraform zipmap function , it will be able to easily do the interpolations without complex code.
D. Use terraform console command to have an interactive UI , but you can only use it with local state , and it does not work with remote state.
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
The terraform console command provides an interactive console for evaluating expressions. This is useful for testing interpolations before using them in configurations, and for interacting with any values currently saved in state.
https://www.terraform.io/docs/commands/console.html
110)	Which of the following way your resources would be destroyed?
12/26/2022 – by Mod_GuideK0 
You wanted to destroy some of the dependent resources from real infrastructure. You choose to delete those resources from your configuration file and run terraform plan and then apply. Which of the following way your resources would be destroyed?
A. Terraform can still determine the correct order for destruction from the state even when you delete one or more items from the configuration.
B. Those would be destroyed in the order in which they were written in the configuration file previously before you have deleted them from configuration file.
C. The resource will be destructed in random order as you have already deleted them from configuration.
D. You can not destroy resources by deleting them from configuration file and running plan and apply.
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
Terraform typically uses the configuration to determine dependency order. However, when you delete a resource from a Terraform configuration, Terraform must know how to delete that resource.
Terraform can see that a mapping exists for a resource not in your configuration and plan to destroy.
However, since the configuration no longer exists, the order cannot be determined from the configuration alone.
To ensure correct operation, Terraform retains a copy of the most recent set of dependencies within the state. Now Terraform can still determine the correct order for destruction from the state when you delete one or more items from the configuration.


111)	State is a requirement for Terraform to function
12/26/2022 – by Mod_GuideK0 
State is a requirement for Terraform to function
A. True
B. False
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
State is a necessary requirement for Terraform to function. It is often asked if it is possible for Terraform to work without state, or for Terraform to not use state and just inspect cloud resources on every run.
Purpose of Terraform State
State is a necessary requirement for Terraform to function. It is often asked if it is possible for Terraform to work without state, or for Terraform to not use state and just inspect cloud resources on every run. This page will help explain why Terraform state is required.
As you’ll see from the reasons below, state is required. And in the scenarios where Terraform may be able to get away without state, doing so would require shifting massive amounts of complexity from one place (state) to another place (the replacement concept).
1. Mapping to the Real World
Terraform requires some sort of database to map Terraform config to the real world. When you have a resource resource “aws_instance” “foo” in your configuration, Terraform uses this map to know that instance i- abcd1234 is represented by that resource.
For some providers like AWS, Terraform could theoretically use something like AWS tags. Early prototypes of Terraform actually had no state files and used this method. However, we quickly ran into problems. The first major issue was a simple one: not all resources support tags, and not all cloud providers support tags.
Therefore, for mapping configuration to resources in the real world, Terraform uses its own state structure.
2. Metadata
Alongside the mappings between resources and remote objects, Terraform must also track metadata such as resource dependencies.
Terraform typically uses the configuration to determine dependency order. However, when you delete a resource from a Terraform configuration, Terraform must know how to delete that resource.
Terraform can see that a mapping exists for a resource not in your configuration and plan to destroy.
However, since the configuration no longer exists, the order cannot be determined from the configuration alone.
To ensure correct operation, Terraform retains a copy of the most recent set of dependencies within the state. Now Terraform can still determine the correct order for destruction from the state when you delete one or more items from the configuration.
One way to avoid this would be for Terraform to know a required ordering between resource types.
For example, Terraform could know that servers must be deleted before the subnets they are a part of. The complexity for this approach quickly explodes, however: in addition to Terraform having to understand the ordering semantics of every resource for every cloud, Terraform must also understand the ordering across providers.
Terraform also stores other metadata for similar reasons, such as a pointer to the provider configuration that was most recently used with the resource in situations where multiple aliased providers are present.
3. Performance
In addition to basic mapping, Terraform stores a cache of the attribute values for all resources in the state. This is the most optional feature of Terraform state and is done only as a performance improvement.
When running a terraform plan, Terraform must know the current state of resources in order to effectively determine the changes that it needs to make to reach your desired configuration.
For small infrastructures, Terraform can query your providers and sync the latest attributes from all your resources. This is the default behavior of Terraform: for every plan and apply, Terraform will sync all resources in your state.
For larger infrastructures, querying every resource is too slow. Many cloud providers do not provide APIs to query multiple resources at once, and the round trip time for each resource is hundreds of milliseconds. On top of this, cloud providers almost always have API rate limiting so Terraform can only request a certain number of resources in a period of time. Larger users of Terraform make heavy use of the -refresh=false flag as well as the -target flag in order to work around this. In these scenarios, the cached state is treated as the record of truth.
4. Syncing
In the default configuration, Terraform stores the state in a file in the current working directory where Terraform was run. This is okay for getting started, but when using Terraform in a team it is important for everyone to be working with the same state so that operations will be applied to the same remote objects.
Remote state is the recommended solution to this problem. With a fully-featured state backend, Terraform can use remote locking as a measure to avoid two or more different users accidentally running Terraform at the same time, and thus ensure that each Terraform run begins with the most recent updated state.

112)	Given the below resource configuration – resource “aws_instance” “web” { # … count = 4 } What does the terraform resource address aws_instance.web refer to?
12/26/2022 – by Mod_GuideK0 
Given the below resource configuration – resource “aws_instance” “web” { # … count = 4 } What does the terraform resource address aws_instance.web refer to?
A. It refers to all 4 web instances , together , for further individual segregation , indexing is required , with a 0 based index.
B. It refers to the last web EC2 instance , as by default , if no index is provided , the last / N-1 index is used.
C. It refers to the first web EC2 instance out of the 4 ,as by default , if no index is provided , the first / 0th index is used.
D. The above will result in a syntax error , as it is not syntactically correct . Resources defined using count , can only be referenced using indexes.
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
A Resource Address is a string that references a specific resource in a larger infrastructure. An
address is made up of two parts:
[module path][resource spec]
Module path:
A module path addresses a module within the tree of modules. It takes the form: module.A.module.B.module.C…
Multiple modules in a path indicate nesting. If a module path is specified without a resource spec, the address applies to every resource within the module. If the module path is omitted, this
addresses the root module.
Given a Terraform config that includes: resource “aws_instance” “web” { # … count = 4
} An address like this: aws_instance.web[3] Refers to only the last instance in the config, and an address like this: aws_instance.web Refers to all four “web” instances.
https://www.terraform.io/docs/internals/resource-addressing.html


113)	What is a downside to using the Vault provider to read secrets from Vault?
12/26/2022 – by Mod_GuideK0 
What is a downside to using the Vault provider to read secrets from Vault?
A. Secrets are persisted to the state file and plans.
B. Terraform and Vault must be running on the same version.
C. Terraform and Vault must be running on the same physical host.
D. Terraform requires a unique auth method to work with Vault.
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
The Vault provider allows Terraform to read from, write to, and configure Hashicorp Vault.
Interacting with Vault from Terraform causes any secrets that you read and write to be persisted in both Terraform’s state file and in any generated plan files. For any Terraform module that reads or writes Vault secrets, these files should be treated as sensitive and protected accordingly.

114)	Which of the following actions are performed during a terraform init?
12/26/2022 – by Mod_GuideK0 
Which of the following actions are performed during a terraform init?
A. Initializes downloaded and/or installed providers
B. Initializes the backend configuration
C. Provisions the declared resources in your configuration
D. Download the declared providers which are supported by HashiCorp
HIDE ANSWERS
Correct Answer: ABD
Explanation/Reference:
Explanation:
The terraform init command is used to initialize a working directory containing Terraform configuration files. This is the first command that should be run after writing a new Terraform configuration or cloning an existing one from version control. It is safe to run this command multiple times.
This command is always safe to run multiple times, to bring the working directory up to date with changes in the configuration. Though subsequent runs may give errors, this command will never delete your existing configuration or state. terraform init command does – * Copy a Source Module * Backend Initialization * Child Module Installation * Plugin Installation
https://www.terraform.io/docs/commands/init.html

115)	What can you do to ensure that all existing is managed by Terraform moving forward without interruption to existing services?
12/26/2022 – by Mod_GuideK0 
Your organization has moved to AWS and has manually deployed infrastructure using the console.
Recently, a decision has been made to standardize on Terraform for all deployments moving forward.
What can you do to ensure that all existing is managed by Terraform moving forward without interruption to existing services?
A. Submit a ticket to AWS and ask them to export the state of all existing resources and use terraform import to import them into the state file.
B. Delete the existing resources and recreate them using new a Terraform configuration so Terraform can manage them moving forward.
C. Resources that are manually deployed in the AWS console cannot be imported by Terraform.
D. Using terraform import, import the existing infrastructure into your Terraform state.
HIDE ANSWERS
Correct Answer: D
Explanation/Reference:
Explanation:
Terraform is able to import existing infrastructure. This allows us take resources we’ve created by some other means (i.e. via console) and bring it under Terraform management.
This is a great way to slowly transition infrastructure to Terraform.
The terraform import command is used to import existing infrastructure.
To import a resource, first write a resource block for it in our configuration, establishing the name by which it will be known to Terraform.
Example: resource “aws_instance” “import_example” {
# …instance configuration…
}
Now terraform import can be run to attach an existing instance to this resource configuration.
$ terraform import aws_instance.import_example i-03efafa258104165f aws_instance.import_example: Importing from ID “i-03efafa258104165f”… aws_instance.import_example: Import complete! Imported aws_instance (ID: i- 03efafa258104165f) aws_instance.import_example: Refreshing state… (ID: i-03efafa258104165f) Import successful! The resources that were imported are shown above. These resources are now in your Terraform state and will henceforth be managed by Terraform.
This command locates the AWS instance with ID i-03efafa258104165f (which has been created outside Terraform) and attaches its existing settings, as described by the EC2 API, to the name aws_instance.import_example in the Terraform state.


116)	Consider the following Terraform 0.
12/26/2022 – by Mod_GuideK0 
Consider the following Terraform 0.12 configuration snippet:
1. variable “vpc_cidrs” {
2. type = map
3. default = {
4. us-east-1 = “10.0.0.0/16”
5. us-east-2 = “10.1.0.0/16”
6. us-west-1 = “10.2.0.0/16”
7. us-west-2 = “10.3.0.0/16”
8. }
9. }
10.
11. resource “aws_vpc” “shared” {
12. cidr_block = _____________
13. }
How would you define the cidr_block for us-east-1 in the aws_vpc resource using a variable?
A. var.vpc_cidrs.0
B. vpc_cidrs[“us-east-1”]
C. var.vpc_cidrs[“us-east-1”]
D. var.vpc_cidrs[0]
HIDE ANSWERS
Correct Answer: C
Explanation/Reference:
Explanation:

117)	What resource dependency information is stored in Terraform’s state?
12/26/2022 – by Mod_GuideK0 
What resource dependency information is stored in Terraform’s state?
A. Only implicit dependencies are stored in state.
B. Both implicit and explicit dependencies are stored in state.
C. Only explicit dependencies are stored in state.
D. No dependency information is stored in state.
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
Terraform state captures all dependency information, both implicit and explicit. One purpose for state is to determine the proper order to destroy resources. When resources are created all of their dependency information is stored in the state. If you destroy a resource with dependencies, Terraform can still determine the correct destroy order for all other resources because the dependencies are stored in the state.
https://www.terraform.io/docs/state/purpose.html#metadata

118)	From the answers below, select the advantages of using Infrastructure as Code.
12/26/2022 – by Mod_GuideK0 
From the answers below, select the advantages of using Infrastructure as Code.
A. Provide a codified workflow to develop customer-facing applications.
B. Safely test modifications using a “dry run” before applying any actual changes.
C. Easily integrate with application workflows (GitLab Actions, Azure DevOps, CI/CD tools).
D. Easily change and update existing infrastructure.
E. Provide reusable modules for easy sharing and collaboration.
HIDE ANSWERS
Correct Answer: BCDE
Explanation/Reference:
Explanation:
Infrastructure as Code is not used to develop applications, but it can be used to help deploy or provision those applications to a public cloud provider or on-premises infrastructure.
All of the others are benefits to using Infrastructure as Code over the traditional way of managing infrastructure, regardless if it’s public cloud or on-premises.


119)	Which of the following values provides the MOST verbose logging?
12/26/2022 – by Mod_GuideK0 
After running into issues with Terraform, you need to enable verbose logging to assist with troubleshooting the error. Which of the following values provides the MOST verbose logging?
A. ERROR
B. INFO
C. WARN
D. TRACE
E. DEBUG
HIDE ANSWERS
Correct Answer: D
Explanation/Reference:
Explanation:
Terraform has detailed logs that can be enabled by setting the TF_LOG environment variable to any value. This will cause detailed logs to appear on stderr.
You can set TF_LOG to one of the log levels TRACE, DEBUG, INFO, WARN or ERROR to change the verbosity of the logs. TRACE is the most verbose and it is the default if TF_LOG is set to something other than a log level name.
Examples: export TF_LOG=DEBUG export TF_LOG=TRACE
Topic 4, Exam Set D

120)	You can migrate the Terraform backend but only if there are no resources currently being managed.
12/26/2022 – by Mod_GuideK1 
You can migrate the Terraform backend but only if there are no resources currently being managed.
A. False
B. True
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
If you need to migrate to another backend, such as Terraform Cloud, so you can continue managing it. By migrating your Terraform state, you can hand off infrastructure without de-provisioning anything.
https://www.terraform.io/docs/cloud/migrate/index.html

121)	Complete the following sentence:
12/26/2022 – by Mod_GuideK0 
Complete the following sentence:
For local state, the workspaces are stored directly in a ___________.
A. a file called terraform.tfstate.backup
B. directory called terraform.workspaces.tfstate
C. a file called terraform.tfstate
D. directory called terraform.tfstate.d
HIDE ANSWERS
Correct Answer: D
Explanation/Reference:
Explanation:
For local state, Terraform stores the workspace states in a directory called terraform.tfstate.d.
https://www.terraform.io/docs/state/workspaces.html#workspace-internals

122)	Terraform Enterprise currently supports running under which the following operating systems?
12/26/2022 – by Mod_GuideK0 
Terraform Enterprise currently supports running under which the following operating systems?
A. Ubuntu
B. Amazon Linux
C. Debian
D. CentOS
E. Red Hat Enterprise Linux
F. Oracle Linux
HIDE ANSWERS
Correct Answer: ABCDEF
Explanation/Reference:
Explanation:
Terraform Enterprise runs on Linux instances, and you must prepare a running Linux instance for Terraform Enterprise before running the installer. You will start and manage this instance like any other server.
Terraform Enterprise currently supports running under the following operating systems:
Standalone deployment:
Debian 7.7+
Ubuntu 14.04.5 / 16.04 / 18.04
Red Hat Enterprise Linux 7.4 – 7.8
CentOS 6.x / 7.4 – 7.8
Amazon Linux 2014.03 / 2014.09 / 2015.03 / 2015.09 / 2016.03 / 2016.09 / 2017.03 / 2017.09 / 2018.03 / 2.0 Oracle Linux 7.4 – 7.8
https://www.terraform.io/docs/enterprise/before-installing/index.html
123)	In Terraform Enterprise, a workspace can be mapped to how many VCS repos?
12/26/2022 – by Mod_GuideK0 
In Terraform Enterprise, a workspace can be mapped to how many VCS repos?
A. 5
B. 2
C. 3
D. 1
HIDE ANSWERS
Correct Answer: D
Explanation/Reference:
Explanation:
A workspace can only be configured to a single VCS repo, however, multiple workspaces can use the same repo.
https://www.terraform.io/docs/cloud/workspaces/vcs.html

124)	Which of the following allows Terraform users to apply policy as code to enforce standardized configurations for resources being deployed via infrastructure as code?
12/26/2022 – by Mod_GuideK0 
Which of the following allows Terraform users to apply policy as code to enforce standardized configurations for resources being deployed via infrastructure as code?
A. Sentinel
B. Module registry
C. Functions
D. Workspaces
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
Sentinel is a language and framework for policy built to be embedded in existing software to enable fine-grained, logic-based policy decisions. A policy describes under what circumstances certain behaviors are allowed. Sentinel is an enterprise-only feature.
https://www.youtube.com/watch?v=Vy8s7AAvU6g&feature=emb_title
125)	You cannot publish your own modules on the Terraform Registry.
12/26/2022 – by Mod_GuideK0 
You cannot publish your own modules on the Terraform Registry.
A. False
B. True
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
Anyone can publish and share modules on the Terraform Registry.
https://www.terraform.io/docs/registry/modules/publish.html

126)	Which command will the user execute to accomplish this?
12/26/2022 – by Mod_GuideK0 
A user has created three workspaces using the command line – prod, dev, and test. The user wants to create a fourth workspace named stage. Which command will the user execute to accomplish this?
A. terraform workspace new stage
B. terraform workspace -new stage
C. terraform workspace -create stage
D. terraform workspace create stage
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
The terraform workspace new command is used to create a new workspace.
https://www.terraform.io/docs/commands/workspace/new.html
127)	Which of the following Terraform commands will automatically refresh the state unless supplied with additional flags or arguments?
12/26/2022 – by Mod_GuideK0 
Which of the following Terraform commands will automatically refresh the state unless supplied with additional flags or arguments? Choose TWO correct answers.
A. terraform state
B. terraform apply
C. terraform plan
D. terraform validate
E. terraform output
HIDE ANSWERS
Correct Answer: BC
Explanation/Reference:
Explanation:

128)	What happens to the resource?
12/26/2022 – by Mod_GuideK0 
During a terraform apply, a resource is successfully created but eventually fails during provisioning.
What happens to the resource?
A. The resource will be planned for destruction and recreation upon the next terraform apply
B. Terraform will retry to provision again.
C. The failure of provisioner will be ignored and it will not cause a failure to terraform apply
D. The resource will be automatically destroyed.
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
If a creation-time provisioner fails, the resource is marked as tainted. A tainted resource will be planned for destruction and recreation upon the next terraform apply. Terraform does this because a failed provisioner can leave a resource in a semi-configured state. Because Terraform cannot reason about what the provisioner does, the only way to ensure proper creation of a resource is to recreate it. This is tainting.
You can change this behavior by setting the on_failure attribute, which is covered in detail below.
https://www.terraform.io/docs/provisioners/index.html#creation-time-provisioners
https://www.terraform.io/docs/provisioners/index.html#destroy-time-provisioners
https://www.terraform.io/docs/provisioners/index.html#failure-behavior
129)	If you delete a remote backend from the configuration, will you need to rebuild your state files locally?
12/26/2022 – by Mod_GuideK0 
If you delete a remote backend from the configuration, will you need to rebuild your state files locally?
A. False
B. True
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
You can change your backend configuration at any time. You can change both the configuration itself as well as the type of backend (for example from “consul” to “s3”).
Terraform will automatically detect any changes in your configuration and request a reinitialization.
As part of the reinitialization process, Terraform will ask if you’d like to migrate your existing state to the new configuration. This allows you to easily switch from one backend to another.
https://www.terraform.io/docs/backends/config.html#changing-configuration
130)	Which of the following state management command allow you to retrieve a list of resources that are part of the state file?
12/26/2022 – by Mod_GuideK0 
Which of the following state management command allow you to retrieve a list of resources that are part of the state file?
A. terraform state list
B. terraform state view
C. terraform view
D. terraform list
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
The terraform state list command is used to list resources within a Terraform state.
Usage: terraform state list [options] [address…]
The command will list all resources in the state file matching the given addresses (if any). If no addresses are given, all resources are listed.
https://www.terraform.io/docs/commands/state/list.html

131)	Terraform-specific settings and behaviors are declared in which configuration block type?
12/26/2022 – by Mod_GuideK0 
Terraform-specific settings and behaviors are declared in which configuration block type?
A. provider
B. terraform
C. resource
D. data
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
The special terraform configuration block type is used to configure some behaviors of Terraform itself, such as requiring a minimum Terraform version to apply your configuration.
Example terraform { required_version = “> 0.12.0”
}
https://www.terraform.io/docs/configuration/terraform.html

132)	Which flag would be used within a Terraform configuration block to identify the specific version of a provider required?
12/26/2022 – by Mod_GuideK0 
Which flag would be used within a Terraform configuration block to identify the specific version of a provider required?
A. required-provider
B. required-version
C. required_providers
D. required_versions
HIDE ANSWERS
Correct Answer: C
Explanation/Reference:
Explanation:
For production use, you should constrain the acceptable provider versions via configuration file to ensure that new versions with breaking changes will not be automatically installed by terraform init in the future.
Example terraform { required_providers { aws = “>= 2.7.0”
}}
133)	What is the best way to do it?
12/26/2022 – by Mod_GuideK0 
Jim has created several AWS resources from a single terraform configuration file. Someone from his team has manually modified one of the EC2 instance.
Now to discard the manual change, Jim wants to destroy and recreate the EC2 instance. What is the best way to do it?
A. terraform recreate
B. terraform taint
C. terraform destroy
D. terraform refresh
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
The terraform taint command manually marks a Terraform-managed resource as tainted, forcing it to be destroyed and recreated on the next apply.
This command will not modify infrastructure, but does modify the state file in order to mark a resource as tainted. Once a resource is marked as tainted, the next plan will show that the resource will be destroyed and recreated and the next apply will implement this change.
Forcing the recreation of a resource is useful when you want a certain side effect of recreation that is not visible in the attributes of a resource. For example: re-running provisioners will cause the node to be different or rebooting the machine from a base image will cause new startup scripts to run.
Note that tainting a resource for recreation may affect resources that depend on the newly tainted resource. For example, a DNS resource that uses the IP address of a server may need to be modified to reflect the potentially new IP
address of a tainted server. The plan command will show this if this is the case.
This example will taint a single resource:
$ terraform taint aws_security_group.allow_all
The resource aws_security_group.allow_all in the module root has been marked as tainted.
https://www.terraform.io/docs/commands/taint.html

134)	Which of the below options is a valid interpolation syntax for retrieving a data source?
12/26/2022 – by Mod_GuideK0 
Which of the below options is a valid interpolation syntax for retrieving a data source?
A. ${google_storage_bucket.backend}
B. ${azurerm_resource_group.test.data}
C. ${aws_instance.web.id.data}
D. ${data.google_dns_keys.foo_dns_keys.key_signing_keys[0].ds_record}
HIDE ANSWERS
Correct Answer: D
Explanation/Reference:
Explanation:
Data source attributes are interpolated with the general syntax data.TYPE.NAME.ATTRIBUTE. The interpolation for a resource is the same but without the data. prefix (TYPE.NAME.ATTRIBUTE).
https://www.terraform.io/docs/configuration-0-11/interpolation.html#attributes-of-a-data-source

135)	State locking does not happen automatically and must be specified at run
12/26/2022 – by Mod_GuideK0 
State locking does not happen automatically and must be specified at run
A. False
B. True
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
State locking happens automatically on all operations that could write state.
https://www.terraform.io/docs/state/locking.html

136)	Command terraform refresh will update state file?
12/26/2022 – by Mod_GuideK0 
Command terraform refresh will update state file?
A. False
B. True
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
The terraform refresh command is used to reconcile the state Terraform knows about (via its state file) with the real-world infrastructure. This can be used to detect any drift from the last-known state, and to update the state file.
This does not modify infrastructure, but does modify the state file. If the state is changed, this may cause changes to occur during the next plan or apply.
https://www.terraform.io/docs/commands/refresh.html

137)	The terraform state command can be used to ____
12/26/2022 – by Mod_GuideK0 
The terraform state command can be used to ____
A. Update current state
B. Refresh existing state file
C. Print the current state file in console
D. It is not a valid command
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
The terraform state command is used for advanced state management. Rather than modify the state directly, the terraform state commands can be used in many cases instead.
https://www.terraform.io/docs/commands/state/index.html

138)	Taint the resource “aws_instance” “baz” resource that lives in module bar which lives in module foo.
12/26/2022 – by Mod_GuideK0 
Taint the resource “aws_instance” “baz” resource that lives in module bar which lives in module foo.
A. terraform taint module.foo.module.bar.baz
B. terraform taint module.foo.bar.aws_instance.baz
C. terraform taint module.foo.module.bar.aws_instance.baz
D. terraform taint foo.bar.aws_instance.baz
HIDE ANSWERS
Correct Answer: C
Explanation/Reference:
Explanation:
Check resource addressing
https://www.terraform.io/docs/internals/resource-addressing.html
139)	Multiple configurations for the same provider can be used in a single configuration file.
12/26/2022 – by Mod_GuideK0 
Multiple configurations for the same provider can be used in a single configuration file.
A. False
B. True
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
You can optionally define multiple configurations for the same provider, and select which one to use on a per-resource or per-module basis. The primary reason for this is to support multiple regions for a cloud platform; other examples include targeting multiple Docker hosts, multiple Consul hosts, etc.
To include multiple configurations for a given provider, include multiple provider blocks with the same provider name, but set the alias meta-argument to an alias name to use for each additional configuration. For example:
# The default provider configuration provider “aws” { region = “us-east-1”
} # Additional provider configuration for west coast region provider “aws” { alias = “west” region = “us-west-2”
} The provider block without alias set is known as the default provider configuration. When alias is set, it creates an additional provider configuration. For providers that have no required configuration arguments, the implied empty configuration is considered to be the default provider configuration.
https://www.terraform.io/docs/configuration/providers.html#alias-multiple-provider-instances

140)	Where is your state file stored?
12/26/2022 – by Mod_GuideK0 
You have created two workspaces PROD and DEV. You have switched to DEV and provisioned DEV infrastructure from this workspace. Where is your state file stored?
A. terraform.d
B. terraform.tfstate
C. terraform.tfstate.DEV
D. terraform.tfstate.d
HIDE ANSWERS
Correct Answer: D
Explanation/Reference:
Explanation:
Terraform stores the workspace states in a directory called terraform.tfstate.d. This directory should be treated similarly to default workspace state file terraform.tfstate
+– main.tf
+– provider.tf
+– terraform.tfstate.d
¦ +– DEV
¦ ¦ +– terraform.tfstate # DEV workspace state file
¦ +– PROD
¦ +– terraform.tfstate # PROD workspace state file
+– terraform.tfvars # Default workspace state file
+– variables.tf


141)	Which of the below options is the equivalent Terraform 0.12 version of the snippet which is written in Terraform 0.11?
12/26/2022 – by Mod_GuideK0 
Which of the below options is the equivalent Terraform 0.12 version of the snippet which is written in Terraform 0.11?
“${var.instance_id}”
A. variable.instance_id
B. var.instance_ids
C. var.instance_id
D. None of the above
HIDE ANSWERS
Correct Answer: C
Explanation/Reference:
Explanation:
142)	You cannot publish your own modules on the Terraform Registry.
12/26/2022 – by Mod_GuideK0 
You cannot publish your own modules on the Terraform Registry.
A. False
B. True
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
https://www.terraform.io/docs/registry/modules/publish.html

143)	What is the possible way to structure the terraform code to facilitate that.
12/26/2022 – by Mod_GuideK0 
Your manager has instructed you to start using terraform for the entire infra provisioning of the application stack. There are 4 environments – DEV , QA , UAT , and PROD. The application team has asked for complete segregation between these environments including the backend , state , and also configurations ,since there will be unique resources in different environments . What is the possible way to structure the terraform code to facilitate that.
A. Completely separate the working directories , keep one for each environment . For each working directory , maintain a separate configuration file , variables file , and map to a different backend.
B. Completely separate the working directories , keep one for each environment . For each working directory , maintain a separate configuration file , variables file , and map to the same backend.
C. Implement terraform workspaces , and map each environment with one workspace.
D. Enable remote backend storage . Configure 4 different backend storages , one for each environment.
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
In particular, organizations commonly want to create a strong separation between multiple deployments of the same infrastructure serving different development stages (e.g. staging vs. production) or different internal teams. In this case, the backend used for each deployment often belongs to that deployment, with different credentials and access controls. Named workspaces are not a suitable isolation mechanism for this scenario.
https://www.terraform.io/docs/state/workspaces.html

144)	Which of the below command will upgrade the provider version to the latest acceptable one?
12/26/2022 – by Mod_GuideK0 
Which of the below command will upgrade the provider version to the latest acceptable one?
A. terraform plan upgrade
B. terraform provider -upgrade
C. terraform init -upgrade
D. terraform init -update
HIDE ANSWERS
Correct Answer: C
Explanation/Reference:
Explanation:
To upgrade to the latest acceptable version of each provider, run terraform init -upgrade. This command also upgrades to the latest versions of all Terraform modules.
https://www.terraform.io/docs/configuration/providers.html

145)	What happens when a terraform apply command is executed?
12/26/2022 – by Mod_GuideK0 
What happens when a terraform apply command is executed?
A. Creates the execution plan for the deployment of resources.
B. Applies the changes required in the target infrastructure in order to reach the desired configuration.
C. The backend is initialized and the working directory is prepped.
D. Reconciles the state Terraform knows about with the real-world infrastructure.
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
The terraform apply command is used to apply the changes required to reach the desired state of the configuration, or the pre-determined set of actions generated by a terraform plan execution plan.
https://www.terraform.io/docs/commands/apply.html

146)	What command will do this?
12/26/2022 – by Mod_GuideK0 
Forcing the recreation of a resource is useful when you want a certain side effect of recreation that is not visible in the attributes of a resource. What command will do this?
A. terraform taint
B. terraform apply
C. terraform graph
D. terraform refresh
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
The terraform taint command manually marks a Terraform-managed resource as tainted, forcing it to be destroyed and recreated on the next apply.
This command will not modify infrastructure, but does modify the state file in order to mark a resource as tainted. Once a resource is marked as tainted, the next plan will show that the resource will be destroyed and recreated and the next apply will implement this change.
Forcing the recreation of a resource is useful when you want a certain side effect of recreation that is not visible in the attributes of a resource. For example: re-running provisioners will cause the node to be different or rebooting the machine from a base image will cause new startup scripts to run.
Note that tainting a resource for recreation may affect resources that depend on the newly tainted resource. For example, a DNS resource that uses the IP address of a server may need to be modified to reflect the potentially new IP
address of a tainted server. The plan command will show this if this is the case.
This example will taint a single resource:
$ terraform taint aws_security_group.allow_all
The resource aws_security_group.allow_all in the module root has been marked as tainted.
https://www.terraform.io/docs/commands/taint.html

147)	What is the best approach to create the EC2 instances that can deal with different AMI IDs based on regions?
12/26/2022 – by Mod_GuideK0 
Every region in AWS has a different AMI ID for Linux and these are keep on changing. What is the best approach to create the EC2 instances that can deal with different AMI IDs based on regions?
A. Use data source aws_ami.
B. Create a map of region to ami id.
C. Create different configuration file for different region.
D. None of the above
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
https://www.terraform.io/docs/configuration/data-sources.html

148)	Mary has created a database instance in AWS and for ease of use is outputting the value of the database password with the following code:
12/26/2022 – by Mod_GuideK0 
Mary has created a database instance in AWS and for ease of use is outputting the value of the database password with the following code:
1. output “db_password”
2. {
3. value = local.db_password
4. }
Mary wants to hide the output value in the CLI after terraform apply? What is the best way?
A. Use secure parameter
B. Use sensitive parameter
C. Use cryptographic hash
D. Encrypt the value using encrypt() function
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:

149)	Dawn has created the below child module. Without changing the module, can she override the instance_type from t2.micro to t2.large form her code while calling this module?
12/26/2022 – by Mod_GuideK0 
Dawn has created the below child module. Without changing the module, can she override the instance_type from t2.micro to t2.large form her code while calling this module?
1. resource “aws_instance” “myec2”
2. {
3. ami = “ami-082b5a644766e0e6f”
4. instance_type = “t2.micro
5. }
A. YES
B. No
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
As the instance_type is hard-coded in source module, you will not be able to change its value from destination module. Instead of hard-coding you should use variable with default values.

150)	Eric needs to make use of module within his terraform code. Should the module always be public and open-source to be able to be used?
12/26/2022 – by Mod_GuideK0 
Eric needs to make use of module within his terraform code. Should the module always be public and open-source to be able to be used?
A. False
B. True
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
Terraform module need not be public and open-source. Module can be placed in – * Local paths * Terraform Registry * GitHub * Bitbucket * Generic Git, Mercurial repositories * HTTP URLs * S3 buckets * GCS buckets
https://www.terraform.io/docs/modules/sources.html

151)	After creating a new workspace “PROD” you need to run the command terraform select PROD to switch to it.
12/26/2022 – by Mod_GuideK0 
After creating a new workspace “PROD” you need to run the command terraform select PROD to switch to it.
A. False
B. True
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
By default, when you create a new workspace you are automatically switched to it To create a new workspace and switch to it, you can use terraform workspace new
<new_workspace_name>; to switch to a existing workspace you can use terraform workspace select
<existing_workspace_name>; Example:
$ terraform workspace new example
Created and switched to workspace “example”!
You’re now on a new, empty workspace. Workspaces isolate their state, so if you run “terraform plan” Terraform will not see any existing state for this configuration.
152)	What feature could you use to iterate over a list of required tcp ports to add to the new security group?
12/26/2022 – by Mod_GuideK0 
You have been given requirements to create a security group for a new application. Since your organization standardizes on Terraform, you want to add this new security group with the fewest number of lines of code. What feature could you use to iterate over a list of required tcp ports to add to the new security group?
A. dynamic backend
B. splat expression
C. terraform import
D. dynamic block
HIDE ANSWERS
Correct Answer: D
Explanation/Reference:
Explanation:
A dynamic block acts much like a for expression, but produces nested blocks instead of a complex typed value. It iterates over a given complex value and generates a nested block for each element of that complex value.
https://www.terraform.io/docs/configuration/expressions.html#dynamic-blocks

153)	You have already set TF_LOG = DEBUG to enable debug log.
12/26/2022 – by Mod_GuideK0 
You have already set TF_LOG = DEBUG to enable debug log. Now you want to always write the log to the directory you’re currently running terraform from. what should you do to achieve this.
A. Run the command export TF_LOG_FILE=./terraform.log.
B. Run the command export TF_LOG_PATH=./terraform.log.
C. Run the command export TF_DEBUG_PATH=./terraform.log.
D. No explicit action required. Terraform will take care of this as you have enable TF_LOG.
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
https://www.terraform.io/docs/commands/environment-variables.html
154)	Terraform Cloud always encrypts state at rest and protects it with TLS in transit.
12/26/2022 – by Mod_GuideK0 
Terraform Cloud always encrypts state at rest and protects it with TLS in transit. Terraform Cloud also knows the identity of the user requesting state and maintains a history of state changes.
A. False
B. True
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
Terraform Cloud always encrypts state at rest and protects it with TLS in transit. Terraform Cloud also knows the identity of the user requesting state and maintains a history of state changes. This can be used to control access and track activity. Terraform Enterprise also supports detailed audit logging.
https://www.terraform.io/docs/state/sensitive-data.html#recommendations


155)	What kind of resource dependency is stored in terraform.tfstate file?
12/26/2022 – by Mod_GuideK0 
What kind of resource dependency is stored in terraform.tfstate file?
A. Both implicit and explicit dependencies are stored in state file.
B. Only explicit dependencies are stored in state file.
C. Only implicit dependencies are stored in state file.
D. No dependency information is stored in state file.
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
Terraform state captures all dependency information, both implicit and explicit. One purpose for state is to determine the proper order to destroy resources. When resources are created all of their dependency information is stored in the state. If you destroy a resource with dependencies, Terraform can still determine the correct destroy order for all other resources because the dependencies are stored in the state.
https://www.terraform.io/docs/state/purpose.html#metadata

156)	Which of the following are string functions?
12/26/2022 – by Mod_GuideK0 
Which of the following are string functions? Select three
A. tostring
B. tonumber
C. Chomp
D. format
E. join
HIDE ANSWERS
Correct Answer: CDE
Explanation/Reference:
Explanation: tonumber and tostring are Type Conversion function
https://www.terraform.io/docs/configuration/functions.html


157)	What is the best way to ensure that you are not using the latest version of the module?
12/26/2022 – by Mod_GuideK0 
A colleague has informed you that a new version of a Terraform module that your team hosts on an Amazon S3 bucket is broken. The Amazon S3 bucket has versioning enabled. Your colleague tells you to make sure you are not using the latest version in your configuration. You have the following configuration block in your code that refers to the module: module “infranet” { source = “s3::https://s3-us-west- 2.amazonaws.com/infrabucket/infra_module.zip”} What is the best way to ensure that you are not using the latest version of the module?
A. Add a module version constraint in your configuration’s backend block and specify a previous version.
B. Add a version key to the module configuration and specify a previous version.
C. Delete the latest version of the module in S3 to rollback to the previous version.
D. Add a version property to the module in Terraform’s state file and specify a previous version.
HIDE ANSWERS
Correct Answer: C
Explanation/Reference:
Explanation:
Version constraints are supported only for modules installed from a module registry, such as the Terraform Registry or Terraform Cloud’s private module registry. Other module sources can provide their own versioning mechanisms within the source string itself, or might not support versions at all.
In particular, modules sourced from local file paths do not support version; since they’re loaded from the same source repository.
Only Terraform Registries support module versioning by using the version key, one cannot configure a previous version of the module in the configuration. Deleting the latest version of the module in S3 is the only option of the available options that ensures you won’t use the latest version. You could also modify the source URL to specify a versionId URL parameter for a previous version.
https://www.terraform.io/docs/configuration/modules.html#source

158)	What is the best way to achieve it?
12/26/2022 – by Mod_GuideK0 
The Security Operations team of ABC Enterprise wants to mandate that all the Terraform configuration that creates an S3 bucket must have encryption feature enabled. What is the best way to achieve it?
A. Use Sentinel Policies.
B. Use S3 bucket policy.
C. Create a script that checks the encryption parameter is enabled on every git commit.
D. Shared a SOP to engineers to mandate encryption feature on S3.
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
Sentinel is an embedded policy-as-code framework integrated with the HashiCorp Enterprise products. It enables fine-grained, logic-based policy decisions, and can be extended to use information from external sources.
Using Sentinel with Terraform Cloud involves:
* Defining the policies – Policies are defined using the policy language with imports for parsing the Terraform plan, state and configuration.
* Managing policies for organizations – Users with permission to manage policies can add policies to their organization by configuring VCS integration or uploading policy sets through the API. They also define which workspaces the policy sets are checked against during runs. (More about permissions.)
* Enforcing policy checks on runs – Policies are checked when a run is performed, after the terraform plan but before it can be confirmed or the terraform apply is executed.
* Mocking Sentinel Terraform data – Terraform Cloud provides the ability to generate mock data for any run within a workspace. This data can be used with the Sentinel CLI to test policies before deployment.
https://www.terraform.io/docs/cloud/sentinel/index.html

159)	What feature of Terraform would you recommend to use to reduce the amount of cloned configuration between the different configurations?
12/26/2022 – by Mod_GuideK0 
You are reviewing Terraform configurations for a big project in your company. You noticed that there are several identical sets of resources that appear in multiple configurations. What feature of Terraform would you recommend to use to reduce the amount of cloned configuration between the different configurations?
A. Packages
B. Backends
C. Provisioners
D. Modules
HIDE ANSWERS
Correct Answer: D
Explanation/Reference:
Explanation:
Modules are reusable configuration packages that Terraform can share through a variety of sources including Terraform Registries, GitHub, and Amazon S3 buckets.
A module is a container for multiple resources that are used together. Modules can be used to create lightweight abstractions, so that you can describe your infrastructure in terms of its architecture, rather than directly in terms of physical objects.
Modules are reusable configuration packages that Terraform can share through a variety of sources including Terraform Registries, GitHub, and Amazon S3 buckets.
https://www.terraform.io/docs/modules/index.html

160)	Which of the following values will be assigned to the name attribute of track_tag variable?
12/26/2022 – by Mod_GuideK0 
Refer to the following terraform variable definition variable “track_tag” { type = list default = [“data_ec2″,”integration_ec2″,”digital_ec2”]} track_tag =
{ Name = element(var.track_tag,count.index)} If count.index is set to 2, which of the following values will be assigned to the name attribute of track_tag variable?
A. integration_ec2
B. digital_ec2
C. track_tag
D. data_ec2
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:

161)	Which of the below features of Terraform can be used for managing small differences between different environments which can act more like completely separate working directories.
12/26/2022 – by Mod_GuideK0 
Which of the below features of Terraform can be used for managing small differences between different environments which can act more like completely separate working directories.
A. Repositories
B. Workspaces
C. Environment Variables
D. Backends
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation: workspaces allow conveniently switching between multiple instances of a single configuration within its single backend. They are convenient in a number of situations, but cannot solve all problems.
A common use for multiple workspaces is to create a parallel, distinct copy of a set of infrastructure in order to test a set of changes before modifying the main production infrastructure. For example, a developer working on a complex set of infrastructure changes might create a new temporary workspace in order to freely experiment with changes without affecting the default workspace.
Non-default workspaces are often related to feature branches in version control. The default workspace might correspond to the “master” or “trunk” branch, which describes the intended state of production infrastructure. When a feature branch is created to develop a change, the developer of that feature might create a corresponding workspace and deploy into it a temporary “copy” of the main infrastructure so that changes can be tested without affecting the production infrastructure. Once the change is merged and deployed to the default workspace, the test infrastructure can be destroyed and the temporary workspace deleted.
https://www.terraform.io/docs/state/workspaces.html
https://www.terraform.io/docs/state/workspaces.html#when-to-use-multiple-workspaces

162)	Which of the below option is a recommended solution for this?
12/26/2022 – by Mod_GuideK0 
When using Terraform in a team it is important for everyone to be working with the same state so that operations will be applied to the same remote objects. Which of the below option is a recommended solution for this?
A. Remote State
B. Module
C. Use the cached state and treat this as the record of truth.
D. Workspace
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
https://www.terraform.io/docs/state/remote.html

163)	Which of the following variable definition files will terraform load automatically?
12/26/2022 – by Mod_GuideK0 
Which of the following variable definition files will terraform load automatically?
A. terraform.tfvar
B. Any files with names ending in .auto.tfvars.json
C. terraform.tfvars
D. terraform.tfvars.json
HIDE ANSWERS
Correct Answer: BCD
Explanation/Reference:
Explanation:
Terraform also automatically loads a number of variable definitions files if they are present:
Files named exactly terraform.tfvars or terraform.tfvars.json.
Any files with names ending in .auto.tfvars or .auto.tfvars.json.
https://www.terraform.io/docs/configuration/variables.html
https://www.terraform.io/docs/configuration/variables.html#variable-definitions-tfvars-files
164)	Which of the following challenges would Terraform be a candidate for solving?
12/26/2022 – by Mod_GuideK0 
Which of the following challenges would Terraform be a candidate for solving? (Select THREE)
A. Enable self-service infrastructure to allocate resources on your proprietary private cloud.
B. Reduce the number of workflows needed for managing infrastructure across each of the companies public and private clouds.
C. Utilize a single tool for all of the infrastructure and configuration management needs.
D. Have a single interoperable tool to manage the variety of services including GitHub repositories, MySQL database, and Kubernetes clusters.
HIDE ANSWERS
Correct Answer: ABD
Explanation/Reference:
Explanation:
165)	What are the options of doing that?
12/26/2022 – by Mod_GuideK0 
You have provisioned some aws resources in your test environment through Terraform for a POC work. After the POC, now you want to destroy the resources but before destroying them you want to check what resources will be getting destroyed through terraform. what are the options of doing that? (Select TWO)
A. Use terraform destroy command
B. This is not possible
C. Use terraform plan command
D. Use terraform plan -destroy command.
HIDE ANSWERS
Correct Answer: AD
Explanation/Reference:
Explanation:
https://learn.hashicorp.com/terraform/getting-started/destroy


166)	What is the value assigned to the itemNum variable?
12/26/2022 – by Mod_GuideK0 
You have a Terraform configuration file where a variable itemNum is defined as follows: variable “itemNum” { default = 3} You also have a defined the following environment variables in your shell: TF_itemNum =6, TF_VAR_itemNum =9.
You also have a terraform.tfvars file with the following contents itemNum = 7 When you run the following apply command, what is the value assigned to the itemNum variable? terraform apply -var itemNum =4
A. 10
B. 6
C. 1
D. 4
E. 3
HIDE ANSWERS
Correct Answer: D
Explanation/Reference:
Explanation:
The -var and -var-file methods of assigning variables have the highest precedence.
https://www.terraform.io/docs/configuration/variables.html


167)	How can you change this default behavior within a provisioner?
12/26/2022 – by Mod_GuideK0 
By default, provisioners that fail will also cause the Terraform apply itself to error. How can you change this default behavior within a provisioner?
A. provisioner “local-exec” { on_failure = “next” }
B. provisioner “local-exec” { when = “failure” terraform apply }
C. provisioner “local-exec” { on_failure = “continue” }
D. provisioner “local-exec” { on_failure = continue }
HIDE ANSWERS
Correct Answer: C
Explanation/Reference:
Explanation:
https://www.terraform.io/docs/provisioners/index.html

168)	Refer below code where pessimistic constraint operator has been used to specify a version of a provider.
12/26/2022 – by Mod_GuideK0 
Refer below code where pessimistic constraint operator has been used to specify a version of a provider. terraform { required_providers { aws = “~> 1.1.0” }} Which of the following options are valid provider versions that satisfy the above constraint. (select two)
A. 1.1.1
B. 1.2.9
C. 1.1.8
D. 1.2.0
HIDE ANSWERS
Correct Answer: AC
Explanation/Reference:
Explanation:
Pessimistic constraint operator, constraining both the oldest and newest version allowed. For example, ~> 0.9 is equivalent to >= 0.9, < 1.0, and ~> 0.8.4, is equivalent to >= 0.8.4, < 0.9

169)	What should be your approach.
12/26/2022 – by Mod_GuideK0 
Your company has been using Terraform Cloud for a some time now . But every team is creating their own modules , and there is no standardization of the modules , with each team creating the resources in their own unique way . You want to enforce a standardization of the modules across the enterprise . What should be your approach.
A. Create individual workspaces for each team , and ask them to share modules across workspaces.
B. Implement a Private module registry in Terraform cloud , and ask teams to reference them.
C. Upgrade to Terraform enterprise , since this is not possible in terraform cloud.
D. Upload the modules in the terraform public module registry , and ask teams to reference them
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
Terraform Cloud’s private module registry helps you share Terraform modules across your organization. It includes support for module versioning, a searchable and filterable list of available modules, and a configuration designer to help you build new workspaces faster.
By design, the private module registry works much like the public Terraform Registry. If you’re already used the public registry, Terraform Cloud’s registry will feel familiar.
Understand the different offerings in Terraform OS, Terraform Cloud and Terraform Enterprise.
Terraform Cloud’s private module registry helps you share Terraform modules across your organization.
https://www.terraform.io/docs/cloud/registry/index.html
https://www.terraform.io/docs/cloud/registry/publish.html

170)	What can be done from your end to solve this problem?
12/26/2022 – by Mod_GuideK0 
You have created a terraform script that uses a lot of new constructs that have been introduced in terraform v0.12. However, many developers who are cloning the script from your git repo, are using v0.11, and getting errors. What can be done from your end to solve this problem?
A. Force developer to use v0.12 by using terraform setting ‘required_version’ and set it to >=0.12.
B. Refactor the code to support both v0.11, and v0.12. It might be a difficult process, but there is no other way.
C. Add a condition in front of each such specific construct, to check whether the running terraform version id v0.11 or v0.12, and ,work accordingly.
D. Add comments in your code to tell developers to use v0.12 . If they use v0.11 , that should be their problem , which they need to figure out.
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
https://www.terraform.io/docs/configuration/terraform.html

171)	What should be your response to the security team in this regard?
12/26/2022 – by Mod_GuideK0 
Your manager has instructed you to start using terraform for your day-to-day operations, but your security team is concerned about the terraform state files. They have heard it contains confidential information, and are worried that it will not be securely protected. What should be your response to the security team in this regard?
A. Inform the security team that using terraform state is optional . There are ways to avoid it , and you will do the same.
B. Ensure that the state is managed in a remote backend , preferably an enterprise grade state management system like Terraform Cloud.
C. Mask the confidential entries in the terraform state file , using Vault Enterprise, another Hashicorp product , while keeping it locally.
D. Keep the state file locally on each developer machine , and ensure that there is a local protection software like KeyPass protecting it.
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
https://www.terraform.io/docs/state/index.htmlState is very important topic for exam. Please read all of the below subtopicsPurposeImport Existing ResourcesLockingWorkspacesRemote StateSensitive Data

172)	In regards to Terraform state file, select all the statements below which are correct?
12/26/2022 – by Mod_GuideK0 
In regards to Terraform state file, select all the statements below which are correct?
A. When using local state, the state file is stored in plain-text.
B. The state file is always encrypted at rest.
C. Storing state remotely can provide better security.
D. Using the mask feature, you can instruct Terraform to mask sensitive data in the state file.
E. The Terraform state can contain sensitive data, therefore the state file should be protected from unauthorized access.
F. Terraform Cloud always encrypts state at rest.
HIDE ANSWERS
Correct Answer: ACEF
Explanation/Reference:
Explanation:
Terraform state can contain sensitive data, depending on the resources in use and your definition of “sensitive.” The state contains resource IDs and all resource attributes. For resources such as databases, this may contain initial passwords.
When using local state, state is stored in plain-text JSON files.
When using remote state, state is only ever held in memory when used by Terraform. It may be encrypted at rest, but this depends on the specific remote state backend.
Storing Terraform state remotely can provide better security. As of Terraform 0.9, Terraform does not persist state to the local disk when remote state is in use, and some backends can be configured to encrypt the state data at rest.
Recommendations
If you manage any sensitive data with Terraform (like database passwords, user passwords, or private keys), treat the state itself as sensitive data.
Storing state remotely can provide better security. As of Terraform 0.9, Terraform does not persist state to the local disk when remote state is in use, and some backends can be configured to encrypt the state data at rest.
For example:
* Terraform Cloud always encrypts state at rest and protects it with TLS in transit. Terraform Cloud also knows the identity of the user requesting state and maintains a history of state changes. This can be used to control access and track activity. Terraform Enterprise also supports detailed audit logging.
* The S3 backend supports encryption at rest when the encrypt option is enabled. IAM policies and logging can be used to identify any invalid access. Requests for the state go over a TLS connection.

173)	Why is it a good idea to declare the required version of a provider in a Terraform configuration file?
12/26/2022 – by Mod_GuideK0 
Why is it a good idea to declare the required version of a provider in a Terraform configuration file?
1. terraform
2. {
3. required_providers
4. {
5. aws = “~> 1.0”
6. }
7. }
A. To remove older versions of the provider.
B. To ensure that the provider version matches the version of Terraform you are using.
C. Providers are released on a separate schedule from Terraform itself; therefore a newer version could introduce breaking changes.
D. To match the version number of your application being deployed via Terraform.
HIDE ANSWERS
Correct Answer: C
Explanation/Reference:
Explanation:
174)	What is a better approach to dealing with this?
12/26/2022 – by Mod_GuideK0 
Hanah is writing a terraform configuration with nested modules, there are multiple places where she has to use the same conditional expression but she wants to avoid repeating the same values or expressions multiple times in the configuration,. What is a better approach to dealing with this?
A. Expressions
B. Local Values
C. Variables
D. Functions
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
https://www.terraform.io/docs/configuration/locals.html

175)	Multiple providers can be declared within a single Terraform configuration file.
12/26/2022 – by Mod_GuideK0 
Multiple providers can be declared within a single Terraform configuration file.
A. True
B. False
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
You can optionally define multiple configurations for the same provider, and select which one to use on a per-resource or per-module basis. The primary reason for this is to support multiple regions for a cloud platform; other examples include targeting multiple Docker hosts, multiple Consul hosts, etc.
To include multiple configurations for a given provider, include multiple provider blocks with the same provider name, but set the alias meta-argument to an alias name to use for each additional configuration.
For Example
# The default provider configuration provider “aws” { region = “us-east-1”
} # Additional provider configuration for west coast region provider “aws” { alias = “west” region = “us-west-2”
} The provider block without alias set is known as the default provider configuration. When alias is set, it creates an additional provider configuration. For providers that have no required configuration arguments, the implied empty configuration is considered to be the default provider configuration.
https://www.terraform.io/docs/configuration/providers.html

176)	Once a resource is marked as tainted, the next plan will show that the resource will be _________ and ___________ and the next apply will implement this change.
12/26/2022 – by Mod_GuideK0 
Once a resource is marked as tainted, the next plan will show that the resource will be _________ and ___________ and the next apply will implement this change.
A. recreated and tainted
B. destroyed and not recreated
C. tainted and not destroyed
D. destroyed and recreated
HIDE ANSWERS
Correct Answer: D
Explanation/Reference:
Explanation:
177)	When multiple engineers start deploying infrastructure using the same state file, what is a feature of remote state storage that is critical to ensure the state doesn’t become corrupt?
12/26/2022 – by Mod_GuideK0 
When multiple engineers start deploying infrastructure using the same state file, what is a feature of remote state storage that is critical to ensure the state doesn’t become corrupt?
A. Object Storage
B. State Locking
C. WorkSpaces
D. Encryption
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
If supported by your backend, Terraform will lock your state for all operations that could write state.
This prevents others from acquiring the lock and potentially corrupting your state.
State locking happens automatically on all operations that could write state. You won’t see any message that it is happening. If state locking fails, Terraform will not continue. You can disable state locking for most commands with the -lock flag but it is not recommended.
If acquiring the lock is taking longer than expected, Terraform will output a status message. If Terraform doesn’t output a message, state locking is still occurring if your backend supports it.
Not all backends support locking. Please view the list of backend types for details on whether a backend supports locking or not.
https://www.terraform.io/docs/state/locking.html

178)	Which of the following value will be accepted for var1?
12/26/2022 – by Mod_GuideK0 
Which of the following value will be accepted for var1? variable “var1” { type = string
}
A. None of the above
B. Both A and B
C. “5”
D. 5
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
Terraform automatically converts number and bool values to strings when needed

179)	Which of the below datatype is not supported by Terraform.
12/26/2022 – by Mod_GuideK0 
Which of the below datatype is not supported by Terraform.
A. Array
B. List
C. Object
D. Map
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
180)	What will happen?
12/26/2022 – by Mod_GuideK0 
You have created an AWS EC2 instance of type t2.micro through your terraform configuration file ec2.tf . Now you want to change the instance type from t2.micro to t2.medium. Accordingly you have changed your configuration file and and ran terraform plan. After running terraform plan you check the output and saw one instance will be updated from t2.micro –> t2.medium. After this you went to grab a coffee without running terraform apply and meanwhile a member of your team changed the instance type of that EC2 instance to t2.medium from aws console. After coming to your desk you run terraform apply. What will happen?
A. No resource will be updated and you will see the message : Apply Complete ! Resources : 0 added, 0 changed, 0 destroyed.
B. The instance type will be changed to t2.micro and again will be changed to t2.medium
C. terraform apply will through an error.
D. 1 resource will be updated and you will see the message : Apply Complete ! Resources : 0 added, 1 changed, 0 destroyed.
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:

181)	What can you do to fix this problem?
12/26/2022 – by Mod_GuideK0 
You have multiple developers working on a terraform project (using terraform OSS), and have saved the terraform state in a remote S3 bucket . However ,team is intermittently experiencing inconsistencies in the provisioned infrastructure / failure in the code . You have traced this problem to simultaneous/concurrent runs of terraform apply command for 2/more developers . What can you do to fix this problem?
A. Use terraform workspaces feature, this will fix this problem by default , as every developer will have their own state file , and terraform will merge them on server side on its own.
B. Structure your team in such a way that only one individual will run terraform apply , everyone will just make changes and share with him. Then there will be no chance of any inconsistencies.
C. Stop using remote state , and store the developer tfstate in their own machine . Once a day , all developers should sit together and merge the state files manually , to avoid any inconsistencies.
D. Enable terraform state locking for the S3 backend using DynamoDB table. This prevents others from acquiring the lock and potentially corrupting your state.
HIDE ANSWERS
Correct Answer: D
Explanation/Reference:
Explanation:
S3 backend support state locking using DynamoDB.
https://www.terraform.io/docs/state/locking.html
182)	A data block requests that Terraform read from a given data source and export the result under the given local name.
12/26/2022 – by Mod_GuideK0 
A data block requests that Terraform read from a given data source and export the result under the given local name.
A. False
B. True
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:


183)	A single terraform resource file that defines an aws_instance resource can simply be renamed to vsphere_virtual_machine in order to switch cloud providers.
12/26/2022 – by Mod_GuideK0 
A single terraform resource file that defines an aws_instance resource can simply be renamed to vsphere_virtual_machine in order to switch cloud providers.
A. True
B. False
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
Every provider has its own required and allowed declarations none of which match between cloud providers.

184)	Which one of the below you will choose?
12/26/2022 – by Mod_GuideK0 
You want terraform plan and terraform apply to be executed in Terraform Cloud’s run environment but the output is to be streamed locally. Which one of the below you will choose?
A. Local Backends.
B. Terraform Backends.
C. This can be done using any of the local or remote backends.
D. Remote Backends.
HIDE ANSWERS
Correct Answer: D
Explanation/Reference:
Explanation:
When using full remote operations, operations like terraform plan or terraform apply can be executed in Terraform Cloud’s run environment, with log output streaming to the local terminal.
Remote plans and applies use variable values from the associated Terraform Cloud workspace.
Terraform Cloud can also be used with local operations, in which case only state is stored in the Terraform Cloud backend.
https://www.terraform.io/docs/backends/types/remote.html

185)	Which of the below commands will rename a EC2 instance without destroying and recreating it?
12/26/2022 – by Mod_GuideK0 
Which of the below commands will rename a EC2 instance without destroying and recreating it?
A. terraform state mv
B. terraform mv
C. terraform plan
D. terraform plan mv
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:

186)	
12/26/2022 – by Mod_GuideK0 
1. resource “aws_s3_bucket” “example” {
2. bucket = “my-test-s3-terraform-bucket”
3. …} resource “aws_iam_role” “test_role” {
4. name = “test_role”
5. …}
Due to the way that the application code is written, the s3 bucket must be created before the test role is created, otherwise there will be a problem. How can you ensure that?
A. Add explicit dependency using depends_on . This will ensure the correct order of resource creation.
B. This will already be taken care of by terraform native implicit dependency. Nothing else needs to be done from your end.
C. This is not possible to control in terraform . Terraform will take care of it in a native way , and create a dependency graph that is best suited for the parallel resource creation.
D. Create 2 separate terraform config scripts , and run them one by one , 1 for s3 bucket , and another for IAM role , run the S3 bucket script first.
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
Implicit dependency works only if there is some reference of one resource to another. Explicit dependency is the option here.

187)	Which of the following is the right substitute for static values that can make Terraform configuration file more dynamic and reusable?
12/26/2022 – by Mod_GuideK0 
Which of the following is the right substitute for static values that can make Terraform configuration file more dynamic and reusable?
A. Output value
B. Input parameters
C. Functions
D. Modules
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
Input variables serve as parameters for a Terraform module, allowing aspects of the module to be customized without altering the module’s own source code, and allowing modules to be shared between different configurations.

188)	What does terraform refresh command do?
12/26/2022 – by Mod_GuideK0 
What does terraform refresh command do?
A. A. terraform refresh can be used to selectively update sections of the state file, using terraform resource level addressing.
B. terraform refresh command basically updates the configuration file with the current state of the actual infrastructure
C. terraform refresh is use to change/modify the infrastructure based on the existing state file, at that moment.
D. terraform refresh can be used to selectively update sections of the state file, using terraform resource level addressing.
E. terraform refresh syncs the state file with the real world infrastructure.
HIDE ANSWERS
Correct Answer: E
Explanation/Reference:
Explanation:

189)	The canonical format may change in minor ways between Terraform versions, so after upgrading Terraform it is recommended to proactively run.
12/26/2022 – by Mod_GuideK0 
The canonical format may change in minor ways between Terraform versions, so after upgrading Terraform it is recommended to proactively run.
A. terraform fmt
B. terraform init
C. terraform validate
D. terraform plan
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:

190)	Which of the following environment variable settings is correct option for him to select.
12/26/2022 – by Mod_GuideK0 
Ric wants to enable detail logging and he wants highest verbosity of logs. Which of the following environment variable settings is correct option for him to select.
A. Set TF_LOG = DEBUG
B. Set VAR_TF = TRACE
C. Set TF_LOG = TRACE
D. Set VAR_TF_LOG = TRACE
HIDE ANSWERS
Correct Answer: C
Explanation/Reference:
Explanation:
https://www.terraform.io/docs/internals/debugging.html
191)	Which of the below commands can be used to remove the already acquired lock on the state?
12/26/2022 – by Mod_GuideK0 
You are using a terraform operation that writes state. Unfortunately automatic state unlocking has failed for that operation. Which of the below commands can be used to remove the already acquired lock on the state?
A. terraform unlock
B. terraform force-unlock
C. terraform state unlock
D. None of the above
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
Command: force-unlock
Manually unlock the state for the defined configuration.
This will not modify your infrastructure. This command removes the lock on the state for the current configuration. The behavior of this lock is dependent on the backend being used. Local state files cannot be unlocked by another process.
https://www.terraform.io/docs/commands/force-unlock.html
https://www.terraform.io/docs/state/locking.htmlTerraform has a force-unlock command to manually unlock the state if unlocking failed.
If you unlock the state when someone else is holding the lock it could cause multiple writers. Force unlock should only be used to unlock your own lock in the situation where automatic unlocking failed.
Topic 3, Exam Set C

192)	What is the standard workflow that a developer follows while working with terraform open source version?
12/26/2022 – by Mod_GuideK0 
What is the standard workflow that a developer follows while working with terraform open source version?
A. Run terraform refresh to update the terraform state , then write the terraform code , and finally run terraform apply.
B. Run terraform destroy first since you need to start from fresh every time , before running terraform apply.
C. Write terraform code , and run terraform push , to update the terraform state to the remote repo , which in turn will take care of the next steps.
D. Write the terraform code on the developer machine , run terraform plan to check the changes , and run terraform apply to provision the infra.
HIDE ANSWERS
Correct Answer: D
Explanation/Reference:
Explanation:
You do not need to run terraform refresh as terraform plan implicitly will run terraform refresh.
https://www.terraform.io/guides/core-workflow.html

193)	How does Terraform handle working with so many providers?
12/26/2022 – by Mod_GuideK0 
How does Terraform handle working with so many providers?
A. Terraform ships with all of the plugins embedded in the Terraform binary.
B. Terraform uses a plugin architecture for providers and only installs the provider plugins required by your configuration in the configuration’s working directory.
C. Terraform uses a plugin architecture for providers and only installs the provider plugins required by your configuration in a shared, system-wide plugins directory.
D. Terraform allows you to select the providers you want to support during the Terraform installation process.
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
Terraform is built on a plugin-based architecture. All providers and provisioners that are used in Terraform configurations are plugins, even the core types such as AWS and Heroku. Users of Terraform are able to write new plugins in order to support new functionality in Terraform.


194)	How to fix this?
12/26/2022 – by Mod_GuideK0 
John wants to use two different regions to deploy two different EC2 instances. He has specified two provider blocks in his providers.tf file. provider “aws” { region = “us-east-1” } provider “aws” { region = “us-west-2” } When he run terraform plan he encountered an error. How to fix this?
A. Use another provider version
B. Use alias for region = “us-west-2”
C. Use default keyword with region = “us-east-1”
D. It can not be fixed
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
195)	Matt wants to import a manually created EC2 instance into terraform so that he can manage the EC2 instance through terraform going forward.
12/26/2022 – by Mod_GuideK0 
Matt wants to import a manually created EC2 instance into terraform so that he can manage the EC2 instance through terraform going forward. He has written the configuration file of the EC2 instance before importing it to Terraform.
Following is the code: resource “aws_instance” “matt_ec2” { ami = “ami-bg2640de” instance_type = “t2.micro” vpc_security_group_ids = [“sg-6ae7d613”, “sg-53370035”] key_name = “mysecret” subnet_id = “subnet-9e3cfbc5” } The instance id of that EC2 instance is i-0260835eb7e9bd40 How he can import data of EC2 to state file?
A. terraform import aws_instance.id = i-0260835eb7e9bd40
B. terraform import i-0260835eb7e9bd40
C. terraform import aws_instance.i-0260835eb7e9bd40
D. terraform import aws_instance.matt_ec2 i-0260835eb7e9bd40
HIDE ANSWERS
Correct Answer: D
Explanation/Reference:
Explanation:
https://www.terraform.io/docs/import/usage.html

196)	What are some of the benefits of using Terraform rather than a provider’s native tooling?
12/26/2022 – by Mod_GuideK0 
In regards to deploying resources in multi-cloud environments, what are some of the benefits of using Terraform rather than a provider’s native tooling? (select three)
A. Terraform can help businesses deploy applications on multiple clouds and on-premises infrastructure.
B. Terraform is not cloud-agnostic and can be used to deploy resources across a single public cloud.
C. Terraform simplifies management and orchestration, helping operators build large-scale, multicloud infrastructure.
D. Terraform can manage cross-cloud dependencies.
HIDE ANSWERS
Correct Answer: ACD
Explanation/Reference:
Explanation:
Terraform is cloud-agnostic and allows a single configuration to be used to manage multiple providers, and to even handle cross-cloud dependencies. This simplifies management and orchestration, helping operators build large-scale multicloud infrastructures.
https://www.terraform.io/intro/use-cases.html

197)	Which of the below options allows terraform to select a specific version or tag instead of selecting the HEAD.
12/26/2022 – by Mod_GuideK0 
While using generic git repository as a module source, which of the below options allows terraform to select a specific version or tag instead of selecting the HEAD.
A. Append ref argument as module “vpc” { source = “git::https://example.com/vpc.git?ref=v1.2.0”}
B. Append version argument as module “vpc” { source = “git::https://example.com/vpc.git?version=v1.2.0”}
C. Append ref argument as module “vpc” { source = “git::https://example.com/vpc.git#ref=v1.2.0”}
D. By default, Terraform will clone and use the default branch (referenced by HEAD) in the selected repository and you can not override this.
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
By default, Terraform will clone and use the default branch (referenced by HEAD) in the selected repository. You can override this using the ref argument: module “vpc” { source = “git::https://example.com/vpc.git?ref=v1.2.0”
} The value of the ref argument can be any reference that would be accepted by the git checkout command, including branch and tag names.
https://www.terraform.io/docs/modules/sources.html


198)	Refer to the below code where developer is outputting the value of the database password but has used sensitive parameter to hide the output value in the CLI.
12/26/2022 – by Mod_GuideK0 
Refer to the below code where developer is outputting the value of the database password but has used sensitive parameter to hide the output value in the CLI. output “db_password” { value = aws_db_instance.db.password description = “The password for logging in to the database.” sensitive = true} Since sensitive is set to true, the value associated with db password will not be present in state file as plain-text?
A. False
B. True
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
Sensitive output values are still recorded in the state, and so will be visible to anyone who is able to access the state data.


199)	You have created 2 workspaces PROD and RQ
12/26/2022 – by Mod_GuideK0 
You have created 2 workspaces PROD and RQ
A. You have switched to RQA and provisioned RQA infrastructure from this workspace. Where is your state file stored?
B. terraform.tfstate.d
C. terraform.d
D. terraform.tfstate.RQA
E. terraform.tfstate
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:

200)	How can Terraform Enterprise automatically and proactively enforce this security control?
12/26/2022 – by Mod_GuideK0 
Your risk management organization requires that new AWS S3 buckets must be private and encrypted at rest. How can Terraform Enterprise automatically and proactively enforce this security control?
A. With a Sentinel policy, which runs before every apply
B. By adding variables to each TFE workspace to ensure these settings are always enabled
C. With an S3 module with proper settings for buckets
D. Auditing cloud storage buckets with a vulnerability scanning tool
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
https://docs.hashicorp.com/sentinel/intro/what
https://medium.com/hashicorp-engineering/enforcing-aws-s3-security-best-practice-usingterraform-sentinel-ddcd181ff4b7


201-300

201)	Terraform works well in Windows but a Windows server is required.
12/26/2022 – by Mod_GuideK0 
Terraform works well in Windows but a Windows server is required.
A. False
B. True
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
Terraform does not require GO language to be installed as a prerequisite and it does not require a Windows Server as well.
202)	Which of the following statements about Terraform modules is not true?
12/26/2022 – by Mod_GuideK0 
Which of the following statements about Terraform modules is not true?
A. Modules must be publicly accessible
B. Modules can be called multiple times
C. Module is a container for one or more resources
D. Modules can call other modules
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
In addition to modules from the local filesystem, Terraform can load modules from a public or private registry. Also, members of your organization might produce modules specifically crafted for your own infrastructure needs. Source: https://www.terraform.io/language/modules

203)	What is the command you can use to set an environment variable named “var1″of type String?
12/26/2022 – by Mod_GuideK0 
What is the command you can use to set an environment variable named “var1″of type String?
A. export TF_VAR_VAR1
B. set TF_VAR_var1
C. variable “var1” { type = “string”}
D. export TF_VAR_var1
HIDE ANSWERS
Correct Answer: D
Explanation/Reference:
Explanation:
The environment variable must be in the format TF_VAR_name, so for the
https://www.terraform.io/docs/commands/environment-variables.html#tf_var_name
204)	Which of the following Terraform files should be ignored by Git when committing code to a repo?
12/26/2022 – by Mod_GuideK0 
Which of the following Terraform files should be ignored by Git when committing code to a repo?
(select Three)
A. Files named exactly terraform.tfvars or terraform.tfvars.json.
B. Any files with names ending in .auto.tfvars or .auto.tfvars.json.
C. input.tf
D. terraform.tfstate
E. output.tf
HIDE ANSWERS
Correct Answer: ABD
Explanation/Reference:
Explanation:
The .gitignore file should be configured to ignore Terraform files that either contain sensitive data or are not required to save.
Terraform state (terraform.tfstate) can contain sensitive data, depending on the resources in use and your definition of “sensitive.” The state contains resource IDs and all resource attributes. For resources such as databases, this may contain initial passwords.
When using local state, state is stored in plain-text JSON files.
The terraform.tfvars file may contain sensitive data, such as passwords or IP addresses of an environment that you may not want to share with others.

205)	Which one of the below you will choose?
12/26/2022 – by Mod_GuideK0 
You want terraform plan and apply to be executed in Terraform Cloud’s run environment but the output is to be streamed locally. Which one of the below you will choose?
A. Local Backends
B. This can be done using any of the local or remote backends
C. Remote Backends
D. Terraform Backends
HIDE ANSWERS
Correct Answer: C
Explanation/Reference:
Explanation:
The remote backend stores Terraform state and may be used to run operations in Terraform Cloud.
When using full remote operations, operations like terraform plan or terraform apply can be executed in Terraform Cloud’s run environment, with log output streaming to the local terminal.
Remote plans and applies use variable values from the associated Terraform Cloud workspace.
https://www.terraform.io/docs/backends/types/remote.html

206)	What is the default backend for Terraform?
12/26/2022 – by Mod_GuideK0 
What is the default backend for Terraform?
A. consul
B. gcs
C. local
D. etcd
HIDE ANSWERS
Correct Answer: C
Explanation/Reference:
Explanation:
By default, Terraform uses the “local” backend, which is the normal behavior of Terraform you’re used to.
https://www.terraform.io/docs/backends/index.html
207)	By default, a defined provisioner is a creation-time provisioner.
12/26/2022 – by Mod_GuideK0 
By default, a defined provisioner is a creation-time provisioner.
A. True
B. False
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
https://www.terraform.io/docs/provisioners/index.html
208)	You want to use different AMI images for different regions and for the purpose you have defined following code block.
12/26/2022 – by Mod_GuideK0 
You want to use different AMI images for different regions and for the purpose you have defined following code block.
1. variable “images”
2. {
3. type = “map”
4.
5. default = {
6. us-east-1 = “image-1234”
7. us-west-2 = “image-4567”
8. us-west-1 = “image-4589”
9. }
10. }
What of the following approaches needs to be followed in order to select image-4589?
A. var.images[“us-west-1”]
B. var.images[3]
C. var.images[2]
D. lookup(var.images[“us-west-1”]
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
209)	Which of the below terraform commands do not run terraform refresh implicitly before taking actual action of the command?
12/26/2022 – by Mod_GuideK0 
Which of the below terraform commands do not run terraform refresh implicitly before taking actual action of the command?
A. terraform apply
B. terraform destroy
C. terraform init
D. terraform import
E. terraform plan
HIDE ANSWERS
Correct Answer: CD
Explanation/Reference:
Explanation:
https://www.terraform.io/docs/commands/refresh.html

210)	What must you do in order to prepare to manage these resources using Terraform?
12/26/2022 – by Mod_GuideK0 
You want to use terraform import to start managing infrastructure that was not originally provisioned through infrastructure as code. Before you can import the resource’s current state, what must you do in order to prepare to manage these resources using Terraform?
A. Run terraform refresh to ensure that the state file has the latest information for existing resources.
B. Update the configuration file to include the new resources.
C. Shut down or stop using the resources being imported so no changes are inadvertently missed.
D. Modify the Terraform state file to add the new resources.
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
The current implementation of Terraform import can only import resources into the state. It does not generate configuration. A future version of Terraform will also generate configuration.
Because of this, prior to running terraform import it is necessary to write manually a resource configuration block for the resource, to which the imported object will be mapped.
The terraform import command is used to import existing infrastructure.
To import a resource, first write a resource block for it in our configuration, establishing the name by which it will be known to Terraform.
Example: resource “aws_instance” “import_example” { # …instance configuration…
}
Now terraform import can be run to attach an existing instance to this resource configuration.
$ terraform import aws_instance.import_example i-03efafa258104165f aws_instance.import_example: Importing from ID “i-03efafa258104165f”… aws_instance.import_example: Import complete! Imported aws_instance (ID: i- 03efafa258104165f) aws_instance.import_example: Refreshing state… (ID: i-03efafa258104165f) Import successful! The resources that were imported are shown above. These resources are now in your Terraform state and will henceforth be managed by Terraform.
This command locates the AWS instance with ID i-03efafa258104165f (which has been created outside Terraform) and attaches its existing settings, as described by the EC2 API, to the name aws_instance.import_example in the Terraform state.

211)	Terraform state subcommands such as list are read-only commands, do read-only commands create state backup files?
12/26/2022 – by Mod_GuideK0 
terraform state subcommands such as list are read-only commands, do read-only commands create state backup files?
A. Yes
B. No
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
Subcommands that are read-only (such as list) do not write any backup files since they aren’t modifying the state.
All terraform state subcommands that modify the state write backup files. The path of these backup file can be controlled with -backup.
https://www.terraform.io/docs/commands/state/index.html#backups

212)	What is the purpose of using the local-exec provisioner?
12/26/2022 – by Mod_GuideK0 
What is the purpose of using the local-exec provisioner? (Select Two)
A. To invoke a local executable.
B. Executes a command on the resource to invoke an update to the Terraform state.
C. To execute one or more commands on the machine running Terraform.
D. Ensures that the resource is only executed in the local infrastructure where Terraform is deployed.
HIDE ANSWERS
Correct Answer: AC
Explanation/Reference:
Explanation:
The local-exec provisioner invokes a local executable after a resource is created. This invokes a process on the machine running Terraform, not on the resource.
Note that even though the resource will be fully created when the provisioner is run, there is no guarantee that it will be in an operable state – for example system services such as sshd may not be started yet on compute resources.
Example usage resource “aws_instance” “web” { # … provisioner “local-exec” { command = “echo ${aws_instance.web.private_ip} >> private_ips.txt”
}
} Note: Provisioners should only be used as a last resort. For most common situations there are better alternatives.
https://www.terraform.io/docs/provisioners/local-exec.html

213)	Which of the following represents a feature of Terraform Cloud that is NOT free to customers?
12/26/2022 – by Mod_GuideK0 
Which of the following represents a feature of Terraform Cloud that is NOT free to customers?
A. Roles and Team Management
B. WorkSpace Management
C. Private Module Registry
D. VCS Integration
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
Role Based Access Controls (RBAC) for controlling permissions for who has access to what configurations within an organization and it is not free to customers.
https://www.hashicorp.com/products/terraform/pricing/

214)	Which of the following command can be used to view the specified version constraints for all providers used in the current configuration.
12/26/2022 – by Mod_GuideK0 
Which of the following command can be used to view the specified version constraints for all providers used in the current configuration.
A. terraform providers
B. terraform state show
C. terraform provider
D. terraform plan
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
Use the terraform providers command to view the specified version constraints for all providers used in the current configuration.
https://www.terraform.io/docs/configuration/providers.html

215)	 Which of the following best describes the default local backend?
12/26/2022 – by Mod_GuideK0 
Which of the following best describes the default local backend?
A. The local backend is where Terraform Enterprise stores logs to be processed by an log collector.
B. The local backend stores state on the local filesystem, locks the state using system APIs, and performs operations locally.
C. The local backend is the directory where resources deployed by Terraform have direct access to in order to update their current state.
D. The local backend is how Terraform connects to public cloud services, such as AWS, Azure, or GCP.
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
The local backend stores state on the local filesystem, locks that state using system APIs, and performs operations locally. terraform { backend “local” { path = “relative/path/to/terraform.tfstate”
}}
https://www.terraform.io/docs/backends/types/local.html
216)	Which of the following type of variable allows multiple values of several distinct types to be grouped together as a single value?
12/26/2022 – by Mod_GuideK0 
Which of the following type of variable allows multiple values of several distinct types to be grouped together as a single value?
A. Map
B. Object
C. Tuple
D. List
HIDE ANSWERS
Correct Answer: BC
Explanation/Reference:
Explanation:
Structural type of variable allows multiple values of several distinct types to be grouped together as a single value. They require a schema as an argument, to specify which types are allowed for which elements.
https://www.terraform.io/docs/configuration/types.html

217)	Terraform import command can import resources into modules as well directly into the root of your state.
12/26/2022 – by Mod_GuideK0 
Terraform import command can import resources into modules as well directly into the root of your state.
A. True
B. False
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
Import will find the existing resource from ID and import it into your Terraform state at the given ADDRESS. ADDRESS must be a valid resource address. Because any resource address is valid, the import command can import resources into modules as well directly into the root of your state.
Terraform is able to import existing infrastructure. This allows us take resources we’ve created by some other means (i.e. via console) and bring it under Terraform management.
This is a great way to slowly transition infrastructure to Terraform.
The terraform import command is used to import existing infrastructure.
To import a resource, first write a resource block for it in our configuration, establishing the name by which it will be known to Terraform. For example: resource “aws_instance” “import_example” { # …instance configuration…
}
Now terraform import can be run to attach an existing instance to this resource configuration:
$ terraform import aws_instance.import_example i-03efafa258104165f aws_instance.import_example: Importing from ID “i-03efafa258104165f”… aws_instance.import_example: Import complete! Imported aws_instance (ID: i- 03efafa258104165f) aws_instance.import_example: Refreshing state… (ID: i-03efafa258104165f) Import successful! The resources that were imported are shown above. These resources are now in your Terraform state and will henceforth be managed by Terraform.
This command locates the AWS instance with ID i-03efafa258104165f (which has been created outside Terraform) and attaches its existing settings, as described by the EC2 API, to the name aws_instance.import_example in the Terraform state.
As a result of the above command, the resource is recorded in the state file. We can now run terraform plan to see how the configuration compares to the imported resource, and make any adjustments to the configuration to align with the current (or desired) state of the imported object.
https://www.terraform.io/docs/commands/import.html

218)	What programming language will need to use to write the fix?
12/26/2022 – by Mod_GuideK0 
You want to get involved in the development of Terraform. As this is an open source project, you would like to contribute a fix for an open issue of Terraform. What programming language will need to use to write the fix?
A. It depends on which command issue related to.
B. Python
C. Go
D. Java
HIDE ANSWERS
Correct Answer: C
Explanation/Reference:
Explanation:
Basic programming knowledge. Terraform and Terraform Plugins are written in the Go programming language, but even if you’ve never written a line of Go before, you’re still welcome to take a dive into the code and submit patches. The community is happy to assist with code reviews and offer guidance specific to Go.
219)	How will you use it for provisioning infrastructure?
12/26/2022 – by Mod_GuideK0 
You have created a custom variable definition file testing.tfvars. How will you use it for provisioning infrastructure?
A. terraform apply -var-state-file =”testing.tfvars”
B. terraform plan -var-file=”testing.tfvar”
C. terraform apply -var-file=”testing.tfvars”
D. terraform apply var-file=”testing.tfvars”
HIDE ANSWERS
Correct Answer: C
Explanation/Reference:
Explanation:
https://www.terraform.io/docs/configuration/variables.html
220)	Which one of the following command will rewrite Terraform configuration files to a canonical format and style.
12/26/2022 – by Mod_GuideK0 
Which one of the following command will rewrite Terraform configuration files to a canonical format and style.
A. terraform graph -h
B. terraform init
C. terraform graph
D. terraform fmt
HIDE ANSWERS
Correct Answer: D
Explanation/Reference:
Explanation:
The terraform fmt command is used to rewrite Terraform configuration files to a canonical format and style. This command applies a subset of the Terrra Terraform language style conventions, along with other minor adjustments for readability.

221)	When using remote state, state is only ever held in memory when used by Terraform.
12/26/2022 – by Mod_GuideK0 
When using remote state, state is only ever held in memory when used by Terraform.
A. False
B. True
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
222)	If you enable TF_LOG = DEBUG, the log will be stored in syslog.
12/26/2022 – by Mod_GuideK0 
If you enable TF_LOG = DEBUG, the log will be stored in syslog.log file in the currect directory.
A. False
B. True
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
https://www.terraform.io/docs/internals/debugging.html
223)	How can you ensure that the engineering team who has access to git repo will not create any noncompliant resources that might lead to a security audit failure in future.
12/26/2022 – by Mod_GuideK0 
How can you ensure that the engineering team who has access to git repo will not create any noncompliant resources that might lead to a security audit failure in future. your team is using Hashicorp Terraform Enterprise Edition.
A. Use Terraform OSS Sentinel Lite version , which will save cost , since there is no charge for OSS , but it can still check for most non-compliant rules using Policy-As-Code.
B. Implement a review process where every code will be reviewed before merging to the master branch.
C. Since your team is using Hashicorp Terraform Enterprise Edition , enable Sentinel , and write Policy-As-Code rules that will check for non-compliant resource provisioning , and prevent/report them.
D. Create a design /security document (in PDF) and share to the team , and ask them to always follow that document , and never deviate from it.
HIDE ANSWERS
Correct Answer: C
Explanation/Reference:
Explanation:
https://www.terraform.io/docs/cloud/sentinel/index.html

224)	Which one of the following will run echo 0 and echo 1 on a newly created host?
12/26/2022 – by Mod_GuideK0 
Which one of the following will run echo 0 and echo 1 on a newly created host?
A. provisioner “local-exec” { command = “echo 0” command = “echo 1”
}
B. provisioner “remote-exec” { inline = [ echo 0, echo 1 ]
}
C. provisioner “remote-exec” { command = “${echo 0}” command = “${echo 1}”
}
D. provisioner “remote-exec” { inline = [ “echo 0”, “echo 1” ]
}
HIDE ANSWERS
Correct Answer: D
Explanation/Reference:
Explanation: remote-exec Provisioner Example usage resource “aws_instance” “web” { # … provisioner “remote-exec” { inline = [ “puppet apply”, “consul join ${aws_instance.web.private_ip}”, ]
}}
Explanation: remote-exec Provisioner Example usage resource “aws_instance” “web” { # … provisioner “remote-exec” { inline = [ “puppet apply”, “consul join ${aws_instance.web.private_ip}”, ]
}}

225)	Which of the following best describes a Terraform provider?
12/26/2022 – by Mod_GuideK0 
Which of the following best describes a Terraform provider?
A. A plugin that Terraform uses to translate the API interactions with the service or provider.
B. Serves as a parameter for a Terraform module that allows a module to be customized.
C. Describes an infrastructure object, such as a virtual network, compute instance, or other components.
D. A container for multiple resources that are used together.
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
A provider is responsible for understanding API interactions and exposing resources. Providers generally are an IaaS (e.g. Alibaba Cloud, AWS, GCP, Microsoft Azure, OpenStack), PaaS (e.g. Heroku), or SaaS services (e.g. Terraform Cloud, DNSimple, Cloudflare).
https://www.terraform.io/docs/providers/index.html

226)	Terraform has detailed logs which can be enabled by setting the _________ environmental variable.
12/26/2022 – by Mod_GuideK0 
Terraform has detailed logs which can be enabled by setting the _________ environmental variable.
A. TF_TRACE
B. TF_DEBUG
C. TF_LOG
D. TF_INFO
HIDE ANSWERS
Correct Answer: C
Explanation/Reference:
Explanation:
Terraform has detailed logs that can be enabled by setting the TF_LOG environment variable to any value. This will cause detailed logs to appear on stderr.
You can set TF_LOG to one of the log levels TRACE, DEBUG, INFO, WARN or ERROR to change the verbosity of the logs. TRACE is the most verbose and it is the default if TF_LOG is set to something other than a log level name.
https://www.terraform.io/docs/internals/debugging.html

227)	The current implementation of Terraform import can only import resources into the state.
12/26/2022 – by Mod_GuideK0 
The current implementation of Terraform import can only import resources into the state. It does not generate configuration.
A. False
B. True
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
The current implementation of Terraform import can only import resources into the state. It does not generate configuration. A future version of Terraform will also generate configuration.
Because of this, prior to running terraform import it is necessary to write manually a resource configuration block for the resource, to which the imported object will be mapped.
While this may seem tedious, it still gives Terraform users an avenue for importing existing resources.
https://www.terraform.io/docs/import/index.html#currently-state-only
228)	Workspaces in Terraform provides similar functionality in the open-source, Terraform Cloud, and Enterprise versions of Terraform.
12/26/2022 – by Mod_GuideK0 
Workspaces in Terraform provides similar functionality in the open-source, Terraform Cloud, and Enterprise versions of Terraform.
A. True
B. False
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
https://www.terraform.io/docs/cloud/migrate/workspaces.htmlWorkspaces, managed with the terraform workspace command, aren’t the same thing as TerraformCloud’s workspaces. Terraform Cloud workspaces act more like completelyseparate workingdirectories; CLI workspaces are just alternate state files.

229)	When TF_LOG_PATH is set, TF_LOG must be set in order for any logging to be enabled.
12/26/2022 – by Mod_GuideK0 
When TF_LOG_PATH is set, TF_LOG must be set in order for any logging to be enabled.
A. False
B. True
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
TF_LOG_PATH specifies where the log should persist its output to. Note that even when TF_LOG_PATH is set, TF_LOG must be set in order for any logging to be enabled.
For example, to always write the log to the directory you’re currently running terraform from: export TF_LOG_PATH=./terraform.log export TF_LOG=TRACE
230)	What does terrafom plan do ?
12/26/2022 – by Mod_GuideK0 
What does terrafom plan do ?
A. Create an execution plan by evaluating the difference between configuration file and state file.
B. Performs a refresh, unless explicitly disabled, and then apply the changes that are necessary to achieve the desired state specified in the configuration files.
C. Create an execution plan by evaluating the difference between configuration file and actual infrastructure.
D. Checks whether the execution plan for a set of changes matches your expectations by making changes to real resources or to the state.
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
231)	Terraform refresh will update the state file?
12/26/2022 – by Mod_GuideK0 
terraform refresh will update the state file?
A. True
B. False
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
The terraform refresh command is used to reconcile the state Terraform knows about (via its state file) with the real-world infrastructure. This can be used to detect any drift from the last-known state, and to update the state file.
This does not modify infrastructure, but does modify the state file. If the state is changed, this may cause changes to occur during the next plan or apply.
232)	What allows you to conveniently switch between multiple instances of a single configuration within its single backend?
12/26/2022 – by Mod_GuideK0 
What allows you to conveniently switch between multiple instances of a single configuration within its single backend?
A. Local backends
B. Providers
C. Remote backends
D. Workspaces
HIDE ANSWERS
Correct Answer: D
Explanation/Reference:
Explanation:
Named workspaces allow conveniently switching between multiple instances of a single configuration within its single backend. … A common use for multiple workspaces is to create a parallel, distinct copy of a set of infrastructure in order to test a set of changes before modifying the main production infrastructure.
Workspaces, allowing multiple states to be associated with a single configuration. The configuration still has only one backend, but multiple distinct instances of that configuration to be deployed without configuring a new backend or changing authentication credentials.
https://www.terraform.io/docs/state/workspaces.html

233)	Which Terraform command will force a marked resource to be destroyed and recreated on the next apply?
12/26/2022 – by Mod_GuideK0 
234)	Which Terraform command will force a marked resource to be destroyed and recreated on the next apply?
A. terraform fmt
B. terraform destroy
C. terraform taint
D. terraform refresh
HIDE ANSWERS
Correct Answer: C
Explanation/Reference:
Explanation:
The terraform taint command manually marks a Terraform-managed resource as tainted, forcing it to be destroyed and recreated on the next apply.
This command will not modify infrastructure, but does modify the state file in order to mark a resource as tainted. Once a resource is marked as tainted, the next plan will show that the resource will be destroyed and recreated and the next apply will implement this change.
Forcing the recreation of a resource is useful when you want a certain side effect of recreation that is not visible in the attributes of a resource. For example: re-running provisioners will cause the node to be different or rebooting the machine from a base image will cause new startup scripts to run.
Note that tainting a resource for recreation may affect resources that depend on the newly tainted resource. For example, a DNS resource that uses the IP address of a server may need to be modified to reflect the potentially new IP
address of a tainted server. The plan command will show this if this is the case.
https://www.terraform.io/docs/commands/taint.html

234)	Provisioners should only be used as a last resort.
12/26/2022 – by Mod_GuideK0 
Provisioners should only be used as a last resort.
A. False
B. True
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
Provisioners are a Last Resort
Terraform includes the concept of provisioners as a measure of pragmatism, knowing that there will always be certain behaviors that can’t be directly represented in Terraform’s declarative model.
However, they also add a considerable amount of complexity and uncertainty to Terraform usage.
Firstly, Terraform cannot model the actions of provisioners as part of a plan because they can in principle take any action. Secondly, successful use of provisioners requires coordinating many more details than Terraform usage usually requires: direct network access to your servers, issuing Terraform credentials to log in, making sure that all of the necessary external software is installed, etc.
The following sections describe some situations which can be solved with provisioners in principle, but where better solutions are also available. We do not recommend using provisioners for any of the use-cases described in the following sections.
Even if your specific use-case is not described in the following sections, we still recommend attempting to solve it using other techniques first, and use provisioners only if there is no other option.
https://www.terraform.io/docs/provisioners/index.html
235)	Which of the below are paid features of Terraform Cloud?
12/26/2022 – by Mod_GuideK0 
Which of the below are paid features of Terraform Cloud?
A. Full API Coverage
B. Secure variable Storage
C. Roles/ Team management
D. Cost Estimation
E. Private Module Registry
F. Sentinel policies
HIDE ANSWERS
Correct Answer: CDF
Explanation/Reference:
Explanation:
https://www.hashicorp.com/products/terraform/pricing/
236)	Where is this data stored?
12/26/2022 – by Mod_GuideK0 
Terraform must track metadata such as resource dependencies. Where is this data stored?
A. workspace
B. backend
C. state file
D. metadata store
HIDE ANSWERS
Correct Answer: C
Explanation/Reference:
Explanation:
Terraform typically uses the configuration to determine dependency order. However, when you delete a resource from a Terraform configuration, Terraform must know how to delete that resource.
Terraform can see that a mapping exists for a resource not in your configuration and plan to destroy.
However, since the configuration no longer exists, the order cannot be determined from the configuration alone.
To ensure correct operation, Terraform retains a copy of the most recent set of dependencies within the state. Now Terraform can still determine the correct order for destruction from the state when you delete one or more items from the configuration.
https://www.terraform.io/docs/state/purpose.html#metadata

237)	Lookup retrieves the value of a single element from which of the below data type?
12/26/2022 – by Mod_GuideK0 
lookup retrieves the value of a single element from which of the below data type?
A. map
B. set
C. string
D. list
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
https://www.terraform.io/docs/configuration/functions/lookup.html

238)	When some or all of the arguments are omitted, we call this a _____________.
12/26/2022 – by Mod_GuideK0 
You do not need to specify every required argument in the backend configuration. Omitting certain arguments may be desirable to avoid storing secrets, such as access keys, within the main configuration. When some or all of the arguments are omitted, we call this a _____________.
A. First Time Configuration
B. Default Configuration
C. Changing Configuration
D. Partial Configuration
E. Incomplete Configuration
HIDE ANSWERS
Correct Answer: D
Explanation/Reference:
Explanation:
You do not need to specify every required argument in the backend configuration. Omitting certain arguments may be desirable to avoid storing secrets, such as access keys, within the main configuration. When some or all of the arguments are omitted, we call this a partial configuration.
With a partial configuration, the remaining configuration arguments must be provided as part of the initialization process. There are several ways to supply the remaining arguments:
* Interactively: Terraform will interactively ask you for the required values, unless interactive input is disabled. Terraform will not prompt for optional values.
* File: A configuration file may be specified via the init command line. To specify a file, use the – backend-config=PATH option when running terraform init. If the file contains secrets it may be kept in a secure data store, such as Vault, in which case it must be downloaded to the local disk before running Terraform.
* Command-line key/value pairs: Key/value pairs can be specified via the init command line. Note that many shells retain command-line flags in a history file, so this isn’t recommended for secrets. To specify a single key/value pair, use the -backend-config=”KEY=VALUE” option when running terraform init.
https://www.terraform.io/docs/backends/config.html#partial-configuration
239)	True or False: A list(.
12/26/2022 – by Mod_GuideK0 
True or False: A list(…) contain a number of values of the same type while an object(…) can contain a number of values of different types.
A. False
B. True
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
Collection Types
A collection type allows multiple values of one other type to be grouped together as a single value.
The type of value within a collection is called its element type. All collection types must have an element type, which is provided as the argument to their constructor.
For example, the type list(string) means “list of strings”, which is a different type than list(number), a list of numbers. All elements of a collection must always be of the same type.
The three kinds of collection type in the Terraform language are:
* list(…): a sequence of values identified by consecutive whole numbers starting with zero.
The keyword list is a shorthand for list(any), which accepts any element type as long as every element is the same type. This is for compatibility with older configurations; for new code, we recommend using the full form.
* map(…): a collection of values where each is identified by a string label.
The keyword map is a shorthand for map(any), which accepts any element type as long as every element is the same type. This is for compatibility with older configurations; for new code, we recommend using the full form.
* set(…): a collection of unique values that do not have any secondary identifiers or ordering.
https://www.terraform.io/docs/configuration/types.htmlStructural TypesA structural type allows multiple values of several distinct types to be grouped together as a single value. Structural types require a schema as an argument, to specify which types are allowed for which elements.
The two kinds of structural type in the Terraform language are:
* object(…): a collection of named attributes that each have their own type.
The schema for object types is { <KEY> = <TYPE>, <KEY> = <TYPE>, … } — a pair of curly braces containing a comma-separated series of <KEY> = <TYPE> pairs. Values that match the object type must contain all of the specified keys, and the value for each key must match its specified type.
(Values with additional keys can still match an object type, but the extra attributes are discarded during type conversion.)
* tuple(…): a sequence of elements identified by consecutive whole numbers starting with zero, where each element has its own type.
The schema for tuple types is [<TYPE>, <TYPE>, …] — a pair of square brackets containing a commaseparated series of types. Values that match the tuple type must have exactly the same number of elements (no more and no fewer), and the value in each position must match the specified type for that position.
For example: an object type of object({ name=string, age=number }) would match a value like the following:
{ name = “John” age = 52
} Also, an object type of object({ id=string, cidr_block=string }) would match the object produced by a reference to an aws_vpc resource, like aws_vpc.example_vpc; although the resource has additional attributes, they would be discarded during type conversion.
Finally, a tuple type of tuple([string, number, bool]) would match a value like the following:
[“a”, 15, true]
https://www.terraform.io/docs/configuration/types.html

240)	What is the way this type of configuration can be managed easily?
12/26/2022 – by Mod_GuideK0 
ABC Enterprise has recently tied up with multiple small organizations for exchanging database information. Due to this, the firewall rules are increasing and are more than 100 rules. This is leading firewall configuration file that is difficult to manage. What is the way this type of configuration can be managed easily?
A. Terraform Backends
B. Terraform Functions
C. Dynamic Blocks
D. Terraform Expression
HIDE ANSWERS
Correct Answer: C
Explanation/Reference:
Explanation:
241)	The terraform init command is always safe to run multiple times, to bring the working directory up to date with changes in the configuration.
12/26/2022 – by Mod_GuideK0 
The terraform init command is always safe to run multiple times, to bring the working directory up to date with changes in the configuration. Though subsequent runs may give errors, this command will never delete your existing configuration or state.
A. False
B. True
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
https://www.terraform.io/docs/commands/init.html
242)	Environment variables can be used to set variables.
12/26/2022 – by Mod_GuideK0 
Environment variables can be used to set variables. The environment variables must be in the format “____”_<variablename>. Select the correct prefix string from the following list.
A. TF_CLI_ARGS
B. TF_VAR
C. TF_VAR_
D. TF_VAR_ENV
HIDE ANSWERS
Correct Answer: C
Explanation/Reference:
Explanation:
Environment variables can be used to set variables. The environment variables must be in the format TF_VAR_name and this will be checked last for a value. For example: export TF_VAR_region=us-west-1 export TF_VAR_ami=ami-049d8641 export TF_VAR_alist='[1,2,3]’ export TF_VAR_amap='{ foo = “bar”, baz = “qux” }’
https://www.terraform.io/docs/commands/environment-variables.html
243)	You have declared a variable name my_var in terraform configuration without a value associated with it.
12/26/2022 – by Mod_GuideK0 
You have declared a variable name my_var in terraform configuration without a value associated with it. variable my_var {} After running terraform plan it will show an error as variable is not defined.
A. True
B. False
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
Input variables are usually defined by stating a name, type and a default value. However, the type and default values are not strictly necessary. Terraform can deduct the type of the variable from the default or input value.
Variables can be predetermined in a file or included in the command-line options. As such, the simplest variable is just a name while the type and value are selected based on the input. variable “variable_name” {} terraform apply -var variable_name=”value” The input variables, like the one above, use a couple of different types: strings, lists, maps, and boolean. Here are some examples of how each type are defined and used.
String
Strings mark a single value per structure and are commonly used to simplify and make complicated values more user-friendly. Below is an example of a string variable definition. variable “template” { type = string default = “01000000-0000-4000-8000-000030080200”
} A string variable can then be used in resource plans. Surrounded by double quotes, string variables are a simple substitution such as the example underneath. storage = var.template List Another type of Terraform variables lists. They work much like a numbered catalogue of values. Each value can be called by their corresponding index in the list. Here is an example of a list variable definition. variable “users” { type = list default = [“root”, “user1”, “user2”]
} Lists can be used in the resource plans similarly to strings, but you’ll also need to denote the index of the value you are looking for. username = var.users[0] Map Maps are a collection of string keys and string values. These can be useful for selecting values based on predefined parameters such as the server configuration by the monthly price. variable “plans” { type = map default = { “5USD” = “1xCPU-1GB” “10USD” = “1xCPU-2GB” “20USD” = “2xCPU-4GB”
}} You can access the right value by using the matching key. For example, the variable below would set the plan to “1xCPU-1GB”. plan = var.plans[“5USD”] The values matching to their keys can also be used to look up information in other maps. For example, underneath is a shortlist of plans and their corresponding storage sizes. variable “storage_sizes” { type = map default = { “1xCPU-1GB” = “25” “1xCPU-2GB” = “50” “2xCPU-4GB” = “80”
}} These can then be used to find the right storage size based on the monthly price as defined in the previous example. size = lookup(var.storage_sizes, var.plans[“5USD”]) Boolean The last of the available variable type is boolean. They give the option to employ simple true or false values. For example, you might wish to have a variable that decides when to generate the root user password on a new deployment. variable “set_password” { default = false
} The above example boolean can be used similarly to a string variable by simply marking down the correct variable. create_password = var.set_password By default, the value is set to false in this example. However, you can overwrite the variable at deployment by assigning a different value in a command-line variable. terraform apply -var set_password=”true”

244)	Which of the following clouds does not have a provider maintained HashiCorp?
12/26/2022 – by Mod_GuideK0 
Which of the following clouds does not have a provider maintained HashiCorp?
A. IBM Cloud
B. DigitalOcean
C. OpenStack
D. AWS
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
IBM Cloud does not have a provider maintained by HashiCorp, although IBM Cloud does maintain their own Terraform provider.
https://www.terraform.io/docs/providers/index.html
245)	Terraform refresh command will not modify infrastructure, but does modify the state file.
12/26/2022 – by Mod_GuideK0 
terraform refresh command will not modify infrastructure, but does modify the state file.
A. True
B. False
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
The terraform refresh command is used to reconcile the state Terraform knows about (via its state file) with the real-world infrastructure. This can be used to detect any drift from the last-known state, and to update the state file. This does not modify infrastructure, but does modify the state file.
https://www.terraform.io/docs/commands/refresh.html
246)	Please identify the offerings which are unique to Terraform Enterprise, and not available in either Terraform OSS, or Terraform Cloud.
12/26/2022 – by Mod_GuideK0 
Please identify the offerings which are unique to Terraform Enterprise, and not available in either Terraform OSS, or Terraform Cloud. Select four.
A. Audit Logs
B. Private Network Connectivity
C. VCS Integration
D. Sentinel
E. Clustering
HIDE ANSWERS
Correct Answer: ABE
Explanation/Reference:
Explanation:
https://www.hashicorp.com/products/terraform/pricing/

247)	Which of the below configuration file formats are supported by Terraform?
12/26/2022 – by Mod_GuideK0 
Which of the below configuration file formats are supported by Terraform? (Select TWO)
A. Node
B. JSON
C. Go
D. YAML
E. HCL
HIDE ANSWERS
Correct Answer: BE
Explanation/Reference:
Explanation:
Terraform supports both HashiCorp Configuration Language (HCL) and JSON formats for configurations.
https://www.terraform.io/docs/configuration/
248)	The Terraform language does not support user-defined functions, and so only the functions built in to the language are available for use.
12/26/2022 – by Mod_GuideK0 
The Terraform language does not support user-defined functions, and so only the functions built in to the language are available for use.
A. False
B. True
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
https://www.terraform.io/docs/configuration/functions.html

249)	Terraform init can indeed be run only a few times, because, every time terraform init will initialize the project
12/26/2022 – by Mod_GuideK0 
Terraform init can indeed be run only a few times, because, every time terraform init will initialize the project , and download all plugins from the internet repository , regardless of whether they were present or not , and this increases the waiting time
A. True
B. False
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
Re-running init with modules already installed will install the sources for any modules that were added to configuration since the last init, but will not change any already-installed modules. Use – upgrade to override this behavior, updating all modules to the latest available source code.
https://www.terraform.io/docs/commands/init.html

250)	If a module declares a variable with a default, that variable must also be defined within the module.
12/26/2022 – by Mod_GuideK0 
If a module declares a variable with a default, that variable must also be defined within the module.
A. True
B. False
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
Topic 2, Exam Set B

251)	What must you do to pass the value to a child module in the configuration?
12/26/2022 – by Mod_GuideK0 
You have declared an input variable called environment in your parent module. What must you do to pass the value to a child module in the configuration?
A. Add node_count = var.node_count
B. Declare the variable in a terraform.tfvars file
C. Declare a node_count input variable for child module
D. Nothing, child modules inherit variables of parent module
HIDE ANSWERS
Correct Answer: C
Explanation/Reference:
Explanation:
“That module may call other modules and connect them together by passing output values from one to input values of another.” https://www.terraform.io/language/modules/develop
252)	What type of block is used to construct a collection of nested configuration blocks?
02/26/2022 – by Mod_GuideK0 
What type of block is used to construct a collection of nested configuration blocks?
A. for_each
B. repeated
C. nesting
D. dynamic
HIDE ANSWERS
Correct Answer: D
Explanation/Reference:
Reference: https://www.hashicorp.com/blog/hashicorp-terraform-0-12-preview-for-and-for-each
253)	Which of the following is allowed as a Terraform variable name?
02/26/2022 – by Mod_GuideK0 
Which of the following is allowed as a Terraform variable name?
A. count
B. name
C. source
D. version
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Reference: https://www.terraform.io/docs/language/values/variables.html

254)	Terraform validate reports syntax check errors from which of the following scenarios?
02/26/2022 – by Mod_GuideK0 
Terraform validate reports syntax check errors from which of the following scenarios?
A. Code contains tabs indentation instead of spaces
B. There is missing value for a variable
C. The state files does not match the current infrastructure
D. None of the above
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Reference: http://man.hubwiz.com/docset/Terraform.docset/Contents/Resources/Documents/docs/commands/validate.html

255)	Terraform provisioners that require authentication can use the_block.
02/26/2022 – by Mod_GuideK0 
Terraform provisioners that require authentication can use the_block.
A. connection
B. credentials
C. secrets
D. ssh
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Reference: https://www.terraform.io/docs/language/resources/provisioners/syntax.html

256)	What do you do next to make your infrastructure match your configuration?
02/26/2022 – by Mod_GuideK2 
You just scaled your VM infrastructure and realized you set the count variable to the wrong value. You correct the value and save your change.
What do you do next to make your infrastructure match your configuration?
A. Run an apply and confirm the planned changes
B. Inspect your Terraform state because you want to change it
C. Reinitialize because your configuration has changed
D. Inspect all Terraform outputs to make sure they are correct
HIDE ANSWERS
Correct Answer: D
Explanation/Reference:
257)	Which of the following should you put into the Terraform 0.12 configuration’s provider block?
02/26/2022 – by Mod_GuideK0 
You need to constrain the GitHub provider to version 2.1 or greater.
Which of the following should you put into the Terraform 0.12 configuration’s provider block?
A. version >= 2.1
B. version ~> 2.1
C. version = “<= 2.1”
D. version = “>= 2.1”
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Reference: https://github.com/hashicorp/terraform-provider-null/issues/31
258)	A terraform apply can not__________infrastructure.
02/26/2022 – by Mod_GuideK2 
A terraform apply can not__________infrastructure.
A. change
B. destroy
C. provision
D. import
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Reference: https://www.terraform.io/docs/cli/run/index.html
259)	Terraform can only manage resource dependencies if you set them explicitly with the depends_on argument.
02/26/2022 – by Mod_GuideK1 
Terraform can only manage resource dependencies if you set them explicitly with the depends_on argument.
A. True
B. False
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Reference: https://learn.hashicorp.com/tutorials/terraform/dependencies?in=terraform/0-13

260)	What command should be used to tell Terraform to no longer manage the resource?
02/26/2022 – by Mod_GuideK0 
A fellow developer on your team is asking for some help in refactoring their Terraform code. As part of their application’s architecture, they are going to tear down an existing deoloyment managed by Terraform and deploy new. However, there is a server resource named aws_instance.ubuntu[1] they would like to keep to perform some additional analysis.
What command should be used to tell Terraform to no longer manage the resource?
A. terraform apply rm aws_instance.ubuntu[1]
B. terraform state rm aws_instance.ubuntu[1]
C. terraform plan rm aws_instance.ubuntu[1]
D. terraform delete aws_instance.ubuntu[1]
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Reference: https ://www.terraform. io/doc s/cli/commands/state/rm.html
261)	What features stops multiple admins from changing the Terraform state at the same time?
02/26/2022 – by Mod_GuideK0 
What features stops multiple admins from changing the Terraform state at the same time?
A. Version control
B. Backend types
C. Provider constraints
D. State locking
HIDE ANSWERS
Correct Answer: D
Explanation/Reference:
Reference: https://blog.gruntwork.io/how-to-manage-terraform-state-28f5697e68fa

262)	Why will the apply fail?
02/26/2022 – by Mod_GuideK0 
You write a new Terraform configuration and immediately run terraform apply in the CLI using the local backend.
Why will the apply fail?
A. Terraform needs you to format your code according to best practices first
B. Terraform needs to install the necessary plugins first
C. The Terraform CLI needs you to log into Terraform cloud first
D. Terraform requires you to manually run terraform plan first
HIDE ANSWERS
Correct Answer: C
Explanation/Reference:

263)	When you initialize Terraform, where does it cache modules from the public Terraform Module Registry?
02/26/2022 – by Mod_GuideK0 
When you initialize Terraform, where does it cache modules from the public Terraform Module Registry?
A. On disk in the /tmp directory
B. In memory
C. On disk in the .terraform sub-directory
D. They are not cached
HIDE ANSWERS
Correct Answer: C
Explanation/Reference:
Reference: https://www.terraform.io/docs/language/modules/sources.html
264)	Which backend does the Terraform CLI use by default?
02/26/2022 – by Mod_GuideK0 
Which backend does the Terraform CLI use by default?
A. Terraform Cloud
B. Consul
C. Remote
D. Local
HIDE ANSWERS
Correct Answer: D
Explanation/Reference:
Reference: https://www.terraform.io/docs/language/settings/backends/configuration.html
265)	Which of the following backends would not work?
02/26/2022 – by Mod_GuideK1 
Your DevOps team is currently using the local backend for your Terraform configuration. You would like to move to a remote backend to begin storing the state file in a central location.
Which of the following backends would not work?
A. Amazon S3
B. Artifactory
C. Git
D. Terraform Cloud
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Reference: https://secrethub.io/blog/secret-management-for-terraform/
266)	Which of these options is the most secure place to store secrets foe connecting to a Terraform remote backend?
02/26/2022 – by Mod_GuideK0 
Which of these options is the most secure place to store secrets foe connecting to a Terraform remote backend?
A. Defined in Environment variables
B. Inside the backend block within the Terraform configuration
C. Defined in a connection configuration outside of Terraform
D. None of above
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
267)	What will happen if you delete the VM using the cloud provider console, and run terraform apply again without changing any Terraform code?
02/26/2022 – by Mod_GuideK0 
You have a simple Terraform configuration containing one virtual machine (VM) in a cloud provider. You run terraform apply and the VM is created successfully.
What will happen if you delete the VM using the cloud provider console, and run terraform apply again without changing any Terraform code?
A. Terraform will remove the VM from state file
B. Terraform will report an error
C. Terraform will not make any changes
D. Terraform will recreate the VM
HIDE ANSWERS
Correct Answer: C
Explanation/Reference:

268)	How is terraform import run?
02/26/2022 – by Mod_GuideK0 
How is terraform import run?
A. As a part of terraform init
B. As a part of terraform plan
C. As a part of terraform refresh
D. By an explicit call
E. All of the above
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Reference: https://www.terraform.io/docs/cli/import/usage.html
269)	Which of the following would achieve this?
02/26/2022 – by Mod_GuideK0 
You want to know from which paths Terraform is loading providers referenced in your Terraform configuration (*.tf files). You need to enable debug messages to find this out.
Which of the following would achieve this?
A. Set the environment variable TF_LOG=TRACE
B. Set verbose logging for each provider in your Terraform configuration
C. Set the environment variable TF_VAR_log=TRACE
D. Set the environment variable TF_LOG_PATH
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Reference: https://www.terraform.io/docs/cli/config/environment-variables.html
270)	When working with Terraform Enterprise and Cloud Workspaces, conceptually you could think about them as completely separate workinc directories.
02/26/2022 – by Mod_GuideK1 
In contrast to Terraform Open Source, when working with Terraform Enterprise and Cloud Workspaces, conceptually you could think about them as completely separate workinc directories.
A. True
B. False
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
271)	How can you protect sensitive data stored in Terraform state files?
02/26/2022 – by Mod_GuideK0 
Your security team scanned some Terraform workspaces and found secrets stored in a plaintext in state files.
How can you protect sensitive data stored in Terraform state files?
A. Delete the state file every time you run Terraform
B. Store the state in an encrypted backend
C. Edit your state file to scrub out the sensitive data
D. Always store your secrets in a secrets.tfvars file.
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Reference: https://www.terraform.io/docs/language/state/sensitive-data.html

272)	How can you do this safely?
02/26/2022 – by Mod_GuideK0 
You’re building a CI/CD (continuous integration/ continuous delivery) pipeline and need to inject sensitive variables into your Terraform run.
How can you do this safely?
A. Pass variables to Terraform with a -var flag
B. Copy the sensitive variables into your Terraform code
C. Store the sensitive variables in a secure_vars.tf file
D. Store the sensitive variables as plain text in a source code repository
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:

273)	What is the name assigned by Terraform to reference this resource?
02/26/2022 – by Mod_GuideK1 
What is the name assigned by Terraform to reference this resource?
 
A. compute_instance
B. main
C. google
D. teat
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:

274)	Which command would you use?
02/26/2022 – by Mod_GuideK0 
You would like to reuse the same Terraform configuration for your development and production environments with a different state file for each.
Which command would you use?
A. terraform import
B. terraform workspace
C. terraform state
D. terraform in it
HIDE ANSWERS
Correct Answer: D
Explanation/Reference:
Reference: https://learn.hashicorp.com/tutorials/terraform/organize-configuration

275)	How can terraform plan aid in the development process?
02/26/2022 – by Mod_GuideK0 
How can terraform plan aid in the development process?
A. Validates your expectations against the execution plan without permanently modifying state
B. Initializes your working directory containing your Terraform configuration files
C. Formats your Terraform configuration files
D. Reconciles Terraform’s state against deployed resources and permanently modifies state using the current status of deployed resources
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Reference: https://github.com/hashicorp/terraform/issues/19235
276)	All standard backend types support state storage, locking, and remote operations like plan, apply and destroy.
02/26/2022 – by Mod_GuideK0 
All standard backend types support state storage, locking, and remote operations like plan, apply and destroy.
A. True
B. False
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Reference: https://www.terraform.io/docs/language/settings/backends/remote.html

277)	When running the command terraform taint against a managed resource you want to force recreation upon, Terraform will immediately destroy and recreate the resource.
02/26/2022 – by Mod_GuideK0 
When running the command terraform taint against a managed resource you want to force recreation upon, Terraform will immediately destroy and recreate the resource.
A. True
B. False
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Reference: https://www.devopsschool.com/blog/terraform-taint-and-untaint-explained-with-example-programs-and-tutorials/
278)	Which of the following is not a valid Terraform collection type?
02/26/2022 – by Mod_GuideK0 
Which of the following is not a valid Terraform collection type?
A. list
B. map
C. tree
D. set
HIDE ANSWERS
Correct Answer: C
Explanation/Reference:
Reference: https://www.terraform.io/docs/language/expressions/type-constraints.html

279)	A Terraform local value can reference other Terraform local values.
02/26/2022 – by Mod_GuideK0 
A Terraform local value can reference other Terraform local values.
A. True
B. False
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Reference: https://www.terraform.io/docs/configuration-0-11/locals.html
280)	What is the name of the default file where Terraform stores the state?
02/26/2022 – by Mod_GuideK0 
FILL BLANK
What is the name of the default file where Terraform stores the state?
Type your answer in the field provided. The text field is not case-sensitive and all variations of the correct answer are accepted.
A. Terraform.tfstate
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Reference: https://www.terraform.io/docs/language/state/index.html
281)	Which flag would you add to terraform plan to save the execution plan to a file?
02/26/2022 – by Mod_GuideK0 
FILL BLANK
Which flag would you add to terraform plan to save the execution plan to a file?
Type your answer in the field provided. The text field is not case-sensitive and all variations of the correct answer are accepted.
A. -out=FILENAME
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Reference: https://www.terraform.io/docs/cli/commands/plan.html
282)	What is terraform refresh intended to detect?
02/26/2022 – by Mod_GuideK0 
What is terraform refresh intended to detect?
A. Terraform configuration code changes
B. Empty state files
C. State file drift
D. Corrupt state files
HIDE ANSWERS
Correct Answer: C
Explanation/Reference:
Reference: https://www.hashicorp.com/blog/detecting-and-managing-drift-with-terraform
283)	Terraform provisioners can be added to any resource block.
02/26/2022 – by Mod_GuideK0 
Terraform provisioners can be added to any resource block.
A. True
B. False
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Reference: https://www.terraform.io/docs/language/resources/provisioners/syntax.html

284)	A Terraform provider is not responsible for:
02/26/2022 – by Mod_GuideK0 
A Terraform provider is not responsible for:
A. Understanding API interactions with some service
B. Provisioning infrastructure in multiple clouds
C. Exposing resources and data sources based on an AP
D. Managing actions to take based on resource differences
HIDE ANSWERS
Correct Answer: D
Explanation/Reference:
Reference: https://www.terraform.io/docs/confiquration-0-11/providers.html
285)	How would you reference the “name” value of the second instance of this fictitious resource?
02/26/2022 – by Mod_GuideK0 
How would you reference the “name” value of the second instance of this fictitious resource?
 
A. element(aws_instance.web, 2)
B. aws_instance.web[1].name
C. aws_instance.web[1]
D. aws_instance.web[2].name
E. aws_instance.web.*.name
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Reference: https://www.terraform.io/docs/confiquration-0-11/interpolation.html
286)	When does terraform apply reflect changes in the cloud environment?
02/26/2022 – by Mod_GuideK0 
When does terraform apply reflect changes in the cloud environment?
A. Immediately
B. However long it takes the resource provider to fulfill the request
C. After updating the state file
D. Based on the value provided to the -refresh command line argument
E. None of the above
HIDE ANSWERS
Correct Answer: E
Explanation/Reference:

287)	Which of these is the best practice to protect sensitive values in state files?
02/26/2022 – by Mod_GuideK0 
Which of these is the best practice to protect sensitive values in state files?
A. Blockchain
B. Secure Sockets Layer (SSL)
C. Enhanced remote backends
D. Signed Terraform providers
HIDE ANSWERS
Correct Answer: C
Explanation/Reference:
Explanation:
Use of remote backends and especially the availability of Terraform Cloud, there are now a variety of backends that will encrypt state at rest and will not store the state in cleartext on machines running.
Reference: https://www.terraform.io/docs/extend/best-practices/sensitive-state.html
288)	Terraform providers are always installed from the Internet.
02/26/2022 – by Mod_GuideK0 
Terraform providers are always installed from the Internet.
A. True
B. False
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
Terraform configurations must declare which providers they require, so that Terraform can install and use them.
Reference: https://www.terraform.io/docs/language/providers/configuration.html
289)	What command should you run to display all workspaces for the current configuration?
02/26/2022 – by Mod_GuideK0 
What command should you run to display all workspaces for the current configuration?
A. terraform workspace
B. terraform workspace show
C. terraform workspace list
D. terraform show workspace
HIDE ANSWERS
Correct Answer: C
Explanation/Reference:
Explanation: terraform workspace list The command will list all existing workspaces.
Reference: https://www.terraform.io/docs/cli/commands/workspace/list.html

290)	In Terraform 0.
02/26/2022 – by Mod_GuideK0 
In Terraform 0.13 and above, outside of the required_providers block, Terraform configurations always refer to providers by their local names.
A. True
B. False
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
Outside of the required_providers block, Terraform configurations always refer to providers by their local names.
Reference: https://www.terraform.io/docs/language/providers/requirements.html

291)	Where in your Terraform configuration do you specify a state backend?
02/26/2022 – by Mod_GuideK0 
Where in your Terraform configuration do you specify a state backend?
A. The terraform block
B. The resource block
C. The provider block
D. The datasource block
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
Backends are configured with a nested backend block within the top-level terraform block.
Reference: https://www.terraform.io/docs/language/settings/backends/configuration.html
292)	Setting the TF_LOG environment variable to DEBUG causes debug messages to be logged into syslog.
02/26/2022 – by Mod_GuideK0 
Setting the TF_LOG environment variable to DEBUG causes debug messages to be logged into syslog.
A. True
B. False
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Reference: https://wwwterraform.io/docs/internals/debugginghtml

293)	What is the name assigned by Terraform to reference this resource?
02/26/2022 – by Mod_GuideK1 
What is the name assigned by Terraform to reference this resource?
 
A. dev
B. azurerm_resource_group
C. azurerm
D. test
HIDE ANSWERS
Correct Answer: D
Explanation/Reference:
294)	What should you do to delete the newly-created VM with Terraform?
02/26/2022 – by Mod_GuideK0 
You have never used Terraform before and would like to test it out using a shared team account for a cloud provider. The shared team account already contains 15 virtual machines (VM). You develop a Terraform configuration containing one VM, perform terraform apply, and see that your VM was created successfully.
What should you do to delete the newly-created VM with Terraform?
A. The Terraform state file contains all 16 VMs in the team account. Execute terraform destroy and select the newly-created VM.
B. The Terraform state file only contains the one new VM. Execute terraform destroy.
C. Delete the Terraform state file and execute Terraform apply.
D. Delete the VM using the cloud provider console and terraform apply to apply the changes to the Terraform state file.
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:

295)	What resource meta-parameter can you use to make sure Terraform respects the dependency?
02/26/2022 – by Mod_GuideK0 
FILL BLANK
You need to specify a dependency manually.
What resource meta-parameter can you use to make sure Terraform respects the dependency?
Type your answer in the field provided. The text field is not case-sensitive and all variations of the correct answer are accepted.
A. the local_file data source
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Reference: https://www.terraform.io/docs/language/functijns/file.html

296)	What value should you enter for the ami argument in the AWS instance resource?
02/26/2022 – by Mod_GuideK0 
Examine the following Terraform configuration, which uses the data source for an AWS AMI.
What value should you enter for the ami argument in the AWS instance resource?
 
A. aws_ami.ubuntu
B. data.aws_ami.ubuntu
C. data. aws_ami. ubuntu, id
D. aws_ami.ubuntu.id
HIDE ANSWERS
Correct Answer: C
Explanation/Reference:
Explanation: resource “aws_instance” “web” { ami = data.aws_ami.ubuntu.id
Reference: https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/instance
297)	Only the user that generated a plan may apply it.
02/26/2022 – by Mod_GuideK0 
Only the user that generated a plan may apply it.
A. True
B. False
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Explanation:
The optional -out argument can be used to save the generated plan to a file for later execution with terraform apply, which can be useful when running Terraform in automation.
Reference: https://learn.hashicorp.com/tutorials/terraform/automate-terraform

298)	What is one disadvantage of using dynamic blocks in Terraform?
02/26/2022 – by Mod_GuideK0 
What is one disadvantage of using dynamic blocks in Terraform?
A. They cannot be used to loop through a list of values
B. Dynamic blocks can construct repeatable nested blocks
C. They make configuration harder to read and understand
D. Terraform will run more slowly
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Reference: https://github.com/hashicorp/terraform/issues/19291
299)	Which option can not be used to keep secrets out of Terraform configuration files?
02/26/2022 – by Mod_GuideK0 
Which option can not be used to keep secrets out of Terraform configuration files?
A. A Terraform provider
B. Environment variables
C. A -var flag
D. secure string
HIDE ANSWERS
Correct Answer: C
Explanation/Reference:
Reference: https://secrethub.io/blog/secret-management-for-terraform/


300)	Where does the Terraform local backend store its state?
02/26/2022 – by Mod_GuideK0 
Where does the Terraform local backend store its state?
A. In the /tmp directory
B. In the terraform.tfvars file
C. In the terraform.tfstate file
D. In the user’s .terraformrc file
HIDE ANSWERS
Correct Answer: C
Explanation/Reference:
Explanation:
The local backend stores state on the local filesystem, locks that state using system APIs, and performs operations locally.
Reference: https://www.terraform.io/docs/language/settings/backends/local.html


301-341
301)	What features does the hosted service Terraform Cloud provide?
 by Mod_0 
What features does the hosted service Terraform Cloud provide? (Choose two.)
A. Automated infrastructure deployment visualization
B. Automatic backups
C. Remote state storage
D. A web-based user interface (Ul)
HIDE ANSWERS
Correct Answer: BC
Explanation/Reference:
Reference:
https://www.terraform.io/docs/enterprise/admin/automated-recovery.html
https://www.terraform.io/docs/language/state/remote.html
302)	How do you specify version 1.0.0?
 by _1 
When using a ule block to reference a ule stored on the public Terraform ule Registry such as:
 
How do you specify version 1.0.0?
A. ules stored on the public Terraform ule Registry do not support versioning
B. Append ?ref=v 1.0.0 argument to the source path
C. Add version = “1.0.0” attribute to ule block
D. Nothing ules stored on the public Terraform Mocule Registry always default to version 1.0.0
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Reference: https://www.terraform.io/docs/language/ues/sources.html
303)	Which argument(s) is (are) required when declaring a Terraform variable?
 by _0 
Which argument(s) is (are) required when declaring a Terraform variable?
A. type
B. default
C. description
D. All of the above
E. None of the above
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Explanation:
The variable declaration can also include a default argument.
Reference: https://www.terraform.io/docs/language/values/variables.html

304)	Which options will produce a list of the IDs?
 by _0 
You have declared a variable called var.list which is a list of objects that all have an attribute id.
Which options will produce a list of the IDs? (Choose two.)
A. { for o in var.list : o => o.id }
B. var.list[*].id
C. [ var.list[*].id 1
D. [ for o in var.list: o.id ]
HIDE ANSWERS
Correct Answer: AB
Explanation/Reference:
305)	Which task does terraform init not perform?
 by _0 
Which task does terraform init not perform?
A. Sources all providers present in the configuration and ensures they are downloaded and available locally
B. Connects to the backend
C. Sources any ules and copies the configuration locally
D. Validates all required variables are present
HIDE ANSWERS
Correct Answer: D
Explanation/Reference:
Reference: https://www.terraform.io/docs/cli/commands/init.html

306)	What value does the Terraform Cloud/Tenaform Enterpnse private ule registry provide over the public Terraform ule Registry?
 by _0 
What value does the Terraform Cloud/Tenaform Enterpnse private ule registry provide over the public Terraform ule Registry?
A. The ability to share ules with public Terraform users and members of Terraform Enterprise Organizations
B. The ability to tag ules by version or release
C. The ability to restrict ules to members of Terraform Cloud or Enterprise organizations
D. The ability to share ules publicly with any user of Terraform
HIDE ANSWERS
Correct Answer: D
Explanation/Reference:
Explanation:
Terraform Registry is an index of ules shared publicly using this protocol. This public registry is the easiest way to get started with Terraform and find ules created by others in the community.
Reference: https://www.terraform.io/docs/language/ules/sources.html

307)	How can you format Terraform HCL (HashiCorp Configuration Language) code according to standard Terraform style convention?
 by _1 
You have multiple team members collaborating on infrastructure as code (IaC) using Terraform, and want to apply formatting standards for readability.
How can you format Terraform HCL (HashiCorp Configuration Language) code according to standard Terraform style convention?
A. Run the terraform fmt command during the code linting phase of your CI/CD process
B. Designate one person in each team to review and format everyone’s code
C. Manually apply two spaces indentation and align equal sign “=” characters in every Terraform file (*.tf)
D. Write a shell script to transform Terraform files using tools such as AWK Python, and sed
HIDE ANSWERS
Correct Answer: C
Explanation/Reference:
Explanation:
Indent two spaces for each nesting level.
When multiple arguments with single-line values appear on consecutive lines at the same nesting level, align their equals signs.
Reference: https://www.terraform.io/docs/language/syntax/style.html
308)	What does the default Tocal” Terraform backend store?
 by _0 
What does the default Tocal” Terraform backend store?
A. tfplan files
B. Terraform binary
C. Provider plugins
D. State file
HIDE ANSWERS
Correct Answer: D
Explanation/Reference:
Explanation:
The local backend stores state on the local filesystem, locks that state using system APIs, and performs operations locally.
Reference: https://www.terraform.io/docs/language/settings/backends/local.html

309)	Terraform can run on Windows or Linux, but it requires a Server version of the Windows operating system.
 by _1 
Terraform can run on Windows or Linux, but it requires a Server version of the Windows operating system.
A. True
B. False
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Reference: https://cloud.gooqle.com/kubernetes-enqine/docs/how-to/creatinq-a-cluster-windows
310)	A Terraform provisioner must be nested inside a resource configuration block.
 by _0 
A Terraform provisioner must be nested inside a resource configuration block.
A. True
B. False
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Most provisioners require access to the remote resource via SSH or WinRM, and expect a nested connection block with details about how to connect.
Reference: https://www.terraform.io/docs/language/resources/provisioners/connection.html


311)	Which of the following is the correct way to pass the value in the variable num_servers into a ule with the input servers?
 by _1 
Which of the following is the correct way to pass the value in the variable num_servers into a ule with the input servers?
A. servers num_servers
B. servers = variable.num_servers
C. servers var(num_servers)
D. servers = var.num_servers
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:

312)	Which command should you use to show all of the resources that will be deleted?
 by _0 
You have used Terraform to create an ephemeral development environment in the cloud and are now ready to destroy all the infrastructure described by your Terraform configuration. To be safe, you would like to first see all the infrastructure that will be deleted by Terraform.
Which command should you use to show all of the resources that will be deleted? (Choose two.)
A. Run terraform plan -destroy.
B. This is not possible. You can only show resources that will be created.
C. Run terraform state rm *.
D. Run terraform destroy and it will first output all the resources that will be deleted before prompting for approval.
HIDE ANSWERS
Correct Answer: CD
Explanation/Reference:
Reference: https://www.terraform.io/docs/cli/commands/state/rm.html


313)	Terraform validate validates the syntax of Terraform files.
 by _0 
terraform validate validates the syntax of Terraform files.
A. True
B. False
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
The terraform validate command validates the syntax and arguments of the Terraform configuration files.
Reference: https://www.terraform.io/docs/cIi/code/index.html

314)	Which of the following is available only in Terraform Enterprise or Cloud workspaces and not in Terraform CLI?
 by _0 
Which of the following is available only in Terraform Enterprise or Cloud workspaces and not in Terraform CLI?
A. Secure variable storage
B. Support for multiple cloud providers
C. Dry runs with terraform plan
D. Using the workspace as a data source
HIDE ANSWERS
Correct Answer: AB
Explanation/Reference:
Reference: https://www.terraform.io/docs/language/providers/confiquration.html

315)	Terraform can import ules from a number of sources which of the following is not a valid source?
 by _0 
Terraform can import ules from a number of sources which of the following is not a valid source?
A. FTP server
B. GitHub repository
C. Local path
D. Terraform ule Registry
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:

316)	When should you use the force-unlock command?
 by _0 
When should you use the force-unlock command?
A. You see a status message that you cannot acquire the lock
B. You have a high priority change
C. Automatic unlocking failed
D. Your apply failed due to a state lock
HIDE ANSWERS
Correct Answer: C
Explanation/Reference:
Manually unlock the state for the defined configuration.
Reference: https://wwwterraform.io/docs/cli/commands/force-unlock.html

317)	Terraform requires the Go runtime as a prerequisite for installation.
 by _0 
Terraform requires the Go runtime as a prerequisite for installation.
A. True
B. False
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Reference: https://www.terraform.io/docs/extend/guides/v1-upqrade-quide.html



318)	Why would you use the terraform taint command?
 by _0 
Why would you use the terraform taint command?
A. When you want to force Terraform to destroy a resource on the next apply
B. When you want to force Terraform to destroy and recreate a resource on the next apply
C. When you want Terraform to ignore a resource on the next apply
D. When you want Terraform to destroy all the infrastructure in your workspace
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
The terraform taint command manually marks a Terraform-managed resource as tainted, forcing it to be destroyed and recreated on the next apply.
Reference: https://www.terraform.io/docs/cli/commands/taint.html

319)	Which two steps are required to provision new infrastructure in the Terraform workflow?
 by _0 
Which two steps are required to provision new infrastructure in the Terraform workflow? (Choose two.)
A. Destroy
B. Apply
C. Import
D. Init
E. Validate
HIDE ANSWERS
Correct Answer: BD
Explanation/Reference:
Reference: https://www.terraform.io/guides/core-workflow.html


320)	Terraform init initializes a sample main.
 by _0 
terraform init initializes a sample main.tf file in the current directory.
A. Tiue
B. False
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Reference: https://www.terraform.io/docs/cli/commands/init.html

321)	How would you solve this using infrastructure as code?
 by _1 
You have recently started a new job at a retailer as an engineer. As part of this new role, you have been tasked with evaluating multiple outages that occurred during peak shopping time during the holiday season. Your investigation found that the team is manually deploying new compute instances and configuring each compute instance manually. This has led to inconsistent configuration between each compute instance.
How would you solve this using infrastructure as code?
A. Implement a ticketing workflow that makes engineers submit a ticket before manually provisioning and configuring a resource
B. Implement a checklist that engineers can follow when configuring compute instances
C. Replace the compute instance type with a larger version to reduce the number of required deployments
D. Implement a provisioning pipeline that deploys infrastructure configurations committed to your version control system following code reviews
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
322)	What are the two things you must do to achieve this?
 by _0 
You have provisioned some virtual machines (VMs) on Google Cloud Platform (GCP) using the gcloud command line tool. However, you are standardizing with Terraform and want to manage these VMs using Terraform instead.
What are the two things you must do to achieve this? (Choose two.)
A. Provision new VMs using Terraform with the same VM names
B. Use the terraform import command for the existing VMs
C. Write Terraform configuration for the existing VMs
D. Run the terraform import-gcp command
HIDE ANSWERS
Correct Answer: BC
Explanation/Reference:
The terraform import command is used to import existing infrastructure.
Import existing Google Cloud resources into Terraform with Terraformer.
Reference: https://www.terraform.io/docs/cli/import/usage.html
https://cloud.qooqle.com/docs/terraform

323)	Which of the following is not a valid string function in Terraform?
 by _0 
Which of the following is not a valid string function in Terraform?
A. split
B. join
C. slice
D. chomp
HIDE ANSWERS
Correct Answer: C
Explanation/Reference:
Reference: https://www.terraform.io/docs/language/functijns/chomp.html


324)	You should store secret data in the same version control repository as your Terraform configuration.
 by _0 
You should store secret data in the same version control repository as your Terraform configuration.
A. True
B. False
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Reference: https://bloq.qruntwork.io/a-comprehensive-quide-to-manaqinq-secrets-in-your-terraform-code-1d586955ace1


325)	If a ule uses a local variable, you can expose that value with a terraform output.
 by _0 
If a ule uses a local variable, you can expose that value with a terraform output.
A. True
B. False
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Output values are like function return values.
Reference: https://www.terraform.io/docs/language/values/locals.html
https://www.terraform.io/docs/language/values/outputs.html

326)	What information does the public Terraform ule Registry automatically expose about published ules?
 by _1 
What information does the public Terraform ule Registry automatically expose about published ules?
A. Required input variables
B. Optional inputs variables and default values
C. Outputs
D. All of the above
E. None of the above
HIDE ANSWERS
Correct Answer: E
Explanation/Reference:
Reference: https://www.terraform.io/docs/reqistry/ules/publish.html

327)	What is not processed when running a terraform refresh?
 by _0 
What is not processed when running a terraform refresh?
A. State file
B. Configuration file
C. Credentials
D. Cloud provider
HIDE ANSWERS
Correct Answer: CD
Explanation/Reference:
What Terraform is doing here is reconciling the resources tracked by the state file with the real world. It does this by querying your infrastructure providers to find out what’s actually running and the current configuration, and updating the state file with this new information. Terraform is designed to co-exist with other tools as well as manually provisioned resources and so it only refreshes resources under its management.
The output for a refresh is minimal. Terraform lists each resource it is refreshing along with its internal ID. Running refresh does not ify infrastructure, but does ify the state file. If the state has drifted from the last time Terraform ran, refresh allows that drift to be detected.
By default, a backup of your state file is written to terraform.tfstate.backup in case the state file is lost or corrupted to simplify recovery.

328)	What is the best practice reflecting this change in Terraform?
 by _1 
If you manually destroy infrastructure, what is the best practice reflecting this change in Terraform?
A. Run terraform refresh
B. It will happen automatically
C. Manually update the state fire
D. Run terraform import
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:

329)	What is the provider for this fictitious resource?
 by _0 
What is the provider for this fictitious resource?
 
A. vpc
B. main
C. aws
D. test
HIDE ANSWERS
Correct Answer: C
Explanation/Reference:
Reference: https://docsawsamazon.com/cloudformation-cli/latest/userquide/resource-typeshtml



330)	Terraform variables and outputs that set the “description” argument will store that description in the state file.
 by _0 
Terraform variables and outputs that set the “description” argument will store that description in the state file.
A. True
B. False
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Reference: https://www.terraform.io/docs/lanquaqe/values/outputs.html



331)	Which of the following is not a key principle of infrastructure as code?
 by _0 
Which of the following is not a key principle of infrastructure as code?
A. Versioned infrastructure
B. Golden images
C. Idempotence
D. Self-describing infrastructure
HIDE ANSWERS
Correct Answer: ABD
Explanation/Reference:
Reference: https://docs.microsoft.com/en-us/azure/devops/learn/what-is-infrastructure-as-code#:-:text=ldempotence%20is%20a%20principle%20otof%20the%20environment,s%20startinq%20state.

332)	What is the best method to quickly find the IP address of the resource you deployed?
 by _0 
You have deployed a new webapp with a public IP address on a clod provider. However, you did not create any outputs for your code.
What is the best method to quickly find the IP address of the resource you deployed?
A. Run terraform output ip_address to view the result
B. In a new folder, use the terraform_remote_state data source to load in the state file, then write an output for each resource that you find the state file
C. Run terraform state list to find the name of the resource, then terraform state show to find the attributes including public IP address
D. Run terraform destroy then terraform apply and look for the IP address in stdout
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Reference: https://www.terraform.io/docs/cli/commands/output.html

333)	What command does Terraform require the first time you run it within a configuration directory?
 by _0 
What command does Terraform require the first time you run it within a configuration directory?
A. terraform import
B. terraform in it
C. terraform plan
D. terraform workspace
HIDE ANSWERS
Correct Answer: B
Explanation/Reference: terraform init command is used to initialize a working directory containing Terraform configuration files.
Reference: https://www.terraform.io/docs/cli/commands/init.html

334)	Which of the following is not true of Terraform providers?
 by _0 
Which of the following is not true of Terraform providers?
A. Providers can be written by individuals
B. Providers can be maintained by a community of users
C. Some providers are maintained by HashiCorp
D. Major cloud vendors and non-cloud vendors can write, maintain, or collaborate on Terraform providers
E. None of the above
HIDE ANSWERS
Correct Answer: D
Explanation/Reference:
Reference: https://iayendrapatil.com/terraform-cheat-sheet/#Terraform Read and write configuration

335)	Which provisioner invokes a process on the resource created by Terraform?
 by _0 
Which provisioner invokes a process on the resource created by Terraform?
A. remote-exec
B. null-exec
C. local-exec
D. file
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
The remote-exec provisioner invokes a script on a remote resource after it is created.
Reference: https://www.terraform.io/docs/language/resources/provisioners/remote-exec.html

336)	Which of the following commands would you use first?
 by _0 
You run a local-exec provisioner in a null resource called null_resource.run_script and realize that you need to rerun the script. Which of the following commands would you use first?
A. terraform taint null_resource.run_script
B. terraform apply -target=null_resource.run_script
C. terraform validate null_resource.run_script
D. terraform plan -target=null_resource.run_script
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:


337)	A provider configuration block is required in every Terraform configuration.
 by _0 
A provider configuration block is required in every Terraform configuration.
Example:
 
A. True
B. False
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Reference: https://github.com/hashicorp/terraform/issues/17928

338)	What is the workflow for deploying new infrastructure with Terraform?
 by _0 
What is the workflow for deploying new infrastructure with Terraform?
A. terraform plan to import the current infrastructure to the state file, make code changes, and terraform apply to update the infrastructure.
B. Write a Terraform configuration, run terraform show to view proposed changes, and terraform apply to create new infrastructure.
C. terraform import to import the current infrastructure to the state file, make code changes, and terraform apply to update the infrastructure.
D. Write a Terraform configuration, run terraform init, run terraform plan to view planned infrastructure changes, and terraform apply to create new infrastructure.
HIDE ANSWERS
Correct Answer: C
Explanation/Reference: https://www.terraform.io/guides/core-workflow.html


339)	How is the Terraform remote backend different than other state backends such as S3, Consul, etc.?
 by _0 
How is the Terraform remote backend different than other state backends such as S3, Consul, etc.?
A. It can execute Terraform runs on dedicated infrastructure on premises or in Terraform Cloud
B. It doesn’t show the output of a terraform apply locally
C. It is only available to paying customers
D. All of the above
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
If you and your team are using Terraform to manage meaningful infrastructure, we recommend using the remote backend with Terraform Cloud or Terraform Enterprise.
Reference: https://www.terraform.io/docs/language/settings/backends/index.html

340)	One remote backend configuration always maps to a single remote workspace.
 by _0 
One remote backend configuration always maps to a single remote workspace.
A. True
B. False
HIDE ANSWERS
Correct Answer: A
Explanation/Reference:
Reference: https://www.terraform.io/docs/language/settings/backends/remote.html

341)	The terraform.
 by _0 
The terraform.tfstate file always matches your currently bjilt infrastructure.
A. True
B. False
HIDE ANSWERS
Correct Answer: B
Explanation/Reference:
Reference: https://www.terraform.io/docs/language/state/index.html


