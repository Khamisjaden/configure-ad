<p align="center">

<img width="278" alt="Screenshot 2025-01-31 at 08 33 43" src="https://github.com/user-attachments/assets/6815dc53-df90-470b-8a97-4c32b55079b5" />

<h1> Configuring Active Directory within Azure VMs
  



<h2>This tutorial outlines the Active Directory within Azure VMs.





<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Create a bunch of Users 
- Manageing Account Lockouts using group policy
- Enable and Disable Accounts 


<h2>Installation Steps</h2>

<p>
<img <img width="546" alt="Screenshot 2025-01-31 at 18 29 31" src="https://github.com/user-attachments/assets/f7fc938d-0656-4c0a-93ad-1420a28ddb5e" />

</p> I logged into DC-1 as jane_admin and opened Powershell_ise as an administrator. I created a new file and pasted the contents of the script into it. After running the script, I observed the accounts being created. Once the process was complete, I opened Active Directory Users and Computers(ADUC) and varified that the accounts appeared in the correct organizational unit (_EMPLOYEES)
<p>
</p>
<br />

<p>
<img <img width="430" alt="Screenshot 2025-01-31 at 19 06 14" src="https://github.com/user-attachments/assets/408ccddd-8a0d-42a4-a829-4dde3589027b" />


</p> I logged into DC-1 and selected a previously created user account, attempting to log in with an incorrect password ten times. Next, I configured the account lockout threshold through Group Policy. I then observed that the acount was locked out in Active Directory, allowing me to unlock the accountt, reset the password, and attempt to log in again.
</p>
<br />

<p>
<img <img width="348" alt="Screenshot 2025-01-31 at 19 07 48" src="https://github.com/user-attachments/assets/4275e8c4-b67c-4ed9-8db5-e118c345c522" />

<p>I disabled the account in Active Directory and attempted to log in, noting the error messsage that appeared. Afterward, I re-enabled the account and tried logging in again
</p>
<br />
