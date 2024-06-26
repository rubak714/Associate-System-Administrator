# Associate-System-Administrator (LinkedIn and Udemy)

There are two types of operating systems when managing servers as a system administrator. 
The first would be Windows and the second would be Linux. There are other types like Unix, but the previous two make up the majority of your server types. 

These server operating systems contain applications, file and printer shares, databases like SQL, and many other services that can do amazing things. 

## Installation and configuration of Domain Controller, Active Directory, DNS, WebServer (IIS), Group Policy, WSUS and more

### Server and Clients:
- Directory Services:
-- Whether you use Active Directory for Windows,
-- Open LDAP, or
-- other third-party directory service products, you need a central location to store objects such as users, passwords, groups, printers, and many others. This is needed for administration and security. Without a directory service product, each user would be responsible for the security of their computer and data streams . And that wouldn't be a good security solution.

  Azure has Active Directory, but to mimic on-premises Active Directory there is Azure Active Directory Domain Services. It is not an exact copy of the on-premises Active Directory, but it is very similar. You'll probably see most Windows clients from Windows 11 all the way back to Windows 7. And in some cases perhaps older. Macintosh computers are found in many offices. They are primarily used by graphics and video editors , but some companies may use them exclusively. Only about 1% of all client computers use a variant of Linux for their operating system client. It works similarly to the server products, but without as many features, backup can be a problem for offices that don't have Linux knowledge. The list you see here may be a partial list of what you will manage as a system administrator. In larger companies you might have one or more of these jobs, in a small company you might wear all of these hats, or you might hire consultants to fill the gap. You don't have to be an expert in everything on your first day, although some people might expect you to. You'll learn a little about the products your company uses every day until you're proficient. For example, I have many years of experience with IBM Storage, but if you give me HP Storage to configure I would need some time to learn it. However, I understand the different ways I can connect each type of storage to a server from what I learned in college and studied for certifications. If you learn the underlying technology of all of these topics, any well-made brand will be pretty easy to understand. Servers and clients require a lot of maintenance, whether they are local or in the cloud. Learn what you can, but don't expect to be the most experienced person in any given room until you have some time and experience as a systems administrator.

  As a sysadmin, the following areas are work of daily activities or Management duties for a Sysadmin:

<img src="https://github.com/rubak714/Associate-System-Administrator/assets/101013219/5000a214-a11a-48fd-9451-0abd38c131cd" alt="Description of image" width="1000" >

### Active directory:

- What is Active Directory? Active Directory is an extensible database that can expand and contract as objects are added or deleted. It includes the ability to securely store object information and authenticate users when they want to access resources. After authenticating a user's credentials, the user is authorized to access shared folders, applications, and others. 
- The schema is a set of rules that define the classes of objects and attributes contained in the directory. It also defines the restrictions and limits on instances of these objects and the format of their names . It is a structure like a tall building with many floors. You can't break the rules that would give you more space or abilities than is allowed. The structure doesn't allow it. If you are assigned a single floor of the building , you cannot leach to another floor or go above or below your assigned floor. This helps keep the structure solid and safe.
- A global catalog contains information about every object in Active Directory. We need at least one global catalog in every domain and forest or in all user accounts and every other object disappears. This allows users and administrators to find directory information regardless of which domain in the directory actually contains the data. When a system administrator needs to find a user to reset the password, the information is stored in the global catalog. Each domain controller can be a global catalog if desired . Domain controllers contain query and indexing mechanisms so that objects can be published in their properties and found by network users or applications . If a user wants to locate and add a printer , they can do so when it is published to Active Directory, and they can add that printer if permissions allow. When another user wants to open a shared folder on a server, Active Directory searches the access control list of allowed users and Groups to determine whether they have the rights to use this data. A domain controller is a server that can authenticate and authorize users as needed. You have multiple DCs for redundancy and load balancing. The replication service distributes directory data over a network. All domain controllers in a domain participate in replication and contain a complete copy of all directory information for their domain. Any change to directory data is replicated to all domain controllers in the domain. This allows users to log in to server resources as needed, with security and availability guaranteed by the information contained in the domain controllers. Active Directory contains a lot of information to run many services for users. This applies to both on-premises and Azure Active Directory services in the cloud.

