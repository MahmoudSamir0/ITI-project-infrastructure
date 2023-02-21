# ITI-project-infrastructure
## Requirements

Before this module can be used on a project, you must ensure that the following pre-requisites are fulfilled:

1. Terraform and kubectl are [installed](#software-dependencies) on the machine where Terraform is executed.
2. The Compute Engine and Kubernetes Engine APIs are [active](#enable-apis) on the project you will launch the cluster in.

### Software Dependencies
#### Kubectl
- [kubectl](https://kubernetes.io/docs/tasks/tools)

#### Terraform and Plugins
- [Terraform](https://www.terraform.io/downloads.html) 0.13+
- [Terraform Provider for GCP][terraform-provider-google] v4.51
- 
#### gcloud
- assumes you already have gcloud installed in your $PATH.

### Enable APIs

- Compute Engine API - compute.googleapis.com
- Kubernetes Engine API - container.googleapis.com

[terraform-provider-google]: https://github.com/terraform-providers/terraform-provider-google
[12.3.0]: https://registry.terraform.io/modules/terraform-google-modules/kubernetes-engine/google/12.3.0
[terraform-0.13-upgrade]: https://www.terraform.io/upgrade-guides/0-13.html


## Before you do anything 

 run following commands in your local machine:
 
 **copy this command**
 
```shell script
sudo apt update
```

1. run following command  to login in your cli 
- login to your  account in (google cloud platform)

 **copy this command**

  ```shell script
  gcloud auth login
  ```

- clone this repo 
 (copy this command)

 ```shell script
git clone https://github.com/MahmoudSamir0/ITI-project-infrastructure.git
```
- enter the file of repo

 **copy this command**

```shell script
  cd ITI-project-infrastructure
```
## Build infrastructure

### Terraform

You can verify that terraform is  installed in your local ,machine
this by running `terraform version`.

 **copy this command**

```shell script
terraform version
```
  ### Initialize the directory

When you create a new configuration — or check out an existing configuration
from version control — you need to initialize the directory with `terraform
init`. This step downloads the providers defined in the configuration.

Initialize the directory.

 **copy this command**


```shell script
terraform init
```

Terraform returns output similar to the following.

```raw
Initializing modules...

Initializing the backend...

Initializing provider plugins...
- Reusing previous version of hashicorp/google from the dependency lock file
- Using previously-installed hashicorp/google v4.53.1

Terraform has been successfully initialized!

You may now begin working with Terraform. Try running "terraform plan" to see
any changes that are required for your infrastructure. All Terraform commands
should now work.

If you ever set or change modules or backend configuration for Terraform,
rerun this command to reinitialize your working directory. If you forget, other
commands will detect it and remind you to do so if necessary.
```

Terraform downloads the `google` provider and installs it in a hidden
subdirectory of your current working directory, named `.terraform`. The
`terraform init` command prints the provider version Terraform installed.
Terraform also creates a lock file named `.terraform.lock.hcl`, which specifies
the exact provider versions used to ensure that every Terraform run is
consistent. This also allows you to control when you want to upgrade the
providers used in your configuration

### Apply Configuration

 **copy this command**

```shell script
terraform apply 
```
answer `yes` to the confirmation prompt.

## now your infrastructure is ready 

