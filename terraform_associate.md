# Bullet Notes: HashiCorp Certified Terraform Associate
> If you are in a Multi-Cloud or Hybrid-Cloud arena, then Terraform is a must to learn and its certification is good to have. I have been working with Terraform for quite some time now and preparing for its certification too.
> I took some bullet notes, a way of revising things just minutes before taking the exam and also documenting my preparation. Please use the notes as such, just as an add-on to your larger exam preparation.
> The notes are from HashiCorp’s Exam Review and Study Material here. This is also structured in similar fashion.

# 1. Understand Infrastructure as Code (IaC) concepts

## why IaC?

- a)  Human readable and easy to use
- b)  Cloud Environment are API driven
- c)  Higher elasticity of today’s infrastructure
- d)  Version control
- e)  Transparency in documentation
- f)  Re-usability & Automation

# 2. Understand Terraform’s purpose (vs other IaC)

## Benefits such as
i) Platform Agnostic
ii) State Management
iii) Operator Confidence with workflow

## Terraform State:
- a. Mapping to the real world
- b. Metadata or Resource dependencies
- c. Ordering of resource types
- d. Pointer to provider configuration
- e. Resource attribute cache for performance
- f. Syncing: Remote state for multi-teams

## Workflows:
- i) Scope - What resources
- ii) Author - Create configuration file
- iii) Initialize - terraform init. Download correct provider plug-ins
- iv) Plan & Apply - terraform plan to verify creation, terraform apply to create real resources

# 3. Understand Terraform Basics

## Provider : 
> Configures the name provider. Providers are installed only in the current working directory. Other working directory can have other providers.

- alias: Multiple configurations of the same provider can be made, like multiple regions of AWS. The additional has to be tagged as 'alias'
- 3rd Party Providers are to be manually placed in plugins directory (.terraform.d/plugins)
- provider plugin cache: As provider plugins are directory specific, same plugins might get downloaded in multiple working directories. To avoid this, plugin cache can be configured to avoid duplicate copies. The unused plugins are to be manually removed from cache over a period of time

## Resource : Defines the infrastructure

- terraform show To inspect the terraform state. It is determined from the file terraform.tfstate
- terraform state For advanced state management such as terraform state list
- While modifying the terraform file and re-applying, a `-/+` denotes that the resource will be deleted and re-created rather than modifying the existing
- `~` denotes that some attributes can be updated in-place
- Implicit Dependency: When a resource attribute is defined with reference to an attribute defined earlier, Terraform understand the dependency and orders the creation accordingly.
- Explicit Dependency: When Terraform has no details of how to order few resources, it can be defined Explicitly using `*depends on`*

### Provisioners: Lets to upload files, run scripts or trigger other tools inside a resource

- Local exec : Executes a command locally
- Remote exec : Invokes a remote script or a tool. But this needs the “connection” block to be defined. Uses SSH or WINRM
- If provisioner fails, Terraform will not destroy the resource but it will taint it as provision failed. During the next deploy, it will destroy the tainted resource and re-created
- One can also manually taint it using terraform taint resource.id
- Destroy provisioners: Provisioners that are needed to be run during destroy activity
- null_resource : Provisioners without a resource
- self block to refer to the parent resource of the provisioner
- Multiple provisioners are executed in the order they're defined in the configuration file.
- on_failure : Can be used to define Terraform on what to be done when provisioner fails
- Variables: Create a separate file with all variables in it.

## Assigning Variables via

* Command-line using `-var` flag
* terraform.tfvars or *.auto.tfvars : Terraform automatically loads variables from these exact file names. If file names are different then they are to be mentioned using var-file
* Secretes can be stored separately in a file as secret.tfvars and called using -var-file during execution
* Multiple -var-file flags can be used during plan or apply
* Variables can also be given in UI console
- Default variables will take into effect if none of the methods were used to define a variable
Variable Data Types
List, use [] to explicitly declare or {} to implicitly declare

Maps - It is a key/value data-structure

### Output Variables

Export value of a variable by defining a *Output variable*
Output is displayed automatically after apply. But to show output after apply-time, terraform output <outputvariable> can be used
### Remote State Storage

For team collaboration, the state file is stored in remote backend and has features such as lock in. This enables multiple people to provision the infrastructure.
### Terraform Cloud: 
Easy to version, audit & collaborate the IaC

* Removes access credentials off from user machines
* To apply remote backend in Terraform Cloud, add the backend configuration in the Terraform Cloud organization → Create Token in TC → Apply the token → Run terraform init

# 4. Use the Terraform CLI (outside of core workflow)

* terraform fmt Updates configuration in the current directory for consistency. Format consistency
* terraform taint To manually taint a resource so that it is re-created during next apply
* terraform import Imports resources to Terraform. Needs Resource Address & ID
* terraform console Interactive console for evaluating expressions

- Workspaces

* Initial there is only one workspace called "default" and its associated persistent back-end
* Default workspace can never be deleted
* Multiple Workspace, allowing multiple sates with a configuration
* terraform workspace new and terraform workspace select
* To create a parallel, distinct copy of a set of infrastructure in order to test a set of changes, similar to Git branch and merging with master
* Terraform stores the workspace states in a directory called terraform.tfstate.d

- State Command

