# Microsoft Entra Permissions Management  Deployment Guide

[What's Permissions Management? - Microsoft Entra | Microsoft Docs ](https://docs.microsoft.com/en-us/azure/active-directory/cloud-infrastructure-entitlement-management/overview)

## Introduction
###  Welcome to the Microsoft Entra Permissions Management trial playbook!

This playbook is a simple guide to help you make the most of your free 90-day trial which includes the Permissions Management Cloud Infrastructure Assessment to help you identify and remediate the most critical permission risks across your multi-cloud infrastructure. Using the suggested steps in this playbook from the Microsoft Identity team, you'll learn how Permissions Management can assist you to protect all your users and data. 


### What is Permissions Management? 
Microsoft Entra Permissions Management (MEPM) is a cloud infrastructure entitlement management (CIEM) solution that provides comprehensive visibility into permissions assigned to all identities including both workload and user identities, actions, and resources across multi-cloud infrastructures in *Microsoft Azure, Amazon Web Services (AWS), and Google Cloud Platform (GCP)*. Permissions Management detects, automatically right-sizes, and continuously monitors unused and excessive permissions.

Permissions Management helps your organization tackle cloud permissions by enabling the capabilities to continuously discover, remediate and monitor the activity of every unique user and workload identity operating in the cloud, alerting security and infrastructure teams to areas of unexpected or excessive risk. 
- Get granular cross-cloud visibility - Get a comprehensive view of every action performed by any identity on any resource.
- Enforce least privilege - Right-size permissions based on usage and activity and enforce permissions on-demand at cloud scale.
- Uncover permission risk - Assess permission risk by evaluating the gap between permissions granted and permissions used.
- Monitor and detect anomalies - Detect anomalous permission usage and generate detailed forensic reports.

![Microsoft Entra Permissions Management](/images/MEPM-key-cases.png)

### Deployment Approach 
Follow the 5 phases below to deploy Entra Permissions Management in your environment:

![Deployment Approach](/images/mepm-deployment-approach.png)

## Phase 1: Enable Microsoft Entra Permissions Management

The steps below are one time setup for the tenant and are to be completed before beginning to onboard cloud infrastructure enviroment

### Prerequisites
To enable Permissions Management in your organization:

- You must have an Azure AD tenant. If you don't already have one, [create a free account](https://azure.microsoft.com/free/).
- You must be eligible for or have an active assignment to the global administrator role as a user in that tenant.

### Personas, Activities and Permissions
![Microsoft Entra Permissions Management](media/personas-act-permiss.png)

### Tools
In order to streamline the enablement of MEPM, the following tools should be available to complete the enablement steps
Ensure you have access to tools used during the enablement and cloud configuration steps, using Any Of:
  - [MS Graph Explorer (Recommended)](https://docs.microsoft.com/en-us/graph/graph-explorer/graph-explorer-overview)
  - [Local session with Azure CLI, Microsoft Graph Powershell SDK module](https://docs.microsoft.com/en-us/powershell/microsoftgraph/overview?view=graph-powershell-1.0)
  - [Cloud Session using Azure Cloud Shell](https://docs.microsoft.com/en-us/azure/cloud-shell/overview)

### Actions to take:
1. In your browser:
    1. Go to [Entra services](https://entra.microsoft.com) and use your credentials to sign in to [Azure Active Directory](https://ms.portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/Overview).
    1. If you aren't already authenticated, sign in as a global administrator user.
    1. If needed, activate the global administrator role in your Azure AD tenant.
    1. In the Azure AD portal, select **Permissions Management**, and then select the link to purchase a license or begin a trial.

>[!OPTIONAL]
> Delegate MEPM console admin access for users – Organizations may choose to delegate permissions to other users in their environment to continue the next phases after the enablement steps are complete. 

- [Group-based permission settings:](https://docs.microsoft.com/en-us/azure/active-directory/cloud-infrastructure-entitlement-management/how-to-create-group-based-permissions) Identify and grant access to users with the correct account scope and permissions. In addition to being admins, users can have the following granular permissions:
  - **Viewers:** View only access to scoped cloud accounts 
  - **Controller:** Modify the CIEM properties
  - **Approvers:** Able to approve permission requests
  - **Requestors:** Request for permissions in cloud accounts
