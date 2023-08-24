# How to Connect 2 Virtual Machines Together Using Microsoft Azure

## Introduction
This guide demonstrates how to connect two virtual machines (VMs) together within Microsoft Azure. By following this tutorial, you'll learn to create and connect VMs, enabling secure communication between them.

## Prerequisites
- An active Microsoft Azure account
- Basic understanding of virtual machines and networking

## Step 1: Sign in to Azure Portal
1. Open your browser and navigate to [Azure Portal](https://portal.azure.com).
2. Enter your email address and password to sign in.
<img src="https://i.imgur.com/ExNiOVz.png"/>

## Step 2: Setting Up the First Virtual Machine
1. Create a resource group.
<img src="https://i.imgur.com/DZiwlcD.png"/>
2. Create your first virtual machine after creating the resource group.
<img src="https://i.imgur.com/0TPmNH6.png"/>
3. Your first virtual machine is now created.
<img src="https://i.imgur.com/Rc8GLM8.png"/>

## Step 2: Setting Up the Second Virtual Machine
### 2.1 Provide Basic Information for the Basics page
## Project details 
1. Select the appropriate Subscription.
2. Create or select an existing 'Resource Group. For this example: we will select "Azure-Lab-1".
## Instance details
3. Enter a name for your virtual machine. For this example: We will name it "VM2".
4. Choose a region closest to your location. For this example: We will select "(US) North Central US".
5. Choose the Virtual Machine Image. For the example: We will select "Ubuntu Server 20.04 LTS - x64 Gen2".
6.  Select the desired 'Size' for your virtual machine. For the example: We will select "Standard_E2s_v3 - 2 vcpus, 16 GiB memory ($91.98/month)".
## Administrator account
7. Select "Password" instead of using SSH public key.
8. For the 2nd virtual machine: Use the same "Username & Password" you used for the 1st virtual machine you created. (If you forget the password, you will have to delete and create another VM.)
<table>
<tr>
<td>
<img src="https://i.imgur.com/2Whx8Eu.png" alt="Image 1 Description" width="100%"/>
</td>
<td>
<img src="https://i.imgur.com/yyJH46c.png" alt="Disk Sanitization Steps" width="100%"/>
</td>
</tr>
</table>

### 2.2 Provide Basic Information for the Disks page
1. Leave the page as is.
<img src="https://i.imgur.com/iLT6u9s.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

### 2.3 Provide Basic Information for the Networking page
1. Verify the public and private IP Addresses then leave the page as is.
<img src="https://i.imgur.com/A3JyALs.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

### 2.4 Review & Create a Virtual Machine
1. Once it starts validating the information to see if everything is clear, you will see "Your deployment is complete". That is when your virtual machine will be created.
<img src="https://i.imgur.com/qnYPKTM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
2. Search and click on "Virtual Machines" from the search bar to look for the VM you created.
<img src="https://i.imgur.com/MdXKfgO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
3. The Virtual machine is now created.
<img src="https://i.imgur.com/Rc8GLM8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

## Step 3: Configuring Networking Between VMs

### 3.1 Creating Virtual Network
1. In Azure portal, navigate to 'Virtual networks' > 'Add.'
2. Configure the virtual network settings, ensuring it matches the virtual network of the VMs.
3. Click 'Create.'

### 3.2 Configuring Subnets
1. Within the virtual network, navigate to 'Subnets' > 'Add.'
2. Configure the subnet settings to enable communication between the VMs.
3. Click 'Create.'

### 3.3 Connecting VMs
1. In the virtual network settings, navigate to 'Peerings.'
2. Configure the peering settings to connect the two VMs.
3. Validate the connection between the VMs.

## Step 4: Testing the Connection
1. Connect to the first VM through SSH or Remote Desktop.
2. Use `ping` or other networking tools to test the connection to the second VM.

## Conclusion
You have successfully connected two virtual machines together in Microsoft Azure. This setup allows for secure communication between VMs and serves as a foundation for more complex networking scenarios.

## References
- [Microsoft Azure Virtual Networking Documentation](link-to-documentation)