<img src="https://github.com/rubak714/Associate-System-Administrator/assets/101013219/23a1907a-86d9-4492-b094-deb502c73bf4"  height="300" width="700" >
<img src="https://github.com/rubak714/Associate-System-Administrator/assets/101013219/9a2a8904-6b3e-4948-bd81-17eb7425de57"  height="300" width="700" >
<img src="https://github.com/rubak714/Associate-System-Administrator/assets/101013219/e26fed0e-89a8-4568-b8d5-bed2f8e2404b"  height="300" width="700" >
<img src="https://github.com/rubak714/Associate-System-Administrator/assets/101013219/4f7e8f2b-5f72-4ff8-bf83-a9c19eee06c2"  height="300" width="700" >
<img src="https://github.com/rubak714/Associate-System-Administrator/assets/101013219/bf128e75-f5a6-475a-8fd0-f89500a3a791"  height="300" width="700" >

### Operating Systems Instalation:

- There are several ways to install an operating system, although you must decide which best suits your company's needs. It certainly helps to have all the facts. The simplest, most interactive, but slowest installation is manual, also called attended installation. Here you install a DVD into your DVD drive and carry out the installation. You need to make individual decisions about the partition size, file locations, network, and other settings. This applies to every operating system. Each of these decisions is called an answer. 
- A response file is used in an unattended installation. This file can be downloaded from Microsoft for Windows installations . You enter things like the computer name, administrator account, network, whether or not it should be joined to a domain, and more. Linux and Unix can also use response files.
- A headless installation is one where you do not use a monitor. Another device connects to it remotely and sets up the machine. This is not a common way to install Windows, but it is possible. A network installation uses the pre-execution environment or PXC boot options that appear when booting into setup mode. Setting this as the default boot option can automatically connect to a Windows deployment server over the network and deploy the operating system with predefined settings and preinstalled software. This is a common practice among larger organizations. There are also third-party products that can perform network installation with different operating systems if necessary . You can schedule a network installation or install immediately. This can be done on a formatted hard drive with no data or on a drive that already has an operating system where everything is deleted and formatted with a new operating system.

- All of these types of installations can occur on a physical computer or using a virtual machine running as a guest operating system on a host computer . Windows is free with Hyper-V for virtual machines preinstalled, but you still need to purchase operating system licenses. Other products include VMware, VirtualBox, Xen and more. They all work in a similar way. You can even host these virtual machines in Azure, Amazon Web Services, and other organizations. Operating system installation decisions may affect how much time you have available for customer support. Be sure to take the time to figure out which one is right for your business.

