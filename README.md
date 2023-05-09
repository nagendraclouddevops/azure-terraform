**Azure-Terraform**
### **1. what is terraform?** <br />
* Terraform is an open-source infrastructure as code (IaC) tool developed by HashiCorp. It allows developers and operations teams to define and manage infrastructure as code using a declarative language. With Terraform, you can define infrastructure resources such as servers, networks, storage, and other components required to run applications in the cloud or on-premises.

* Terraform works by defining infrastructure resources in a configuration file, which is then used to create, update, or delete the resources in a cloud provider or on-premises environment. It uses a state file to keep track of the current infrastructure state and changes made to it.

* Terraform supports a wide range of cloud providers such as Amazon Web Services (AWS), Microsoft Azure, Google Cloud Platform (GCP), and many others. It also supports multiple operating systems and can be used to manage infrastructure across different environments, from development to production.

* With Terraform, you can automate the deployment and management of infrastructure, making it faster and more efficient. It also allows you to version and audit infrastructure changes, and facilitates collaboration between developers and operations teams.

* Overall, Terraform is a powerful tool that helps organizations achieve greater agility and efficiency by automating infrastructure management and reducing manual errors.


###  **2.Why Terraform ?** <br />

Terraform is popular IaC (Infrastructure as a Code) tool. It is best in the market now.

* **Version Control:** <br />

    Since it is code, we can maintain in Git to version control. We can completely maintain the history of infra and collaboration is easy.

* **Consistent Infra:** <br />

    Often we face the problem of different configurations in different environments like DEV, QA, PROD, etc. Using terraform we can create similar infra in multiple environments with more reliability.

* **Automated Infra CRUD:** <br />

    Using terraform we can create entire infra in minutes reducing the human errors.
    Updating infra using terraform is also easy.
    Using Terraform we can delete infra.

* **Inventory Management:** <br />

    If we create infra manually it is very tough to maintain the inventory of resources in diff region. But by seeing terraform you can easily tell the resources you are using in different regions.

* **Cost Optimisation:** <br />

    When you need infra you can create in minutes. When you don't you can delete in minutes, so you can save the cost.

* **Automatic dependency management:** <br />

    terraform can understand the dependency of resources. It can tell us the dependency clearly.

* **Modular Infra:** <br />
    Code reuse. We can develop our own modules our use open source modules to reuse the infra code. instead of spending more time to create infra from the scratch we can reuse modules.




**TERRAFROM SETUP:**

        Below is the environment setup.

**Softwares Required:**

* VS Code
* Terraform: Download from here https://releases.hashicorp.com/terraform/1.4.6/terraform_1.4.6_windows_386.zip
* AWS CLI V2: https://releases.hashicorp.com/terraform/1.4.6/terraform_1.4.6_windows_386.zip
* AZURE CLI : https://releases.hashicorp.com/terraform/1.4.6/terraform_1.4.6_windows_386.zip



**For AWS Steps:**

* Create IAM administrator user. Copy the access key and secret key. Don't push to any GitHub or internet.
* Configure user in your laptop using
```
aws configure
```
* Add the terraform path to system variables.




**For Azure env setup**

* terraform file location paste in environment variables
* install az-cli and login to azure using az -login.






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