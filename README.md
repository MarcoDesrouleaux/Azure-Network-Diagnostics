# VM Network Reachability Project

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
1. Verify the Networking page then leave as is.
<img src="https://i.imgur.com/Xg5EZXc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

### 2.4 Review & Create a Virtual Machine
1. Once it starts validating the information to see if everything is clear, you will see "Validation Passed" on the left side of the screen. Then you can proceed to create the virtual machine.
<img src="https://i.imgur.com/vOe7RQS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
2. Once you click the "Create button", you will see "Your deployment is complete". That is when your virtual machine will be created.
<img src="https://i.imgur.com/s8Y5l1Y.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
3. Search and click on "Virtual Machines" from the search bar to look for the VM you created.
<img src="https://i.imgur.com/3HLNBB6.png" width="80%" alt="Disk Sanitization Steps"/>
4. The 2nd Virtual Machine is now created.
<img src="https://i.imgur.com/W2RK5vs.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

## Step 3: Configuring Networking Between VMs (We will use Remote Desktop for Windows) 
## Side Note: MacOS Users have to download the "Microsoft Remote Desktop" on the App Store.
<img src="https://i.imgur.com/DefN6Ca.png"/>

### 3.3 Connecting VMs to Host Computer
<br>1. On the Virtual Machines page, click on VM1.
<img src="https://i.imgur.com/fG3ViG9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br>2. Once you open VM1, copy the Public IP address on the right side of the page. For this example: We will copy "20.88.18.59" from the page.
<img src="https://i.imgur.com/VseLPOC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br>3. Once copied, click on the start menu to look for "Remote Desktop Connection" and open it.
<br>4. Paste it on where it says "Computer" then click the "Connect button".
<table>
<tr>
<td>
<img src="https://i.imgur.com/1tmvX3B.png" alt="Image 1 Description" width="100%"/>
</td>
<td>
<img src="https://i.imgur.com/M1fYSOq.png" alt="Image 1 Description" width="100%"/>
</td>
</tr>
</table>
<br>5. Enter the credentials you used when you created VM1.
<br>6. For this example: We will use the username "Azureuser" with the password I chose earlier to create VM1.
<table>
<tr>
<td>
<img src="https://i.imgur.com/q0odoQf.png" alt="Image 1 Description" width="100%"/>
</td>
<td>
<img src="https://i.imgur.com/fr0L1Q7.png" alt="Image 1 Description" width="100%"/>
</td>
</tr>
</table>
<br>7. Click the "Yes" button to continue.
<img src="https://i.imgur.com/vvJlY2o.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br>8. After the page finishes to load, set the privacy settings the way you want. Then press the "Accept" button to continue.
<img src="https://i.imgur.com/KU12aOq.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br>9. Now VM1 is running on our host computer.
<img src="https://i.imgur.com/ig5KLE1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

## Step 4: Testing the Connection
In order to PING or test the connection between VM1 and VM2. We must know the IP address for it.
<br>1. On the Virtual Machines page, click on VM2.
<img src="https://i.imgur.com/tKUPoKL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br>2. Once you open VM2, copy the Private IP address on the right side of the page. For this example: We will copy "10.0.0.5" from the page.
<img src="https://i.imgur.com/U0cmROy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br>3. Once copied, click on the start menu in VM1 to look for "Windows PowerShell" and open it.
<table>
<tr>
<td>
<img src="https://i.imgur.com/W7CKDmP.png" alt="Image 1 Description" width="100%"/>
</td>
<td>
<img src="https://i.imgur.com/QDtT4ul.png" alt="Image 1 Description" width="100%"/>
</td>
</tr>
</table>
<br>4. On Windows PowerShell, type "ping 10.0.0.5".
<img src="https://i.imgur.com/YaAMZfZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br>5. Once you press enter and if there are 0 packets lost it means that all the messages sent from one computer (or VM) to another were successfully received. This is a good indication that the network connection between the two is stable and reliable, without any loss of data. 
<img src="https://i.imgur.com/Oehxe6d.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


## Conclusion
You have successfully connected two virtual machines together in Microsoft Azure. This setup allows for secure communication between VMs and serves as a foundation for more complex networking scenarios.

## References
- [Microsoft Azure Virtual Networking Documentation](link-to-documentation)
