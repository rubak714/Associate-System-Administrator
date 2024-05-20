# Associate-System-Administrator (LinkedIn)

There are two types of operating systems when managing servers as a system administrator. 
The first would be Windows and the second would be Linux. There are other types like Unix, but the previous two make up the majority of your server types. 

These server operating systems contain applications, file and printer shares, databases like SQL, and many other services that can do amazing things. 

## Operating Systems: Installing, updating, and maintaining OSs

### Server and Clients:
- Directory Services:
-- Whether you use Active Directory for Windows,
-- Open LDAP, or
-- other third-party directory service products, you need a central location to store objects such as users, passwords, groups, printers, and many others. This is needed for administration and security. Without a directory service product, each user would be responsible for the security of their computer and data streams . And that wouldn't be a good security solution.

  Azure has Active Directory, but to mimic on-premises Active Directory there is Azure Active Directory Domain Services. It is not an exact copy of the on-premises Active Directory, but it is very similar. You'll probably see most Windows clients from Windows 11 all the way back to Windows 7. And in some cases perhaps older. Macintosh computers are found in many offices. They are primarily used by graphics and video editors , but some companies may use them exclusively. Only about 1% of all client computers use a variant of Linux for their operating system client. It works similarly to the server products, but without as many features, backup can be a problem for offices that don't have Linux knowledge. The list you see here may be a partial list of what you will manage as a system administrator. In larger companies you might have one or more of these jobs, in a small company you might wear all of these hats, or you might hire consultants to fill the gap. You don't have to be an expert in everything on your first day, although some people might expect you to. You'll learn a little about the products your company uses every day until you're proficient. For example, I have many years of experience with IBM Storage, but if you give me HP Storage to configure I would need some time to learn it. However, I understand the different ways I can connect each type of storage to a server from what I learned in college and studied for certifications. If you learn the underlying technology of all of these topics, any well-made brand will be pretty easy to understand. Servers and clients require a lot of maintenance, whether they are local or in the cloud. Learn what you can, but don't expect to be the most experienced person in any given room until you have some time and experience as a systems administrator.

  As a sysadmin, the following areas are work of daily activities or Management duties for a Sysadmin:
![Screenshot 2024-05-20 112837](https://github.com/rubak714/Associate-System-Administrator/assets/101013219/5000a214-a11a-48fd-9451-0abd38c131cd)

### Active directory:

What is Active Directory? Active Directory is an extensible database that can expand and contract as objects are added or deleted. It includes the ability to securely store object information and authenticate users when they want to access resources. After authenticating a user's credentials, the user is authorized to access shared folders, applications, and others. The schema is a set of rules that define the classes of objects and attributes contained in the directory. It also defines the restrictions and limits on instances of these objects and the format of their names . It is a structure like a tall building with many floors. You can't break the rules that would give you more space or abilities than is allowed. The structure doesn't allow it. If you are assigned a single floor of the building , you cannot leach to another floor or go above or below your assigned floor. This helps keep the structure solid and safe. A global catalog contains information about every object in Active Directory. We need at least one global catalog in every domain and forest or in all user accounts and every other object disappears. This allows users and administrators to find directory information regardless of which domain in the directory actually contains the data. When a system administrator needs to find a user to reset the password, the information is stored in the global catalog. Each domain controller can be a global catalog if desired . Domain controllers contain query and indexing mechanisms so that objects can be published in their properties and found by network users or applications . If a user wants to locate and add a printer , they can do so when it is published to Active Directory, and they can add that printer if permissions allow. When another user wants to open a shared folder on a server, Active Directory searches the access control list of allowed users and Groups to determine whether they have the rights to use this data. A domain controller is a server that can authenticate and authorize users as needed. You have multiple DCs for redundancy and load balancing. The replication service distributes directory data over a network. All domain controllers in a domain participate in replication and contain a complete copy of all directory information for their domain. Any change to directory data is replicated to all domain controllers in the domain. This allows users to log in to server resources as needed, with security and availability guaranteed by the information contained in the domain controllers. Active Directory contains a lot of information to run many services for users. This applies to both on-premises and Azure Active Directory services in the cloud.

  
