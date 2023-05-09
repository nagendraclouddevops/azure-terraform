### Basics





**Terraform Commands**

* First command is to initialize the terraform, at this stage terraform downloads the provider into .terraform folder.

***terraform init*** command is used to initialize a Terraform working directory. When you run terraform init, Terraform will perform the following tasks:

* Download providers: If your Terraform configuration file references any cloud providers, terraform init will download and install the appropriate provider plugins. These plugins are used to interact with the cloud provider's APIs and perform resource management tasks.

* Initialize backend: terraform init initializes the backend configuration, which is used to store and manage the state of the infrastructure resources. The backend can be local, remote, or encrypted storage.

* Install modules: If your Terraform configuration file references any external modules, terraform init will download and install them in the .terraform/modules directory.

* Create a lock file: terraform init creates a lock file named terraform.lock.hcl that lists the exact version of each provider and module required by the configuration file. This helps ensure that the same version of the provider and modules are used when running terraform apply or terraform plan to avoid any version conflicts.

```
terraform init
```

* Next we need to run plan command, at this stage terraform compares the infra between declared and existing. This is only plan terraform will not create

```
terraform plan
```

* Next we need to apply the infra, at this stage terraform create the infra with approval.

```
terraform apply
```

* Providers are the plugins that Terraform uses to manage those resources. Every supported service or infrastructure platform has a provider that defines which resources are available and performs API calls to manage those resources.