* terraform state Advanced state management
* terraform state subcommands that modify the state write backup files
* terraform show : Inspect the current state
* terraform state list aws_instance.bar : List State resources
* terraform state mv : Move resources in state or to a different state file
* terraform state pull : Manually download and output the state
* terraform state push : Manually upload a state
* terraform state rm : Remove items from the Terraform state
* terraform state show : Show the attributes of a single resource

- Debugging Terraform

Detailed log can be enabled by setting up values for the environment variable TF_LOG

Values are TRACE, DEBUG, INFO, WARN or ERROR. TRACE being default and most verbose

# 5. Interact with Terraform modules

Modules Can:

- Organize Configuration by keeping related parts together
- Encapsulate configuration can prevent unintended consequences
- Re-use configuration to save time and error free
- Provide consistency and ensure best practice

Modules can either be used from another local directory or remote registry

Example of Module from Terraform Registry:
```
module “vpc” {
source = “terraform-aws-modules/vpc/aws”
version = “2.21.0”

name = var.vpc_name
cidr = var.vpc_cidr

azs = var.vpc_azs
private_subnets = var.vpc_private_subnets
public_subnets = var.vpc_public_subnets

enable_nat_gateway = var.vpc_enable_nat_gateway

tags = var.vpc_tags
}
```
- To create a local module, create a sub-directory within the root module(directory) with the name of the module. Start creating with main.tf, variable.tf & output.tf
- To use configuration files for different purposes, Different Directory or Workspace approach can be taken.
* Different Directory: If there are larger differences
* Workspaces : If there are minimal differences but 2 different state file.
# 6. Navigate Terraform workflow

terraform init To initialize the terraform in the working directory and load the plugins, providers.

- Copy of Source Module
- Back-end Initialization
- Child Module Initialization
- Plugin Installation
* terraform validate Check and report errors within modules, attribute names and value types. Validates the configuration files in a directory, referring only to the configuration and not accessing any remote services. Whether a configuration is syntactically valid,

* terraform plan To plan the infrastructure execution. Terraform performs a refresh, unless explicitly disabled, and then determines what actions are necessary to achieve the desired state.

Resource Targeting: Optional and used to focus Terraform on a specific resource.

* terraform apply: Apply changes required to attain the desired state
* terraform destroy: Terminates resources mentioned in the configuration file

The behavior of any terraform destroy command can be previewed at any time with an equivalent terraform plan -destroy command

# 7. Implement and Maintain state

State Locking:

- For supported backends, Terraform locks the state during write operations and prevent corruption
- Types of Backend: Enhanced (Local & Remote), Standard (azurerm,s3, etc)
- force-unlock: Manually unlock the state

The state file consists of sensitive data such as credentials, resource ID etc. The local state file stores them in plain JSON format. Remote state file encrypts it at rest (depending on the backend).
```
terraform {
backend “remote” {
hostname = “app.terraform.io”
organization = “company”

workspaces {
name = “my-app-prod”
}
}
```
OR
```
terraform {
backend “azurerm” {
resource_group_name = “StorageAccount-ResourceGroup”
storage_account_name = “abcd1234”
container_name = “tfstate”
key = “prod.terraform.tfstate”
}
}
```
terraform refresh : reconciles the state Terraform knows by comparing with real infrastructure. To detect any drifts and update state file.

# 8. Read, generate, and modify configuration

## Resources: Describes one or more infrastructure objects

- On most cases there are no resource dependencies and TF can create resources in parallel
- Other times, it reads the resource block to create implicit dependencies
- We can also explicitly maintain the dependency using `depends_on`
## Data Sources: Data to be fetched or computed for use elsewhere in configuration

- Unique to a resource and provider
- Arguments within the DS block are query constraints
- For constant values, Data resource updates the state during TF “refresh” 1stage
- For dynamic value, reading of values is done after “apply” phase and other dependent resources results are kept in pending
## Resource Addressing:

[module path][resource spec]

- If module path is omitted, it refers to the root module
- Resource spec: *resource_type.resource_name[resource index]*
## Complex Types
- Collection Type: Similar types like list, map, set
- Structural Type: Values of different types, object & tuple
## Built-in functions: TF has set of defined functions that can be used. No user defined functions. Eg: max, min, lower, upper

## Dynamic Block: Dynamically constructs repeatable nested blocks within resource, data, provider, provisioner etc

Vault Provider for Terraform

# 9. Understand Terraform Cloud and Enterprise capabilities

Workspace, Version Control, Shared State, Private Module Registry, Access Control & Sentinel Policies, Command Line Integration

## Terraform Cloud: Collaborate with teams.

* Free Plans include most services with 5 active users. Sentinel belongs to paid.
* Billing is organization based
* Has 3 models : Free, Team, Team & Governance
## Terraform Enterprise: For Large Enterprises, self hosted distribution of Terraform Cloud

- i) Terraform state can be migrated to Terraform cloud by updating the backend
- ii) Terraform Cloud organizes infrastructure as Workspaces. CLI does in directories
- iii) For each workspace, TF Cloud stores State Versions & Run History

## Worspaces & Modules:

* Workspaces are more of organizing the code, in-terms of various infrastructure resources, variable files, state file & permissions
* Modules, are for standardizing the code across org. Re-usable code.
* Module Registry — For Hashicorp certified & comunity developed modules
## Policy As Code: Sentinel

* Compliance Policies
* Security Policies
* Operational Policies