### Microsoft Center Suite:
System Center is a suite of applications intended for both on-premises and cloud resources. They allow CIS administrators to manage all of your devices in your organization. System Center solved a major problem for CIS administrators from previous years. They had to control computers to deploy and secure them. Microsoft has developed a centralized system that has evolved over the years to include mobile devices and cloud devices. There is a long history of System Center products with Microsoft. System Manager Server was originally provided with NT4 in the 1990s. This product was difficult to use and primarily provided Microsoft and third-party applications to control and monitor basic computer functions. MOM or Microsoft Operations Manager came out in 2000 to integrate Active Directory with SMS. We could now use Group Policy and Security Groups to manage computers and deploy products such as applications and operating systems and to monitor computers and servers. In 2007 we had the first System Center Suite. The main product was the configuration manager. Microsoft said it can deploy operating systems, software applications, software updates, measure software usage, assess deviations from desired configurations, provide hardware and software inventory and manage computers remotely. That's a lot for one program. 2012 System Center was improved over 2007, but added additional functionality with Orchestrator for mobile device management and better endpoint protection features. The most important innovations concerned mobile and general security. 2016 System Center is more about refining and updating 2016 features, such as: B. Integration with Intune for even better mobile management and better monitoring and resource management. The 2019 System Center release focused on three main areas. It adds more functionality to the existing components and features . It brought integration for Windows Server 2019, and System Center 2019 adds more hybrid cloud integrations with Microsoft Azure. Configuration Manager manages PCs, servers and mobile devices such as Apple and Android. Data Protection Manager can back up and restore data for servers, applications and services. Operation Manager monitors servers, services and all types of devices across the company. It helps identify problems and can provide scripts for immediate fixes. Orchestrator automates the creation and deployment of resources in the Windows Azure environment. Service Manager manages incidents and controls the asset lifecycle. Service management automation can automate the creation and provisioning of resources in Windows Azure. Virtual Machine Manager provides and manages resources needed to quickly create and deploy virtual machines. Service Provider Foundation delivers Infrastructure-as-a-Service to customers by providing virtual machine management capabilities. Endpoint Protection was previously part of System Center Configuration Manager, but is now embedded in the SCCM client that is pushed to every computer that uses SCCM. There is no longer a need for a separate product in the suite as it is integrated. Understanding System Center's history will help you appreciate the application in its current form and see how Microsoft has developed its product over two decades. For the modern CIS administrator, System Center may be a good choice for your organization.

# Udemy

<img src="https://github.com/rubak714/Associate-System-Administrator/assets/101013219/c2860864-4602-4f13-81b6-90967790aa5b"  width="700" >
<img src="https://github.com/rubak714/Associate-System-Administrator/assets/101013219/2ccf2dfd-e3b6-408d-99c5-08d2fb2871a2"  width="700" >
<img src="https://github.com/rubak714/Associate-System-Administrator/assets/101013219/d17fab02-2a7e-4f8b-bdda-99b50d730eb9"  width="700" >
<img src="https://github.com/rubak714/Associate-System-Administrator/assets/101013219/5ccb4d40-0748-491f-a959-fa0b84231831"  width="700" >
<img src="https://github.com/rubak714/Associate-System-Administrator/assets/101013219/6bfe62ec-95a9-416a-a9be-b4fea44820d7"  width="700" >
<img src="https://github.com/rubak714/Associate-System-Administrator/assets/101013219/d99dd757-e9b5-4525-8008-f71ab4ee6af9"  width="700" >
<img src="https://github.com/rubak714/Associate-System-Administrator/assets/101013219/0231d7bb-2562-4155-8b13-f58e40aad44f"  width="700" >
<img src="https://github.com/rubak714/Associate-System-Administrator/assets/101013219/0742cb87-f531-4fb5-b3d2-29f46c5778bf"  width="700" >
<img src="https://github.com/rubak714/Associate-System-Administrator/assets/101013219/4c9e492d-ddda-4583-8070-61b3df5cfbca"  width="700" >
<img src="https://github.com/rubak714/Associate-System-Administrator/assets/101013219/78d73f5b-fc6c-44f3-9f8a-e57c8557fc06"  width="700" >
<img src="https://github.com/rubak714/Associate-System-Administrator/assets/101013219/0be98b19-c539-457f-98bb-7d08e27b05c3"  width="700" >
<img src="https://github.com/rubak714/Associate-System-Administrator/assets/101013219/83aa4780-1f6d-4c5e-999c-bd5d7b54cef5" width="700" >


By: Imran Afzal
## Module 1 – Understanding of Microsoft Windows
•	What is Windows?
•	Different Versions of Windows
•	Microsoft Background and Products
•	Windows Market Share - Everyday Windows
•	Windows vs. Linux vs. MAC
•	Quiz, Handouts and Homework

## Module 2 – Setting up a Lab
•	Oracle Virtual Box
•	Installing Oracle Virtual Box
•	Creating First Virtual Machine
•	Quiz, Handouts and Homework

