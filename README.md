<h2>Active Directory Project Part 4</h2>

<h3>Objectives</h3>
- Install & Configure Active Directory onto Server 
<br />
- Promote Domain Controller
<br />
- Configure Target Machine to Join Domain 
<br />
<br />

To begin, I open "Server Manager" on my server virtual machine and proceed to install the Active Directory Domain Services. Interestingly, this turned out to be quite challenging as my virtual machine repeatedly crashed during the installation process, requiring several days and a stroke of luck to finally complete the installation successfully. Following the installation, the next step is to promote the server to a domain controller. This involves adding a new forest and naming it with ".local" at the end, setting a password, and progressing through the installation steps. Once the installation is complete and the server resets, observing the domain followed by a backslash indicates that Active Directory Domain Services were successfully installed, and the server was promoted to the domain controller.
<br />
<br />
<img src="https://github.com/Yagoobz/ActiveDirectoryProjectPart4/assets/145611184/7a57e190-6138-42e2-b4d2-dfbaa05d9d7d" height="30%" width="70%" alt="Disk Sanitization Steps"/>

Next, I proceed to create user accounts within the Active Directory environment. Within "Server Manager," I access "Active Directory Users and Computers" to initiate this process. In order to mimic a real-world organizational structure, I create two organizational units (OU) by right-clicking on the domain and selecting "Organization Unit." I name these units "IT" and "HR" respectively. Within each unit, I create a user account complete with a name, username, and password, representing the users within those departments.
<br />
<br />
<img src="https://github.com/Yagoobz/ActiveDirectoryProjectPart4/assets/145611184/7bf0133c-0b64-4388-98fd-8a93a75c9222" height="30%" width="70%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://github.com/Yagoobz/ActiveDirectoryProjectPart4/assets/145611184/b5e8ab27-d733-40e9-8570-e0af4cf99e73" height="30%" width="70%" alt="Disk Sanitization Steps"/>

With the Active Directory setup and the server functioning as a domain controller, I proceed to integrate the Windows target machine into the newly established domain and authenticate it using one of the organizational units. Initially, I update the DNS server address on the target machine to point to the domain controller, ensuring correctness. Next, I access "Advanced system settings" and modify the domain to "(myname).local." Following this, I input the correct administrator credentials, successfully connecting the target machine to the domain.
<br />
<br />
<img src="https://github.com/Yagoobz/ActiveDirectoryProjectPart4/assets/145611184/0095251e-5807-4276-85e6-6558404d0d1d" height="30%" width="70%" alt="Disk Sanitization Steps"/>

After restarting the virtual machine, I attempt to log in using one of the newly created user accounts. Upon selecting "Other user" for sign-in, the login prompt correctly points to my domain, indicating successful integration. Everything seems to be functioning perfectly!
<br />
<br />
<img src="https://github.com/Yagoobz/ActiveDirectoryProjectPart4/assets/145611184/399ad145-d4e3-4fca-b8ef-e78bcb39370b" height="30%" width="70%" alt="Disk Sanitization Steps"/>
