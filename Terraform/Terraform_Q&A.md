# 🏗 Terraform Interview Questions & Answers (DevOps)

This section contains commonly asked **Terraform interview questions for DevOps Engineers (Fresher – 2+ Years Experience).**

---

# 1. What is Terraform?

Terraform is an **Infrastructure as Code (IaC) tool** developed by HashiCorp used to create, manage, and provision infrastructure using code.

It supports multiple cloud providers like:

- AWS
- Azure
- Google Cloud
- Kubernetes
- VMware

---

# 2. What is Infrastructure as Code (IaC)?

Infrastructure as Code means **managing infrastructure using configuration files instead of manual processes**.

Benefits:

- Automation
- Version control
- Consistency
- Faster deployments

---

# 3. What language does Terraform use?

Terraform uses **HCL (HashiCorp Configuration Language)**.

Example:

```
resource "aws_instance" "web" {
  ami           = "ami-123456"
  instance_type = "t2.micro"
}
```

---

# 4. What are Terraform providers?

Providers are **plugins that allow Terraform to interact with APIs of cloud platforms**.

Example providers:

- AWS
- Azure
- Google Cloud
- Kubernetes

Example:

```
provider "aws" {
  region = "ap-south-1"
}
```

---

# 5. What is a Terraform resource?

A resource is a **component of infrastructure** managed by Terraform.

Examples:

- EC2 instance
- VPC
- S3 bucket
- Security group

Example:

```
resource "aws_instance" "example" {
  ami           = "ami-0abcdef123456"
  instance_type = "t2.micro"
}
```

---

# 6. What are Terraform modules?

Modules are **reusable Terraform configurations** used to organize infrastructure code.

Example use cases:

- VPC module
- EC2 module
- Security group module

---

# 7. What is Terraform state?

Terraform state is a **file that stores information about the infrastructure Terraform manages**.

Default state file:

```
terraform.tfstate
```

State helps Terraform track changes and manage infrastructure.

---

# 8. What is remote state?

Remote state stores the Terraform state file in **remote storage instead of locally**.

Common remote backends:

- AWS S3
- Terraform Cloud
- Azure Storage

Example:

```
backend "s3" {
  bucket = "terraform-state"
  key    = "dev/terraform.tfstate"
  region = "ap-south-1"
}
```

---

# 9. Terraform Workflow

The basic Terraform workflow is:

```
terraform init
terraform plan
terraform apply
terraform destroy
```

Explanation:

terraform init  
Initializes the Terraform project.

terraform plan  
Shows what changes Terraform will make.

terraform apply  
Creates or updates infrastructure.

terraform destroy  
Deletes infrastructure.

---

# 10. What is `terraform init`?

`terraform init` initializes the working directory and downloads required provider plugins.

Example:

```
terraform init
```

---

# 11. What is `terraform plan`?

`terraform plan` shows **what changes Terraform will make before applying them**.

Example:

```
terraform plan
```

---

# 12. What is `terraform apply`?

`terraform apply` creates or updates infrastructure according to the Terraform configuration.

Example:

```
terraform apply
```

---

# 13. What is `terraform destroy`?

`terraform destroy` removes all resources created by Terraform.

Example:

```
terraform destroy
```

---

# 14. What are Terraform variables?

Variables allow **dynamic configuration of Terraform code**.

Example:

```
variable "instance_type" {
  default = "t2.micro"
}
```

Use variable:

```
instance_type = var.instance_type
```

---

# 15. What are Terraform outputs?

Outputs display useful information after infrastructure is created.

Example:

```
output "instance_ip" {
  value = aws_instance.web.public_ip
}
```

---

# 16. What is `terraform fmt`?

`terraform fmt` formats Terraform code according to standard style.

Example:

```
terraform fmt
```

---

# 17. What is `terraform validate`?

`terraform validate` checks whether Terraform configuration is syntactically correct.

Example:

```
terraform validate
```

---

# 18. What is a Terraform backend?

A backend defines **where Terraform stores its state file**.

Example backends:

- Local
- S3
- Terraform Cloud

---

# 19. What is Terraform workspace?

Workspaces allow you to **manage multiple environments using the same Terraform configuration**.

Example environments:

- dev
- staging
- production

Example:

```
terraform workspace new dev
```

---

# 20. Real DevOps Scenario

### Problem: Infrastructure created manually in AWS.

Solution:

Use Terraform to **automate infrastructure provisioning**.

Benefits:

- Consistent infrastructure
- Version-controlled code
- Faster deployments
- Easy rollback

---

# 🚀 Why Terraform is Important for DevOps

Terraform helps DevOps teams:

- Automate infrastructure provisioning
- Manage cloud infrastructure using code
- Maintain consistent environments
- Integrate with CI/CD pipelines

Terraform integrates with:

- AWS
- Kubernetes
- Docker
- Jenkins
- GitHub Actions