## Module 3 - Windows Installation and Configuration
•	Different Ways to Install OS
•	Downloading Windows Server 2016
•	Installing Windows Server 2016
•	Adding Resources
•	Hostname and System Information
•	Windows Server GUI Overview
•	Quiz, Handouts and Homework

## Module 4 - System Access and File System
•	Accessing Windows System
•	File System and Description
•	Navigating to File System
•	File Types and Creation
•	File Properties
•	Finding Files and Directories
•	File Maintenance (copy, delete, move and rename)
•	Files Operations
•	File Editing Short-Cut Keys
•	Quiz, Handouts and Homework

## Module 5 - System Administration
•	User Account Management
•	Elevating User Roles
•	Monitor Users Activity (Task manager and command line)
•	System Utilities Under Accessories
•	Programs and Service Management (Control panel and services)
•	System Resource Monitoring (Task Manager)
•	Windows Event Logs
•	System Maintenance
•	Jobs and Schedules
•	Windows Settings
•	Server Manager Dashboard
•	Installing and Uninstalling Programs
•	Windows Applications (Microsoft or 3rd Party)
•	Windows Short-Cut Keys (e.g. Alt+Ctl+Del etc.)
•	Check System Hardware
•	Quiz, Handouts and Homework

## Module 6 - Advance Windows Administration
•	Roles vs. Features
•	Adding Roles and Features
•	What is Domain Controller?
•	Domain Controller and Active Directory
•	Active Directory Prerequisites
•	What is DNS?
•	Active Directory Installation
•	Active Directory "Users and Computers“
•	Active Directory User Account Management
•	Installing Windows Client
•	Joining the Domain from Windows 7 and 10
•	Active Directory "Administrative Center“
•	Active Directory "Domain and Trust“
•	Active Directory "Module for Windows PowerShell“
•	Active Directory "Site and Services“
•	Group Policy Management
•	DNS Administration
•	Web Server (IIS) Installation
•	Quiz, Handouts and Homework

## Module 7 - Windows Scripting and Command Line
•	Windows Batch Scripting
•	First Batch Script "Hello World“
•	Script to Automate Simple Tasks
•	Windows PowerShell
•	Windows PowerShell Commands
•	Windows PowerShell ISE (Integrated Scripting Environment)
•	Windows Management Instrument (WMIC)
•	Difference Between DOS and PowerShell
•	Quiz, Handouts and Homework

## Module 8 - Networking and System Updates
•	What is NIC?
•	Enable Internet on the VM
•	NIC Teaming
•	Network Configuration
•	Windows Updates
•	NTP Configuration
•	File Transfer Methods
•	FTP Server Installation and Configuration
•	Sharing FileSystem (Samba or NFS)
•	WSUS Server Installation and Configuration
•	Windows Firewall
•	Quiz, Handouts and Homework

## Module 9 – Storage Management
•	What is Computer Storage?
•	Type of Computer Storage
•	How to Add Disk
•	Extend an Existing Disk
•	Disk Cleanup and Defragmentation
•	RAID
•	Windows Backup and Restore
•	Quiz, Handouts and Homework

## Module 10 - Additional Resources (Bonus)
•	What is IT?
•	IT Components
•	Facts about IT
•	IT Management Jobs
•	Resume Workshop
•	Interview Workshop
•	Post Resume and What to Expect
•	VMWare Workstation Player Download and Installation
•	Install Oracle VirtualBox on MAC
•	Quiz, Handouts and Homework


# Module 1:


Well, Windows is an operating system which sits in the middle of your hardware and users.

So you have a hardware, right?

A piece of brick that or it's your laptop that you could feel you could touch it.

Then you actually strike some commands on your keyboard and then you run, you create some programs,

you run those programs, right?

But there is a middleman in the middle that actually allows you to do that.

That middleman is the operating system.

And this topic, this lesson, we are going to learn the Windows operating system.






