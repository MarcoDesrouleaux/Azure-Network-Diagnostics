# How to Connect 2 Virtual Machines Together Using Microsoft Azure

## Introduction
This guide demonstrates how to connect two virtual machines (VMs) together within Microsoft Azure. By following this tutorial, you'll learn to create and connect VMs, enabling secure communication between them.

## Prerequisites
- An active Microsoft Azure account
- Basic understanding of virtual machines and networking

## Step 1: Setting Up the First Virtual Machine
1. Log in to your Azure portal.
2. Navigate to 'Create a resource' > 'Compute' > 'Virtual Machine.'
3. Configure the VM settings as required, including the virtual network and subnet.
4. Click 'Create' to deploy the VM.

## Step 2: Setting Up the Second Virtual Machine
1. Repeat the process for the first VM.
2. Ensure that the second VM is on the same virtual network as the first.

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
