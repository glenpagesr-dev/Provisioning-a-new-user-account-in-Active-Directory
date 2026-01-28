<h1> Watch me build the Lab here

 https://www.loom.com/share/5b8db4e5b6f341aabb33eeab9261b53f
# Active Directory User Provisioning Lab
A hands-on lab demonstrating the setup and configuration of a Virtual Machine for Active Directory on AWS

## Overview

This lab demonstrates the process of provisioning a new user account in **Active Directory Domain Services (AD DS)** using industry-standard practices. The objective is to simulate a real-world Help Desk / Junior Systems Administrator onboarding task while following security, documentation, and RBAC principles.

---

## Objectives

* Create a new user account in Active Directory
* Configure core user attributes
* Assign security group memberships
* Validate account functionality
* Document the provisioning process

---

## Environment

* Windows Server (Domain Controller)
* Active Directory Users and Computers (ADUC)
* Domain-joined workstation

---

## Prerequisites

* Domain Admin or delegated account creation permissions
* Approved access request (simulated)
* User details (name, department, role, manager)

---

## Step-by-Step Procedure

### 1. Open Active Directory Users and Computers
![image alt](https://github.com/glenpagesr-dev/Active-Directory-User-Provisioning-Lab/blob/3bd6ec2d2ade4157f34eb06f8970ac2ab309318a/user%20and%20computer.png)
* Log into a domain-joined system.
* Launch **Active Directory Users and Computers** (`dsa.msc`).

---

### 2. Create the User Account
![image alt](https://github.com/glenpagesr-dev/Active-Directory-User-Provisioning-Lab/blob/d4ebb43038a1f6cfdd23d1da8c9070d96c3061d9/create%20user.png)
* Right-click the OU → **New → User**
* Enter the following:

  * First Name
  * Last Name
  * User Principal Name (UPN)
  * sAMAccountName

---

### 3. Populate User Attributes
![image alt](https://github.com/glenpagesr-dev/Active-Directory-User-Provisioning-Lab/blob/f13e540e41c0644c1be12e044d071ce7ccd5b21f/user%20attributes.png)

* Open User Properties and configure:

* Job Title

* Department

* Company

* Manager

* Office Location

* Proper attributes support RBAC, directory services, and reporting.

### 4. Assign Security Group Memberships

* Add the user to required groups:

  * Departmental security groups
  * Application access groups
  * File share / printer groups
* Follow **least privilege** principles.

---

### 5. Configure Initial Password Settings
![image alt](https://github.com/glenpagesr-dev/Active-Directory-User-Provisioning-Lab/blob/1eee61db2aa9e9c56c686d891ec08f1eae43273d/configure%20password.png)


* Assign a temporary password that meets domain policy.
* Select:

  * ✔ User must change password at next logon
  * (Optional) Account disabled if start date is future

---

### 6. Enable the Account
![image alt](https://github.com/glenpagesr-dev/Active-Directory-User-Provisioning-Lab/blob/95dc448c8c47da63325cc8638571b1f52ac38df8/enable%20account.png)


* Ensure the account is enabled if onboarding is complete.
* Confirm account status in ADUC.

---

### 7. Validate Account Provisioning
![image alt](https://github.com/glenpagesr-dev/Active-Directory-User-Provisioning-Lab/blob/ffcd8f529a40e8ed0e52aeafa96b953bbf8e9ce9/Validate.png)


* Verify:

  * Successful login
  * Correct group memberships
  * GPOs are applied
  * Access to assigned resources

---

### 8. Documentation

* Update the ticket or lab notes with:

  * Username / UPN
  * Groups assigned
  * Password reset requirement
  * Completion confirmation

---

## Results

* User account successfully provisioned
* Access aligned with role-based requirements
* Account validated and documented

---

## Key Takeaways

* Accurate OU placement ensures proper policy enforcement
* Group-based access simplifies management
* Documentation is critical for audit and compliance

---

## Skills Demonstrated

* Active Directory user management
* RBAC implementation
* Identity and access management fundamentals
* Enterprise documentation practices

---

## Next Steps

* Automate user provisioning with PowerShell
* Integrate with Azure AD / Entra ID
* Implement MFA and lifecycle management
