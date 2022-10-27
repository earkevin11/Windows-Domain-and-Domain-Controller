# Windows-Domain-and-Domain-Controller

# What are Windows Domains?
- Allows admins to manage large comptuer networks
- Generally contain a large number of computers on the same network

# What are Domain Controllers?
- Windows Domain uses a windows server called a Domain Controller. Often referred to as "DC"
- Domain Controller is any <strong> <em> SERVER </strong> </em> that has the AD DS role installed.
- DC server's job is to <strong> <em> HANDLE AUTHENTICATION REQUEST </strong> </em> across the domain.
- DCs contains Active Directory and Group Policy
- You can have several Domain Controllers within a Domain but there is only a primary DC.
- Primary reason to have more than one DC is fault tolerance. Critical data would be replicated to the other DC.
- <b> Domain Controllers uses Active Directory to manage users, computers, and act as a directory service for printers and files shares. <b>

<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/176091217-33e788be-4732-42e2-8ae5-bc9f0d9c48cc.png" height="75%" width="75%" alt="Azure LAW"/>

<p/>

# What is Active Directory?
- AD is a tool used to manage users, computers, printers, file shares, and groups.
- AD uses objects and organizational units (folders)


# Group Policy Management 
- GP is used to manage all domain users and computers remotely.
- GP uses Group Policy Objects (GPOs) to manage client settings
- GP can be used to target specific usres, computers, groups, or OUs
- Can install software remotely or anything you want to configure such as users' desktop background
- Manage what website they can visit
- Manage and configure security settings


# Install AD Domain Service
<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/176195321-584cdfde-312c-43f8-a1ed-5e5511de77db.png" height="75%" width="75%" alt="Azure LAW"/>

<p/>

# After installation, click the flag and select "promote this server as a domain controller"
<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/176196137-b12f8e0e-fc37-40c5-8281-0f4d463ad68c.png" height="75%" width="75%" alt="Azure LAW"/>

<p/>


# Create a domain called ITFLEE.COM
- Subdomain or child would be called courses.itflee.com
<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/176196984-0f82cb37-f23a-4cb9-92b2-3cb0a7212a19.png" height="75%" width="75%" alt="Azure LAW"/>

<p/>

# Click install and wait for installing of the AD DS Role
<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/176199531-2d92fc7b-8342-4005-b9c1-536351f36069.png" height="75%" width="75%" alt="Azure LAW"/>

<p/>


# After installation, the Virtual machine will restart. You can see the new roles installed.
<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/176204463-f4613f38-e677-4f32-adab-5ed740771324.png" height="75%" width="75%" alt="Azure LAW"/>

<p/>


# Download Windows 10 OS from Microsoft and Install
- Select Create Installationn media for another PC

<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/176205847-646f0905-6386-4f47-b829-96ac2fa800ac.png" height="75%" width="75%" alt="Azure LAW"/>

<p/>


# Create a new virtual machine from virtual box and mount the Windows 10 ISO
<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/176215694-34ca8793-8ba9-4bdf-abba-c8d626996ec1.png" height="75%" width="75%" alt="Azure LAW"/>

<p/>

# Start machine and install Windows 10

<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/176215832-5fdeb78c-b54b-4f2c-bf17-3ddf88ed9a23.png" height="75%" width="75%" alt="Azure LAW"/>

<p/>


# Reminder to install VM Box Guest Additions
- After installation, things like copying and paste between VM and host will work

<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/176219041-89938689-e622-4354-b0d0-41e79aa92c61.png" height="75%" width="75%" alt="Azure LAW"/>

<p/>


# It will prompt you to enter the domain name that you want to join
- Itflee.com is the domain controller on the other workstation
<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/176329388-f81f837a-6587-407e-af84-a6a82f4939f7.png" height="75%" width="75%" alt="Azure LAW"/>

<p/>

# Domain join our Windows 10 VM workstation  #17 of video
- First, ensure that both the Domain Controller (KevinVM) and workstation (Windows 10 VM) are on the same network. 
- Check Network section on virtual box for both virtual machines.

<p align="center">
  
<img src="![join Windows 10 to domain controller](https://user-images.githubusercontent.com/104326475/176329229-425005a4-3190-42f9-a13d-8eae4baf2160.png)" height="75%" width="75%" alt="Azure LAW"/>

<p/>

# Add credentials that you created for Windows 2016 Server
<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/176329252-d324323f-2521-41f5-8636-45194015af03.png" height="75%" width="75%" alt="Azure LAW"/>

<p/>

# This is our domain that we want to join. It is our virtual machine (KevinVM) that has the AD Domain Service role installed.
- Remember, any server that has AD DS role installed is a DOMAIN CONTROLLER

<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/176330352-3f48eb1c-f627-4da0-a621-49b0d4be2349.png" height="155%" width="155%" alt="Azure LAW"/>

<p/>

# This is how we can check if our Windows 10 VM, named ITFWS01, domain joined to our domain controller virtual machine (KevinVM)
- Tools > Active Directory Users and Computers > ITflee.com > Computers > You should see the comptuer of Windows 10 VM (ITFSW01)

<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/176330472-f3cf7993-ab7c-4087-8cfc-1a0c89c25594.png" height="155%" width="155%" alt="Domain Controller"/>

<p/>

# What are organization units?
- They're essentially folders.

# What OU is a computer placed into by default when it is joined to a domain?
- Computers 

# What does a PING command do?
- Sends a message to target host asking for a response

# Regarding the TCP/IP settings of a domain workstation, what IP address should you configure for your DNS server settings?
- The IP address of a domain controller

# What tool do you use to run a PING command?
- Command Prompt

# (True or false) A computer that is joined to a Windows Domain also needs its Workgroup to be configured.
- False. It should automatically update.

# On any computer on which you are configuring the TCP/IP setting, what IP address should you enter for the default gateway?
- The IP address of the switch that the computer is connected to, or the IP address of the virtual network the computers is connected to.
