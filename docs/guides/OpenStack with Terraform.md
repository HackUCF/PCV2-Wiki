# OpenStack Infrastructure Provisioning with Terraform

## 1. Introduction

This document provides a comprehensive guide for provisioning and managing OpenStack infrastructure using Terraform, an Infrastructure as Code (IaC) tool. It outlines the necessary steps for configuring Terraform, authenticating with OpenStack, and deploying virtual machine instances.

### 1.1 Purpose

This guide serves as a technical reference for the infrastructure team and club members seeking to automate OpenStack resource deployment using Terraform.

### 1.2 Scope

This document covers the following topics:

* Terraform fundamentals
* OpenStack application credential generation
* Terraform project setup and configuration
* Virtual machine instance deployment

## 2. Prerequisites

The following prerequisites must be met prior to proceeding with this guide:

* **OpenStack Cloud Access:** Valid credentials for an OpenStack environment are required.
* **Control Node:** A dedicated system (physical or virtual) with Terraform installed. It is recommended to deploy a virtual machine within the OpenStack environment for this purpose.
* **Terraform Installation:** Terraform CLI must be installed on the Control Node. Refer to the official [Terraform documentation](https://developer.hashicorp.com/terraform/tutorials/aws-get-started/install-cli) for installation instructions.

## 3. OpenStack Application Credentials

Application credentials are required for Terraform to authenticate with OpenStack.

### 3.1 Credential Generation

1.  **Access Horizon Dashboard:** Log in to the OpenStack Horizon web interface.
2.  **Navigate to Identity:** Proceed to "Identity" > "Application Credentials."
3.  **Create Credentials:** Initiate the credential creation process by clicking "Create Application Credential."
4.  **Configuration:**
    * Provide a descriptive name, optional description, and an expiration date.
    * Leave other fields at their default values.
5.  **Download `clouds.yaml`:** Download the generated `clouds.yaml` file, which contains the application credentials.

## 4. Terraform Project Setup

### 4.1 Project Directory

Create a dedicated directory for the Terraform project on the Control Node.

```bash
mkdir terraform_project && cd terraform_project
```
### 4.2 Configuration Files

Create the following Terraform configuration files: `main.tf` and `variables.tf`.
```bash
touch main.tf variables.tf
```
### 4.3 `clouds.yaml` Placement

Move the downloaded `clouds.yaml` file into the `terraform_project` directory.

## 5. Terraform Configuration

### 5.1 `variables.tf` Configuration

Define input variables in `variables.tf` to parameterize the infrastructure deployment. Note: replace "key_pair" with the name of your key pair in OpenStack.
```
variable "image_name" {
  default = "Ubuntu 24.04"
}

variable "flavor_name" {
  default = "m1.small"
}

variable "network_name" {
  default = "External Network"
}

variable "key_pair" {
  default = "Openstack-Personal"
}

variable "instance_count" {
  default = 3
}
```
### 5.2 `main.tf` Configuration

Define the OpenStack provider and virtual machine resources in `main.tf` and replace "Allow-ssh" with your SSH security group.
```
terraform {
  required_version = ">= 1.10.0"
  required_providers {
    openstack = {
      source  = "terraform-provider-openstack/openstack"
      version = "~> 1.53.0"
    }
  }
}

provider "openstack" {
  cloud = "openstack"
}

resource "openstack_compute_instance_v2" "ubuntu_servers" {
  count           = var.instance_count
  name            = "ubuntu-vm-${count.index + 1}"
  image_name      = var.image_name
  flavor_name     = var.flavor_name
  key_pair        = var.key_pair
  security_groups = ["Allow-ssh"]

  network {
    name = var.network_name
  }
}
```
## 6. Infrastructure Deployment

### 6.1 Terraform Initialization

Initialize the Terraform project to download provider plugins.
```bash
terraform init
```
### 6.2 Configuration Validation

Validate the Terraform configuration.
```bash
terraform validate
```
### 6.3 Execution Plan

Generate an execution plan to preview the changes.
```bash
terraform plan
```
### 6.4 Resource Application

Apply the Terraform configuration to deploy the virtual machine instances.
```bash
terraform apply
```
Confirm the deployment by typing `yes` when prompted.

### 6.5 Verification

Verify the deployment by confirming the creation of the virtual machine instances in the OpenStack Horizon dashboard.