# Terraform Learning

## Course

[Learn Terraform](https://www.linkedin.com/learning/learning-terraform-2/welcome?u=2138932)

## Learning Notes

### What is Terraform

[Terraform](https://github.com/hashicorp/terraform) is a CLI tool for IaC

### Setup

<details>
  <summary>Details</summary>
  
  1. Download and install from https://www.terraform.io/
  2. Setup system PATH
  3. Create AWS profile and setup locally
  4. Setup provider "aws" in first_code.tf
</details>

### Terraform Commands

<details>
  <summary>terraform init</summary>
  
  1. After init, a ".terraform" folder will be created in current path
  2. During init, Terraform searches the configuration for both direct and indirect references to providers and attempts
   to load the required plugins.
</details>

<details>
  <summary>terraform apply</summary>
  
  1. An execution plan will be generated for review.
  2. Reply 'yes' to execute the plan
  3. Execution sample: "Apply complete! Resources: 1 added, 0 changed, 0 destroyed."
</details>

<details>
  <summary>terraform plan</summary>
  
  1. Check infrastructure state, compare, show results and resource actions if needed
  2. With -destroy option, it will list down what will be destroyed
  3. With -out option, the plan result will be stored in a binary file afterward,
  e.g. terraform -destroy -out=result.plan
</details>

<details>
  <summary>terraform show</summary>
  
  - terraform show result.plan - display plan content 
  - terraform show - display all states
  - terraform show -json - display all states info in json format
</details>

<details>
  <summary>terraform state</summary>
  
  1. for local storage (in-memory), it's a local terraform.tfstate file (in json format)
  2. remote storage - for team work and version control maybe
  
  - terraform state list - list all terraform resources
  - terraform state show RESOURCE_NAME - show one resource state
</details>

<details>
  <summary>terraform graph</summary>
  
  1. generate a visual representation in DOT format which can be used by GraphViz to generate charts.
  2. copy paste output into an online editor to check chart, e.g. [GraphvizOnline](https://dreampuf.github.io/GraphvizOnline)
</details>