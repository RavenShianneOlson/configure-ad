<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Microsoft Remote Desktop for Mac
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

## High-Level Deployment and Configuration Steps

1. **Azure Resource Setup:**
   - Create a resource group in the Azure portal.
   - Provision Azure Virtual Machines running Windows Server within the resource group.
   - Ensure the VMs are connected to the same virtual network for seamless communication.

2. **Active Directory Domain Services Configuration:**
   - Install and configure Active Directory Domain Services (AD DS) on one of the Azure VMs.
   - Promote the VM to a domain controller using the AD DS Configuration Wizard.
   - Configure DNS settings on the domain controller to ensure proper domain resolution.

3. **Active Directory Replication and Redundancy:**
   - Optionally, configure additional domain controllers on other Azure VMs for redundancy and fault tolerance.
   - Enable Active Directory replication between domain controllers to synchronize changes and ensure data consistency.

4. **Integration with On-premises Resources:**
   - Establish a site-to-site VPN connection between your on-premises network and Azure Virtual Network for seamless integration.
   - Update DNS settings on your on-premises resources to point to the Azure Virtual Machines acting as domain controllers.


# Friendly Tutorial: Implementing On-premises Active Directory within Azure Virtual Machines

Welcome to our friendly tutorial on implementing On-premises Active Directory within Azure Virtual Machines! In this guide, we'll walk you through the process step by step, ensuring a smooth setup of your Active Directory environment in the Azure cloud.

## Why Use On-premises Active Directory in Azure?

Bringing your Active Directory infrastructure to Azure Virtual Machines offers numerous benefits, including centralized user management, seamless integration with Azure services, and improved scalability and flexibility.

## Prerequisites

Before we begin, here's what you'll need:

- An active Azure subscription
- Basic understanding of Azure Virtual Machines and Active Directory concepts

## Step 1: Setting Up Azure Resources

Let's kick things off by setting up the necessary Azure resources:

1. **Create a Resource Group:**
   - Sign in to the Azure portal (portal.azure.com).
   - Navigate to "Resource groups" and create a new resource group.
   - Choose a name and location for the resource group that suits your organization.

2. **Provision Virtual Machines:**
   - Within the resource group, create Azure Virtual Machines running Windows Server.
   - Ensure the VMs are connected to the same virtual network for seamless communication.

## Step 2: Configuring Active Directory Domain Services

Now, let's configure Active Directory Domain Services on our Azure VM:

1. **Install AD DS:**
   - RDP into one of the VMs and install Active Directory Domain Services using Server Manager or PowerShell.

2. **Promote to Domain Controller:**
   - Use the AD DS Configuration Wizard to promote the VM to a domain controller.
   - Choose to create a new forest or join an existing one, depending on your requirements.

3. **Configure DNS:**
   - Ensure DNS is configured correctly on the domain controller. Use the default settings provided during AD DS installation.

## Step 3: Setting Up Active Directory Replication

For redundancy and fault tolerance, let's set up Active Directory replication:

1. **Configure Additional Domain Controllers:**
   - Repeat the previous steps to configure additional domain controllers on other Azure VMs if desired.

2. **Enable Replication:**
   - Configure Active Directory replication to synchronize changes between domain controllers, ensuring data consistency.

## Step 4: Integration with On-premises Resources

Now, let's integrate our Azure-hosted Active Directory with on-premises resources:

1. **Establish VPN Connection:**
   - Set up a site-to-site VPN connection between your on-premises network and Azure Virtual Network.

2. **Update DNS Settings:**
   - Update DNS settings on your on-premises resources to point to the Azure Virtual Machines acting as domain controllers.

## Step 5: Testing and Verification

Time to ensure everything is working smoothly:

1. **Test Domain Join:**
   - Join a test VM or workstation to the Active Directory domain hosted within Azure Virtual Machines to verify domain integration.

2. **Verify Replication:**
   - Confirm that Active Directory replication is functioning correctly between domain controllers to ensure data consistency.

3. **Authentication Testing:**
   - Perform authentication tests using accounts managed by the Azure-hosted Active Directory to confirm user access and permissions.

## Conclusion

Congratulations! You've successfully implemented On-premises Active Directory within Azure Virtual Machines. This setup combines the power of Azure with the familiarity of Active Directory, offering centralized identity management and enhanced scalability for your organization's IT infrastructure.
