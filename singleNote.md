
# Understanding IaC - Spaced Repetition (Anki) Cards

What is Infrastructure as Code (IaC)? The practice of managing and provisioning infrastructure resources using code

What are the advantages of IaC patterns? 
{{c1::automation}} 
{{c2::consistency}}
{{c3::scalability}} 
{{c4::version control}}

What is the purpose of version control in IaC? It allows for tracking of infrastructure configurations over time

How does IaC improve collaboration among teams? Teams can work together by using a shared, version-controlled codebase for infrastructure management

How does IaC provide scalability? Through automating the provisioning and scaling of infrastructure resources 

How does IaC provide consistency? By using infrastructure configurations that are deployed in a repeatable way




# The Purpose of Terraform

## Reading

[What is Terraform?](https://developer.hashicorp.com/terraform/intro)  
[Use cases](https://developer.hashicorp.com/terraform/intro/v1.1.x/use-cases)  
[Purpose of Terraform State](https://developer.hashicorp.com/terraform/language/v1.1.x/state/purpose)

## Notes

### Cloud-agnostic

Terraform can provision infrastructure across many providers in one workflow. When provisioning resources across multiple cloud providers increase your tolerance as you protect yourself form provider specific outages. 

### Terraform State

The two requirements for Terraform to run are: the state and the configuration files. So, why is state good?

**Mapping to the Real World**

The state file is used as a database for resources you have provisioned in your providers. 

Be warned, when importing existing resources into your Terraform config, you need to make sure that you maintain only one reference to it in your configuration.

**Metadata**

Terraform needs to track metadata about the built resources as it needs to be able to calculate dependency trees so that it knows the sequencing of deletes. This is important when it comes to deleting resources across providers as well. 

**Performance**

When your state becomes rather large, you can use the state file as a cache so that you don't need to go out to your provider to check the status of all of the infrastructure when writing a plan. This is enabled with the `-refresh=false` flag.

**Syncing**

Remote state allows for people to collaborate on the same Terraform project. Terraform performs remote locking and will prevent users from running Terraform at the same time. Without state this wouldn't be possible.

## Exam Objectives / Testing

<details>
<summary>Explain multi-cloud and provider-agnostic benefits</summary>

- Increases reliability through distributing your infrastructure across multiple platforms
</details>

<details>
<summary>Explain the benefits of state</summary>
</details>
<details>
<summary>Performance</summary>

- You can cache the state of your infrastructure so that Terraform doesn't have to query the providers every run
</details>

<details>
<summary>Syncing</summary>

- State enables multiple people to be able to work on one Terraform project by using remote state and locking configuration changes to one person at a time
</details>

<details>
<summary>Metadata</summary>

- By using state, Terraform can track metadata needed to infer what order to delete resources in
</details>



# Terraform Basics

## Reading

[Get Get Started - AWS](https://developer.hashicorp.com/terraform/tutorials/aws-get-started)  
[Terraform Settings](https://developer.hashicorp.com/terraform/language/v1.1.x/settings)  
[Purpose of Terraform State](https://developer.hashicorp.com/terraform/language/v1.1.x/state/purpose)  
[Manage Terraform Versions](https://developer.hashicorp.com/terraform/tutorials/configuration-language/versions)  
[Providers](https://developer.hashicorp.com/terraform/language/v1.1.x/providers)  
[Provider Requirements](https://developer.hashicorp.com/terraform/language/v1.1.x/providers/requirements)  
[How Terraform Works With Plugins](https://developer.hashicorp.com/terraform/plugin/how-terraform-works)  
[Provider Configuration](https://developer.hashicorp.com/terraform/language/v1.1.x/providers/configuration)  
[Lock and Upgrade Provider Versions](https://developer.hashicorp.com/terraform/tutorials/configuration-language/provider-versioning)  
[Dependency Lock File](https://developer.hashicorp.com/terraform/language/v1.1.x/files/dependency-lock)

## Notes

### **Terraform providers**

Providers are plugins that allow Terraform to interact with cloud providers, SaaS providers, and other APIs. Providers supply the **resource types** and **data sources** that Terraform can manage. Without providers, Terraform cannot build any infrastructure. You can think of providers as downloading the API that Terraform then interacts with to manage infrastructure.

Providers come from the **Terraform Registry** for most large providers, but you can download them from other sources if your provider is in some niche.

Providers are defined as follows:

```terraform
provider "azurerm" {
  // mainly holds provider specific configuration
  features {}
  skip_provider_registration = true
}

```

Providers must be specified in the `required_providers` block within the `terraform` resource before they can be used. A `required_providers` block consists of a local name, a source location, and a version constraint:

```terraform
terraform {
  required_providers {
    azurerm = {
      source  = "hashicorp/azurerm"
      version = "=3.0.0"
    }
  }
}
```

You can use variables in provider configurations, but not outputs from resources.

There are also two "meta-arguments" that are defined by Terraform itself and available for all provider blocks:
  - `alias`, for using the same provider with different configurations for different resources
  - `version`, which Terraform **doesn't recommend** using (use provider requirements instead)


#### **Using Multiple Providers**

```terraform
# The default provider configuration; resources that begin with `aws_` will use
# it as the default, and it can be referenced as `aws`.
provider "aws" {
  region = "us-east-1"
}

# Additional provider configuration for west coast region; resources can
# reference this as `aws.west`.
provider "aws" {
  alias  = "west"
  region = "us-west-2"
}
```

To then use that alternate provider, you can select it as a reference:

```terraform
resource "aws_instance" "foo" {
  provider = aws.west

  # ...
}
```

#### **How Terraform Fetches Providers**

**Source Addresses** are used to uniquely identity providers. They are built in three parts: `[<HOSTNAME>/]<NAMESPACE>/<TYPE>`

- Hostname (optional): The hostname of the Terraform registry that distributes the provider
- Namespace: An organizational namespace within the specified registry
- Type: short name for the platform or system the provider manages

An example of a source address is `registry.terraform.io/hashicorp/http`.

Terraform will then download providers from this source address when `terraform init` is run. This will create a lock file to ensure that Terraform will use the same provider versions when re-running `terraform apply`.

### **Plugin-based architecture**

Plugins enable developers to extend Terraform by writing new plugins or compiling modified versions of existing plugins.

There are two parts to Terraform: **Terraform Core** and **Terraform Plugins**. **Terraform Core** provides the entry point to `terraform` and then it enables people to build upon it with plugins.

## Exam Objectives / Testing

<details>
<summary>Install and version Terraform providers</summary>

<details>
<summary>Installing providers</summary>

- To install a provider, you need both a `required_providers` block in the `terraform` resource, and a `provider` resource block detailing the configuration for that provider
- The `required_providers` block will need the **source address** of the provider
- You prepare the provider for being used by running `terraform init`
</details>

<details>
<summary>Versioning providers</summary>

- You can version your provider in the `required_providers` block in the `terraform resource`
- `terraform init` will create a versioning lock file when it's run
</details>

</details>

<details>
<summary>Write Terraform configuration using multiple providers</summary>

- You can define multiple providers and reference them using their `alias` field which is passed into the `provider` resource block
</details>

<details>
<summary>Describe how Terraform finds and fetches providers</summary>

- **Source Addresses** are used to uniquely identity providers. They are built in three parts: `[<HOSTNAME>/]<NAMESPACE>/<TYPE>`. Terraform will then download providers from this source address when `terraform init` is run. The `hostname` determines what **registry** terraform will look in for the provider. 

</details>

<details>
<summary>Describe plugin-based architecture</summary>

- Plugins enable Terraform's platform to be extended. There are two parts to Terraform: **Terraform Core** and **Terraform Plugins**. **Terraform Core** provides the entry point to `terraform` and then it enables people to build upon it with plugins.
</details>



# Terraform Outside of the Core Workflow

## Reading

[Command: state](https://developer.hashicorp.com/terraform/cli/v1.1.x/commands/state)  
[Manage Resources in Terraform State](https://developer.hashicorp.com/terraform/tutorials/state/state-cli)  
[Command: import](https://developer.hashicorp.com/terraform/cli/v1.1.x/commands/import)  
[Import Terraform Configuration](https://developer.hashicorp.com/terraform/tutorials/state/state-import)  
[Debugging Terraform](https://developer.hashicorp.com/terraform/internals/v1.1.x/debugging)  
[Troubleshoot Terraform](https://developer.hashicorp.com/terraform/tutorials/configuration-language/troubleshooting-workflow#enable-terraform-logging)  

## Notes

### **Terraform Import**

Terraform allows you to import existing infrastructure into Terraform management. This will bring the management of this resource under Terraform's control.

When importing, you must manually build a `resource` configuration block for the mapping of the resource.

Importing infrastructure involves five steps:

1) Identify the existing infrastructure you will import.
1) Import infrastructure into your Terraform state file.
1) Write Terraform configuration that matches that infrastructure.
1) Review the Terraform plan to ensure the configuration matches the expected state and infrastructure.
1) Apply the configuration to update your Terraform state.


#### **Commands**

`terraform import [options] <resource_id>` where the `resource_id` matches the existing resource in your provider

Example: `terraform import aws_instance.foo i-abcd1234` will import an AWS instance into the `aws_instance` resource named `foo`

#### **Usage Tips**

Make sure that each resource imported into Terraform is only reference once. Just like in programming, it's not good to have two references to one object as you may have unexpected behavior.

### **Terraform State Commands**

The `terraform state` command is used for advanced state management. 

When running `terraform state` commands that modify the state, Terraform will build a backup file, you can control where this outputs with the `-backup` arg.

#### **Tainting**

A resource can become tainted when an object is in an incomplete or a degraded state. In this case, running `terraform apply` will re-create the resource.

#### **Commands**

`terraform state list` will display the resources addresses for all resources in your state

`terraform state show <resource_address>` will show detailed information about one resource 

`terraform refresh` will update the state data to match the real-world condition of the managed resources

`terraform state mv` can be used to move resources from one state file to another, or to rename resources

`terraform state rm` will stop Terraform from managing a resource *without* deleting the real-world resource

`terraform state pull` will manually download and override your local copy of state from a remote state location

`terraform state push` will manually upload a local state file to a remote state (it shouldn't be used, let the normal workflow handle this)

`terraform apply -replace=<resource_address>` if you know that the state of a resource is corrupt and you want to replace that resource, you can force that with passing of the `-replace` arg to terraform

`terraform taint <resource_address>` to purposefully taint a resource so that it's replaced

`terraform untaint <resource_address>` when you know a resource is actually untainted and Terraform has marked it incorrectly

### **Logging**

To configure logging in Terraform you must manipulate environment variables. `TF_LOG` is used to change the detail of the logging you receive on stderr. 

You can set `TF_LOG` to one of the log levels `TRACE`, `DEBUG`, `INFO`, `WARN` or `ERROR` to change the verbosity of the logs.

To persist logs you can set the `TF_LOG_PATH`. 

## Exam Objectives / Testing

<details>
<summary>Describe when to use terraform import to import existing infrastructure into your Terraform state</summary>

- When you want an already existing resource in your infrastructure to be manged by Terraform
- This is good for gradually moving your infrastructure management over to Terraform
</details>

<details>
<summary>Use terraform state to view Terraform state</summary>

- `terraform state list` to view the resources addresses for all resources in your state
- `terraform state show <resource_address>` to view the detailed state for one resource
- `terraform show` can also be used to view state 
</details>

<details>
<summary>Describe when to enable verbose logging and what the outcome is</summary>

- You should enable logging when you want to debug an issue that you're having
- You can set the logging level using the environment variable `TF_LOG`
- The debugging logs are outputted to `stderr`
</details>




# Interact with Terraform Modules

## Reading

[Modules](https://developer.hashicorp.com/terraform/language/modules)  
[Finding and Using Modules](https://developer.hashicorp.com/terraform/registry/modules/use)  
[Input Variables](https://developer.hashicorp.com/terraform/language/values/variables)  
[Module Blocks](https://developer.hashicorp.com/terraform/language/v1.1.x/modules/syntax#accessing-module-output-values)  

## Notes

### **Modules**

*Modules* are containers for multiple resources that are used together. Modules are the main way to reuse resource configurations in Terraform.

There are *root modules* and *child modules*. Child modules are used within root modules.

#### **Calling a child module**

When calling a module, you must pass in values for its input variables. 

```terraform
module "servers" {
  source = "./app-cluster"

  servers = 5
}
```

All modules require a `source` argument, which is a pointer either to the local module, or to a remote module source that Terraform will then download to use.

You must run `terraform init` when adding, removing or modifying modules.

#### **Setting the module version**

When using public modules from a module registry, it's recommended to pass in a `version` argument into the `module` block. This is not required for local modules. 

To update modules, you can run the `terraform get` command.

#### **Accessing module output values**

The resources defined inside a module are encapsulated, so the calling module cannot access them directly, instead you use *output values* to selectively export values to then be used in the calling module.

To reference an output from a module block you can call it with `module.<name>.<output_value>`.

#### **Using input variables**

Each input variable accepted by a `module` must be declared within that `module` using a variable block:

You can force validation on a variable block by using the `validation` block.

```terraform
variable "image_id" {
  type        = string
  description = "The id of the machine image (AMI) to use for the server."

  validation {
    condition     = length(var.image_id) > 4 && substr(var.image_id, 0, 4) == "ami-"
    error_message = "The image_id value must be a valid AMI id, starting with \"ami-\"."
  }
}
```

Variables are then used by calling an object named `var`.

```terraform
resource "aws_instance" "example" {
  instance_type = "t2.micro"
  ami           = var.image_id
}
```

When defining variables within a `.tfvar` file, you do not need to build the `variable` block, you only need the variable name assignment:

```terraform
image_id = "ami-abc123"
availability_zone_names = [
  "us-east-1a",
  "us-west-1c",
]
```

#### **Module sources**

The `source` for a module tells Terraform where to find the source code for the module. 

The `source` argument can be treated as a URL, or in special cases you can prefix with actions such as `git::` or `s3::`. If your module is local, you can also pass in a path.

When using modules from the Terraform registry, you can reference the `registry source address` like you would with a provider. `<NAMESPACE>/<NAME>/<PROVIDER>`.

#### **Variable scope within modules/child modules**

The root module variables are set using the CLI, environment variables, variable files or in a Terraform Cloud workspace.

When passing variables into the child modules, the calling module passes the variables in using the `module` block.

The outputs defined by the child module will then be accessible in the calling module.

Terraform will automatically pick up files with the name `terraform.tfvars` or `terraform.tfvars.json`, or files ending in `.auto.tfvars` or `.auto.tfvars.json`

Variables defined within modules will not be accessible by their parent module.

## Exam Objectives / Testing

<details>
<summary>Contrast and use different module source options including the public Terraform Module Registry</summary>

- All `module` blocks require a source argument
- This source argument can be a local path, a URL or a special format for module providers like `git`, `s3` buckets and `svn`
- When using a module from the Terraform public registry, you use the format `<NAMESPACE>/<NAME>/<PROVIDER>`, which is very similar to a `source address` for a provider
</details>

<details>
<summary>Interact with module inputs and outputs</summary>

- When defining a `module` block, you need to pass in the `source` argument and the inputs required for that module
- The inputs for that module are decided by variables that are used within the `child module`, and are then defined when passed in as input by the calling module
- When `terraform apply` is run, the module will have output that it defines that can then be used by the calling module
</details>

<details>
<summary>Describe variable scope within modules/child modules</summary>

- The root module variables are set using the CLI, environment variables and variable files
- When passing variables into the child modules, the calling module passes the variables in using the `module` block, these variables are then used within the scope of the child module
</details>

<details>
<summary>Set module version</summary>

- When using remote modules, it's recommended that you set the version you're using by passing the `version` argument into the `module`
</details>


# Core Terraform Workflow

## Reading

[Navigate the core workflow](https://developer.hashicorp.com/terraform/tutorials/certification-003/associate-study-003)  
[Command: init](https://developer.hashicorp.com/terraform/cli/v1.1.x/commands/init)  
[Command: validate](https://developer.hashicorp.com/terraform/cli/v1.1.x/commands/validate)  
[Command: plan](https://developer.hashicorp.com/terraform/cli/v1.1.x/commands/plan)  
[Command: apply](https://developer.hashicorp.com/terraform/cli/v1.1.x/commands/apply)  
[Command: destroy](https://developer.hashicorp.com/terraform/cli/v1.1.x/commands/destroy)  
[Command: fmt](https://developer.hashicorp.com/terraform/cli/v1.1.x/commands/fmt)

## Notes

### **Workflow**

The core Terraform workflow has three steps:

1) **Write** - Author infrastructure as code
1) **Plan** - Preview changes before applying, `terraform plan`
1) **Apply** - Provision reproducible infrastructure, `terraform apply`

When working as a team, Terraform recommends using source control and branches. When running Terraform in a larger team, it's also recommended that you run the applying of your configuration in a [Continuous Integration environment](https://developer.hashicorp.com/terraform/tutorials/automation/automate-terraform?utm_source=WEBSITE&utm_medium=WEB_IO&utm_offer=ARTICLE_PAGE&utm_content=DOCS). When running the `terraform apply` within a CI environment, you will be able to review team member's plans using a pull request.

### **Initializing a working directory**

The `terraform init` command is used to initialize a working directory containing Terraform configuration files. This is the first command that should be run. This is safe to run multiple times.

`terraform init` will configure your backend state configurations if you have them, it will also handle the installation of your child modules and plugins/providers.

The running of `terraform init` will create a dependency version lock file for your plugins.

### **Validating a configuration**

The `terraform validate` command validates the configuration files in a directory, referring only to the configuration and not accessing any remote services such as remote state, provider APIs, etc.

This is good for validating that the configuration that you've written is syntactically valid and internally consistent, especially the linking of child modules which is prone to misconfiguration.

### **Reviewing an execution plan**

The `terraform plan` command creates an execution plan, which lets you preview the changes that Terraform plans to make to your infrastructure.

The steps of a plan are as follows:

1) Reads the current state of any already-existing remote objects to make sure that the Terraform state is up-to-date
2) Compares the current configuration to the prior state and noting any differences
3) Proposes a set of change actions that should, if applied, make the remote objects match the configuration

`terraform plan` will not modify any of your resources. It is also ran prior to applying changes when `terraform apply` is ran, so if your intention is to modify resources, just stick with `terraform apply`. 

A common way to use `terraform plan` is to produce a plan file, which can then be selectively executed by `terraform apply` using the `-out=` argument with `terraform apply`. To view the output from this plan in human-readable text when it is on disk you can use the `terraform show` command.

If there is a tilde (~) next to a resource when planning, this means that the resource will be updated in place.

### **Executing your configuration**

The `terraform apply` command executes the actions proposed in a Terraform plan. If run with no further arguments, it will build an execution plan before prompting you to continue with executing that plan. 

You can pass a saved plan to apply like this: `terraform apply [plan file]`.

### **Destroying resources**

The `terraform destroy` command is a convenient way to destroy all remote objects managed by a particular Terraform configuration. You don't want to run this in production!

### **Formatting and styling your configuration**

The `terraform fmt` command is used to rewrite Terraform configuration files to a canonical format and style. Very straightforward.

## Exam Objectives / Testing

<details>
<summary>Describe Terraform workflow</summary>

1) **Write** - Author infrastructure as code
2) **Plan** - Preview changes before applying, `terraform plan`
3) **Apply** - Provision reproducible infrastructure, `terraform apply`
</details>

<details>
<summary>Initialize a Terraform working directory</summary>

- `terraform init`
</details>

<details>
<summary>Validate a Terraform configuration</summary>

`terraform validate`
</details>

<details>
<summary>Generate and review an execution plan for Terraform</summary>

- Use `terraform plan` to view the plan
- If you want a plan on file you run `terraform plan -out=<plan_file>`
- If you want to read that plan run `terraform show <plan_file>`
</details>

<details>
<summary>Execute changes to infrastructure with Terraform</summary>

- `terraform apply`
- If you want to run a specific plan run `terraform apply <plan_file>`
</details>

<details>
<summary>Destroy Terraform managed infrastructure</summary>

- `terraform destroy`
</details>

<details>
<summary>Apply formatting and style adjustments to a configuration</summary>

- `terraform fmt`
</details>



# Implement and Maintain State

## Reading

[Backends](https://developer.hashicorp.com/terraform/language/v1.1.x/settings/backends)  
[State Locking](https://developer.hashicorp.com/terraform/language/v1.1.x/state/locking)  
[Command: login](https://developer.hashicorp.com/terraform/cli/commands/login)  
[Cloud configuration](https://developer.hashicorp.com/terraform/language/settings/terraform-cloud)  
[Manage Resource Drift](https://developer.hashicorp.com/terraform/tutorials/state/resource-drift#introduce-drift)  

## Notes

### **Backends**

Backends define where Terraform's state snapshots are stored. Terraform state is used to keep track of resources that terraform manages.

Terraform can store its state in a remote backend, integrate with Terraform Cloud, or do neither and default to storing state locally.

Backend configuration is done using a `backend` block. The backend block goes within the `terraform` configuration block. A backend block cannot refer to named values (like variables, locals or data sources).

```terraform
terraform {
  backend "remote" {
    organization = "example_corp"

    workspaces {
      name = "my-app-prod"
    }
  }
}
```

Whenever a configuration's backend changes, you must run `terraform init` again to validate and configure the backend before you can perform any plans, applies, or state operations.d.

If you change your configuration settings you will be prompted to `reinitialize`. 

#### **Default local backend**

By default, the state is stored locally. This is not optimal as 1) secrets are in plain text in state and 2) you cannot collaborate effectively when you have two copies of state running for one Terraform configuration.

#### **Backend and cloud integration authentication methods**

When using Terraform cloud, Terraform will manage your state file for you. If you have a `cloud` block, you cannot specify a `backend` block for this reason.

Because `backend` configurations often require secrets, and you cannot refer to named values, you can pass in credentials into your terraform command to fill in a *partial configuration*. A partial configuration is where you purposefully omit certain backend arguments that contain secret information.

You can pass in these missing arguments using a file, cli arguments, or interactively. 

Passing in using cli:
```bash
terraform init \
    -backend-config="address=demo.consul.io" \
    -backend-config="path=example_app/terraform_state" \
    -backend-config="scheme=https"
```

To pass in the arguments using a file, `terraform init -backend-config=PATH`. The file name should follow use the suffix `.tfbackend`

#### **Remote state back end options**

- There are cloud provider storage solutions like an AWS S3 bucket, or Azure Blob Storage
- There is also the option of Terraform cloud that provides a smoother integration experience and convenience

It is important to note if your remote state provider supports *state locking*, which will lock the state file when a `terraform apply` is being run. This keeps your state consistent and helps with collaboration.

To unlock the state manually, you must run the `terraform force-unlock <lock_id>` command.

#### **Backend block and cloud integration in configuration**

Example Azure configuration

```terraform
terraform {
  backend "azurerm" {
    resource_group_name  = "StorageAccount-ResourceGroup"
    storage_account_name = "abcd1234"
    container_name       = "tfstate"
    key                  = "prod.terraform.tfstate"
  }
}
```

### **State Locking**

As stated above, it is important to note if your remote state provider supports *state locking*, which will lock the state file when a `terraform apply` is being run. This keeps your state consistent and helps with collaboration.

You can `force-unlock` the state but this is not recommended.

### **Resource drift and Terraform state**

Resource drift is when your resources within your cloud provider have been modified through a method other than Terraform.

If you suspect that your infrastructure configuration changed outside of the Terraform workflow, you can use a `terraform plan -refresh-only` to inspect what the changes to your state file would be. This is safer than the refresh subcommand, which automatically overwrites your state file without displaying the updates.

If you opt yes to `refresh`ing your data, your state will have the current state of your resources, and your 
configuration will be out of date. You want to now either update your configuration, or run `terraform apply` to revert the manual changes made in the cloud. 

### **Secret management in state files**

When you run Terraform commands with a local state file, Terraform stores secrets in plain text, even if you have flagged them as sensitive. Terraform needs to store these values in your state so that it can tell if you have changed them since the last time you applied your configuration.

In order to secure these secrets, you need to store your `state` in a `backend` that has correct access controls. 

## Exam Objectives / Testing

<details>
<summary>Describe default local backend</summary>

- Default location of state in local
- Secrets are in plain text in state
- Limits collaboration as you shouldn't have two copies of state representing one Terraform configuration, which you will have if two people clone one Terraform repo with no remote backend
</details>

<details>
<summary>Describe state locking</summary>

- When modifying resources in the cloud, your state file is updated
- You don't want this file to be corrupted by two people editing it as the same time, hence locking
- In order to lock the state file, it needs to be in a remote state solution that supports *state locking*
</details>

<details>
<summary>Handle backend and cloud integration authentication methods</summary>

- When using a remote backend for your state, you will need to authenticate
- You can use a *partial configuration* by leaving sensitive arguments black in your `backend` block 
- You can then pass in the definition of these sensitive arguments using a file, cli arguments, or interactively
</details>

<details>
<summary>Differentiate remote state back end options</summary>

- There are cloud provider storage solutions like an AWS S3 bucket, or Azure Blob Storage
- There is also the option of Terraform cloud that provides a smoother integration experience and convenience
- It's pertinent that your `backend` provides state locking for collaboration
</details>

<details>
<summary>Manage resource drift and Terraform state</summary>

- Resource drift is when your resources within your cloud provider have been modified through a method other than Terraform
- You can use a `terraform plan -refresh-only` to inspect what the changes to your state file would be from this drift
- If you update your resources outside of the Terraform flow, you should run `terraform plan -refresh-only` and then ensure that you update your Terraform configuration to match what is in the cloud provider
</details>

<details>
<summary>Describe backend block and cloud integration in configuration</summary>

- The `backend` block is configured within the `terraform` block
```terraform
terraform {
  backend "azurerm" {
    resource_group_name  = "StorageAccount-ResourceGroup"
    storage_account_name = "abcd1234"
    container_name       = "tfstate"
    key                  = "prod.terraform.tfstate"
  }
}
```
</details>

<details>
<summary>Understand secret management in state files</summary>

- When you run Terraform commands with a local state file, Terraform stores secrets in plain text
- In order to secure these secrets, you need to store your `state` in a `backend`
</details>


# Read, Generate and Modify Configuration

## Reading

[Resources](https://developer.hashicorp.com/terraform/language/v1.1.x/resources)  
[Data Sources](https://developer.hashicorp.com/terraform/language/v1.1.x/data-sources)  
[Resource Graph](https://developer.hashicorp.com/terraform/internals/v1.1.x/graph)  
[Complex Types](https://developer.hashicorp.com/terraform/language/v1.1.x/expressions/type-constraints#complex-types)  
[Functions](https://developer.hashicorp.com/terraform/language/v1.1.x/functions)  

## Notes

### **Variables and outputs**

Variables are straightforward in Terraform if you have previous coding experience.

Please refer to [Objective 5 - Interact with Terraform Modules](../5-%20Interact%20with%20Terraform%20Modules/5-notes.md) for examples of defining and using variables and outputs, along with details about their scope.

What was missed in the above section was how to use a variable in a string, which can be done with the following: `"${var.name}-rest-of-string"`.

### **Resources**

A resource block is how we define infrastructure we want built in our environment. A resource block can range from something quite simple to something rather more complex.

```terraform
resource "aws_instance" "web" {
  ami           = "ami-a1b2c3d4"
  instance_type = "t2.micro"
}
```

The resource is given a *resource type* and a *name*. The name is used to later reference the resource within the module scope, and the resource type tells the provider what you want to build. The resource type and name together serve as an identifier for a given resource and so must be unique within a module. `<RESOURCE TYPE>.<NAME>.` You can use this access attributes of the built resource with `<RESOURCE TYPE>.<NAME>.<ATTRIBUTE>`.

An *implicit dependency* will be created when a resource references a named value from another resource. If you use the `[depends_on]` variable, you have created an *explicit dependency*. 

### **Data sources**

*Data sources* allow Terraform to use information defined outside of Terraform, defined by another separate Terraform configuration. Each provider may offer data sources alongside its set of resource types.

Data sources can be accessed using a `data` block:

```terraform
data "aws_ami" "example" {
  most_recent = true

  owners = ["self"]
  tags = {
    Name   = "app-server"
    Tested = "true"
  }
}
```

They are *read* objects and as such shouldn't be confused with `resource` blocks that *create, update, modify and read* the resources.

If the query constraint arguments for a data resource refer only to constant values or values that are already known, the data resource will be read and its state updated during Terraform's "refresh" phase, which runs prior to creating a plan. This ensures that the retrieved data is available for use during planning and so Terraform's plan will show the actual values obtained.

You can access data from a data block using `data.<TYPE>.<NAME>.<ATTRIBUTE>`.

### **Resource graph**

Terraform builds a dependency graph from the Terraform configurations, and walks this graph to generate plans, refresh state, and more.

A graph is built from these node types:

- **Resource Node** - Represents a single resource. If you have the count metaparameter set, then there will be one resource node for each count. The configuration, diff, state, etc. of the resource under change is attached to this node.

- **Provider Configuration Node** - Represents the time to fully configure a provider. This is when the provider configuration block is given to a provider, such as AWS security credentials.

- **Resource Meta-Node** - Represents a group of resources, but does not represent any action on its own. This is done for convenience on dependencies and making a prettier graph. This node is only present for resources that have a count parameter greater than 1.

To walk the graph, a standard depth-first traversal is done. Graph walking is done in parallel: a node is walked as soon as all of its dependencies are walked.

### **Types**

- `List`
  - Lists/tuples are represented by a pair of square brackets containing a comma-separated sequence of values, like `["a", 15, true]`

- `Map`
  - Maps/objects are represented by a pair of curly braces containing a series of <KEY> = <VALUE> pairs:
```terraform
{
  name = "John"
  age  = 52
}
```
  - Maps can be separated using a comma or a line break
  - The keys in a map must be strings; they can be left unquoted if they are a valid identifier, but must be quoted otherwise. You can use a non-literal string expression as a key by wrapping it in parentheses, like (var.business_unit_tag_name) = "SRE"
- `Set`
  - Used in much the same way that a `list` is

A *structural type* will allow *several distinct types* to be grouped together as a single value. Like the list `["a", 15, true]`, where as a *collection type* will only allow *one* type, such as `["a", "b", "c"]`. 


### **Functions**

The Terraform language includes a number of built-in functions that you can call from within expressions to transform and combine values. The general syntax for function calls is a function name followed by comma-separated arguments in parentheses `max(5,12,9)`.

To treat the value of a variable as sensitive, you need to surround the variable with a `sensitive()` function.

```terraform
locals {
  sensitive_content = sensitive(file("${path.module}/sensitive.txt"))
}
```

You can test functions using `terraform console`.

### **Secure secret injection**

For the following examples I will show how to populate this variable:
```terraform
variable "username" {
  description = "The username for the DB master user"
  type        = string
}
```

1) **Environment Variables**  
You can set the environment variable called `TF_VAR_username` to populate `var.username`
1) **Encrypted Files** (e.g., KMS, PGP, SOPS)  
Create a file containing `username: <username>` and then encrypt this file and include it into version control, you can then use a `data` block to read the file into Terraform, then load that into a `locals` variable block and then use it in your `resource` 
1) **Secret Stores** (e.g., Vault, AWS Secrets manager)  
This method is similar to storing the variable in a file, but instead you use a cloud provider vault, and then pull it into your configuration using a `data` block

## Exam Objectives / Testing

<details>
<summary>Demonstrate use of variables and outputs</summary>

Please refer to [Objective 5 - Interact with Terraform Modules](../5-%20Interact%20with%20Terraform%20Modules/5-notes.md) for examples of defining and using variables and outputs.
</details>

<details>
<summary>Describe secure secret injection best practice</summary>

- Leave the variable name undefined and use one of the following processes to populate it
- There's three ways to populate secret values
  - Environment variables
  - Encrypted files
  - Secret stores
</details>

<details>
<summary>Understand the use of collection and structural types</summary>

- A *structural type* will allow *several distinct types* to be grouped together as a single value. Like the list `["a", 15, true]`
- A *collection type* will only allow *one* type, such as `["a", "b", "c"]`

</details>

<details>
<summary>Create and differentiate resource and data configuration</summary>

- A `resource` is used to modify your infrastructure in your `provider`, whereas a `data` block is for read-only data
- Defining a `resource` block
```terraform
resource "aws_instance" "web" {
  ami           = "ami-a1b2c3d4"
  instance_type = "t2.micro"
}
```
- Defining a `data` block
```terraform
data "aws_ami" "example" {
  most_recent = true

  owners = ["self"]
  tags = {
    Name   = "app-server"
    Tested = "true"
  }
}
```
</details>

<details>
<summary>Use resource addressing and resource parameters to connect resources together</summary>

- The `resource` is given a *resource type* and a *name*
- The resource type and name together serve as an identifier for a given resource and so must be unique within a module
- You can use `<RESOURCE TYPE>.<NAME>.<ATTRIBUTE>` to access attributes from a resource, this can then be used to populate arguments in other resources
</details>

<details>
<summary>Use HCL and Terraform functions to write configuration</summary>

- Terraform includes a number of built-in functions
- The general syntax for function calls is function name followed by comma-separated arguments in parentheses `max(5,12,9)`
- You can test functions using `terraform console`
</details>

<details>
<summary>Describe built-in dependency management (order of execution based)</summary>

- Terraform builds a dependency graph from configuration and walks this graph to perform its functions
- The walking of the graph is done with depth-first traversal and is done in parallel
- The graph is built from these node types
  - Resource Node
  - Provider Configuration Node
  - Resource Meta-Node
</details>


# Terraform Cloud Capabilities

## Reading

[What is Terraform Cloud?](https://developer.hashicorp.com/terraform/cloud-docs)  
[Terraform Workflow](https://developer.hashicorp.com/terraform/cloud-docs/overview#terraform-workflow)
[Workspaces](https://developer.hashicorp.com/terraform/cloud-docs/workspaces)
[Private Registry](https://developer.hashicorp.com/terraform/cloud-docs/registry)
[Teams](https://developer.hashicorp.com/terraform/cloud-docs/users-teams-organizations/teams)
[Sentinel](https://developer.hashicorp.com/terraform/cloud-docs/policy-enforcement/sentinel)

## Notes

### **Terraform Cloud**

*Terraform Cloud* is an application that helps teams use Terraform together. It provides solutions for the pain points of using Terraform, such as remote state, resource drift, access control, secrets and more.

Terraform Cloud offers a generous free tier, including the use of workspaces.

#### **Workflow**

When more than one person is working on a Terraform project, you need at minimum to have a remote state solution, and ideally also a CI environment. Terraform Cloud can handle this for you. Terraform Cloud offers *Terraform Cloud Agents* that will run Terraform on your own isolated, private, or on-premises infrastructure, or they can provide cloud services for "remote operations".

#### **Workspaces**

When working in a corporate workplace, it's natural that you will have many collections of Terraform configurations for different environments. This is usually handled by having separate directories for each environment in your configuration.

Terraform Cloud manages infrastructure collections with *workspaces* instead of directories.

| Component               | Local Terraform                                               | Terraform Cloud                                                            |
| ----------------------- | ------------------------------------------------------------- | -------------------------------------------------------------------------- |
| Terraform configuration | On disk                                                       | In linked version control repository, or periodically uploaded via API/CLI |
| Variable values         | As `.tfvars` files, as CLI arguments, or in shell environment | In workspace                                                               |
| State                   | On disk or in remote backend                                  | In workspace                                                               |
| Credentials and secrets | In shell environment or entered at prompts                    | In workspace, stored as sensitive variables                                |

To switch workspaces in Terraform, you run the `terraform workspace select <workspace_name>` command. Terraform will not create a new workspace when this is run. To create a new workspace, you must run `terraform workspace new <workspace_name>`.

#### **Private Registry**

Terraform Cloud's *private registry* works similarly to the public Terraform Registry and helps you share Terraform providers and Terraform modules across your organization.Private providers and private modules are hosted on an organization's private registry and are only available to members of that organization.

#### **Teams**

*Teams* are groups of Terraform Cloud users within an organization. If a user belongs to at least one team in an organization, they are considered a member of that organization.

The organization can grant *workspace* permissions to teams that allow its members to start Terraform runs, create workspace variables, read and write state, etc

#### **Sentinel**

Policies are rules that Terraform Cloud enforces on runs. You use the *Sentinel* policy language to define Sentinel policies. After you define policies, you must add them to policy sets that Terraform Cloud can enforce on workspaces.

## Exam Objectives / Testing

<details>
<summary>Explain how Terraform Cloud helps to manage infrastructure</summary>

- Terraform cloud provides streamlined solutions for the pain points of setting up a Terraform platform in a corporate environment
- Remote state, secrets, a CI environment are all provided as a service to consume
</details>

<details>
<summary>Describe how Terraform Cloud enables collaboration and governance</summary>

- With *sentinel* and *teams*, you can govern who has access to run what, creating a more secure Terraform configuration
- Remote state, secrets, a CI environment are all provided as a service to consume, which are essential for collaboration
</details>

