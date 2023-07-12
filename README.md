<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
In this tutorial I will outline the prerequisites and installation of the open-source help desk ticketing system osTicket.


<h2>Objectives</h2>

-  More Experience with Azure (I will Create the environment here)
-  Experience as both the administrator AND the user of a ticketing system
-  Gain a better understanding of all parts of ticketing system such as <b>Tickets properties, SLAs, Departments, Permissions</b> and <b>Users</b>.

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)

<h2>List of Prerequisites</h2>

- All you need for this lab is the Azure Tenant and Subscription
    
<h2>Installation Steps</h2>

-  Step 1: Create VM1

First thing first, I will create a Research Group (RG-osTicket) in www.portal.azure.com and then create a Virtual Machine(VM1) and Azure automatically assigns me a virtual network and subnet. I chose Windows 10 as OS and 2Vcpu for my VM1 and created a username. Just a reminder that I created VM1 under RG-osTicket.

![image](https://github.com/danielbangm/osticket-prereqs/assets/22795502/84f84161-9647-4480-b518-ea73ed24b20b)

-  Step 2: Connect to VM1 using RDP

I connected to VM1 via Remote Desktop Connection using VM1's public IP address(20.51.185.57) from the Azure Portal. Then I am prompted to login and now have access to VM1. I use Remote Desktop Connection because my PC runs Windows OS but if you happen to be on a MAC I would recommend to download and Install Microsoft Remote Desktop first.

![image](https://github.com/danielbangm/osticket-prereqs/assets/22795502/0dc6df39-2748-4f99-bbf5-e431e98f97ca)

-  Step 3: Install and Enable <b>IIS</b> in Windows with CGI and common HTTP features

Internet Information Service(IIS) is essentially a web server that allows our computer to serve up websites because osTicket runs out of a website. Go to control panel -> programs -> Turn windows features on and off. Then chech up this boxes by allowing: World Wide Web Services -> Application Development Features -> CGI -> Common HTTP Features.

![image](https://github.com/danielbangm/osticket-prereqs/assets/22795502/522227e8-ff10-4ff2-b6f9-1b321fb6af17)

-  Step 4: Confirm IIS is installed

After enabling IIS in Windows WITH CGI, Common HTTP Features and IIS Management Console, I open a web browser in VM1 and type 127.0.0.1 to check if my web server is up and I have a result looking like this 

![image](https://github.com/danielbangm/osticket-prereqs/assets/22795502/9d293999-5a5a-42be-a028-94fa69de494d)

-  Step 5: Download and Install PHP manager for IIS

From the <a href="https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6">Installation Files</a>, download and install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi). download and install the Rewrite Module (rewrite_amd64_en-US.msi). 


