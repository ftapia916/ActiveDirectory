  <p align="center">
    <img src="https://github.com/user-attachments/assets/7c9a458b-d110-40bf-82dc-a50291d1bbc8" alt=activedirecotry_logo logo"/>

  
Microsoft Active Directory (AD) is a directory service designed to simplify network management for organizations. Operating on Windows Server, AD efficiently stores and organizes information about network components, including users, devices, and services. It provides convenient access to this information for both administrators and users. Furthermore, AD allows administrators to regulate permissions, manage access to network resources, and create security policies, thus optimizing the overall network management process. <br>

<h2>Technologies used</h2>
-Microsoft Azure <br>
-Remote Desktop <br>
-Active Directory Domain <br>
-PowerShell

<h2>Operating System used</h2>
- Windows 10 <br>
- Windows Server <br>

<h2>Steps setting up in Azure</h2>
<p>
<p align="center">
    <img src="https://github.com/user-attachments/assets/e0b19458-0154-43b3-8b12-9cd0f2a66eed" height="50%" width="50%" alt="step one"/>
</p>
<p>
The Virtual machines have to sit in the same resource group and same virtual network to be connected. The virtual network can be created separately. The Domain Controller will have Windows Server 2022 as the client computer will be in Windows 10. Windows server 2022 has access to the server manager. This will be in use later in the steps. 

</p>
<p>
  <p align="center">
    <img src="https://github.com/user-attachments/assets/2ab69638-e3f0-411b-8460-cbbbaa594f96" height="50%" width="50%" alt="step one"/> 
  </p>
  <p>
In demonstration, the NIC in the domain controller needs to be set to static and the DNS of the client VM needs to be on the same DNS. To check connectivity, turn off the firewall in the domain controller. In the client's computer, pull up Powershell and type in ipconfig/ all. Here the DNS should show the Domain Controller IP address. 

  </p>

<h2>Configuration Steps</h2>
<p>
<p align="center">
    <img src="https://github.com/user-attachments/assets/7eb0a977-4b72-43b0-b0a9-8881d42dfd12"
height="50%" width="50%" alt="step one"/><br>
</p>
<p>
In the Domain Control, download the Active Directory Domain Services: set up a new forest with the domain name (in the workplace it can be the company or department name), restart and log back in with the domain name.

</p>
<p>
<p align="center">
    <img src="https://github.com/user-attachments/assets/9300f0cf-a30f-43b4-b033-d0f9cb785b90"height="50%" width="50%" alt="step one"/>
</p>
<p>
Here, create Domain Adim users by creating new Organizational Units. For the sake of the tutorial use the name _EMPLOYEES and _ADMIN. The new employee would have their name and permissions listed under _EMPLOYEES or _ADMIN. Log out and log back in as the new employee. 
</p>
<p>
<p align="center">
    <img src="https://github.com/user-attachments/assets/33537227-a2e6-4ce0-9b06-dc29a3d60617"height="50%" width="50%" alt="step one"/>
</p>
<p>
Add the client-1 Virtual Machine into the domain. After restarting, the client-1 should show up in the Active Directory Users and Computers (ADUC). Drag the account to _CLIENTS. Under _CLIENTS will have non admin permissions, by logging into client-1 as admin (mydomain.com/alice_admin). 
</p>

<h2>To learn more in depth of Active Directory:</h2>

### [Microsoft Learning Center](https://learn.microsoft.com/en-us/windows-server/identity/ad-ds/get-started/virtual-dc/active-directory-domain-services-overview)


