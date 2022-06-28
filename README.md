# Windows-Domain-and-Domain-Controller

# What are Windows Domains?
- Allows admins to manage large comptuer networks
- Generally contain a large number of computers on the same network

# What are Domain Controllers?
- Windows Domain uses a windows server called a Domain Controller. Often referred to as "DC"
- Domain Controller is any <strong> <em> SERVER </strong> </em> that has the AD DS role installed.
- Server's job is to handle authentication request across the domain.
- DCs contains Active Directory and Group Policy
- You can have several Domain Controllers within a Domain but there is only a primary DC.
- Primary reason to have more than one DC is fault tolerance. Critical data would be replicated to the other DC.
- Domain Controllers uses Active Directory to manage users, computers, and act as a directory service for printers and files shares.

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


