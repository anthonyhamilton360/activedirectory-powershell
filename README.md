
![Screenshot 2025-03-15 190857](https://github.com/user-attachments/assets/5ac6045a-86bf-4b1a-b068-d695f4e7820e)


</p>

<h1>Creating Users with Powershell</h1>
This tutorial explores deploying an Active Directory environment, from creation and management to deactivation and removal.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Powershell

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Setup Remote Desktop for non-administrative users on Client-1 
- Create users and attempt to log into client-1 with one of the users
- Item 3
- Item 4

<h2>Lifecycle Stages</h2>

<p>
  
![Screenshot 2025-03-10 082603](https://github.com/user-attachments/assets/fdb618ca-fcfb-4e6a-a3b0-fd34831403b4)

</p>
<p>
To launch client-1 and dc-1 virtual machines, go to Azure's virtual machines section and choose both. 
</p>dd
<br />

<p>
  
![Screenshot 2025-03-10 082611](https://github.com/user-attachments/assets/0bcebfce-3ef2-4021-92fa-0fc4756225e5)

</p>
<p>
Select Yes.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 084854](https://github.com/user-attachments/assets/315a3a87-47b4-427f-8ed1-c46c5d25ac16)

</p>
<p>
Copy client-1's IP address, paste it into Remote Desktop, and choose Connect.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 085122](https://github.com/user-attachments/assets/ab5bb14f-51ed-4eb8-a7e5-cab4406f066a)

</p>
<p>
Right-click the Start menu in the client-1 virtual machine and choose System.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 085137](https://github.com/user-attachments/assets/6c03f2e5-c84c-4b82-90a4-5ad5cc2a2aad)

</p>
<p>
Select Remote Desktop on the right.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 085243](https://github.com/user-attachments/assets/daf77953-2283-4405-8758-9e65627bfb9d)

</p>
<p>
Under User Accounts, click on Select users that can remotely access this PC.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 085321](https://github.com/user-attachments/assets/6c223158-8ff4-4e1a-9174-677e2daac9f0)

</p>
<p>
Select Add.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 085435](https://github.com/user-attachments/assets/64ab89ce-f9ae-4426-9677-688030c4dc57)

</p>
<p>
To pick the object names, enter domain users. Then, click Check Names and click OK.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 085449](https://github.com/user-attachments/assets/8dc01209-16d4-4235-baec-f32b8f314120)

</p>
<p>
Click on add and click OK
</p>
<br />

<p>
  
![Screenshot 2025-03-10 085932](https://github.com/user-attachments/assets/049cb249-ef48-435f-a6ca-f47c4941e981)

</p>
<p>
Return to Azure, copy the dc-1 IP address from the virtual machines section, paste it into Remote Desktop, and select Connect.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 090159](https://github.com/user-attachments/assets/8d434db9-2bda-47b3-8eb6-11a667221ecc)

</p>
<p>
Look for Windows Powershell ISE in DC-1, then right-click and select "Run as administrator."
</p>
<br />

<p>
  
![Screenshot 2025-03-10 090222](https://github.com/user-attachments/assets/e8b8b49e-e380-4a71-a641-67b656e87d21)

</p>
<p>
Select Yes.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 090303](https://github.com/user-attachments/assets/b5bac640-3ee0-4980-93c5-3a9b5ab4a053)

</p>
<p>
In Windows Powershell ISE, click on the arrow drop down next to script.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 113203](https://github.com/user-attachments/assets/34eedc29-d62c-4adb-8a05-17ed66d3fe7b)

</p>
<p>
Ten thousand random users with the password Password1 will be created by the script I used.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 113335](https://github.com/user-attachments/assets/a8a35040-a64d-4600-9dd4-2b47a0d376d4)

</p>
<p>
Click on Run Script.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 113344](https://github.com/user-attachments/assets/84e4e385-1939-442b-a7b9-3b01b77e0b36)

</p>
<p>
The script is being run successfully.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 113632](https://github.com/user-attachments/assets/eee1f197-0ff7-4e03-b3bf-4f63d703c88e)

</p>
<p>
Search for Active Directory Users and Computers.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 113704](https://github.com/user-attachments/assets/c8a64b0c-1025-4a2c-be4d-749309b66652)

</p>
<p>
The new users were retrieved.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 113717](https://github.com/user-attachments/assets/5d01e145-381d-49dd-a190-d3f042c45063)

</p>
<p>
Right-click on the _EMPLOYEES organizational unit and select refresh.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 113909](https://github.com/user-attachments/assets/c8f0eb65-b1e6-40a2-a151-14c56e6fc514)

</p>
<p>
Click on the start menu and sign out.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 113950](https://github.com/user-attachments/assets/59d6f5ac-6cf8-4baa-a27a-da395a2c43db)

</p>
<p>
Go back to Azure, copy client-1's IP address, put it into Remote Desktop, and select Connect.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 115514](https://github.com/user-attachments/assets/6efa1f16-93d2-4048-a87f-1d588b523318)

</p>
<p>
I choose a random user that was created using the script to see if I can log in successfully.
</p>
<br />

<p>

![Screenshot 2025-03-10 115523](https://github.com/user-attachments/assets/03eac12a-c1ce-4ea3-a8e8-6c2e13972887)

</p>
<p>
Select Yes.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 115805](https://github.com/user-attachments/assets/a397c31d-21fe-40b6-8e43-60c81b980672)

</p>
<p>
Once I have successfully logged in as lil.jof, I opened upcommand prompt to verify.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 115848](https://github.com/user-attachments/assets/441841b2-36b3-4998-a027-c46172af9cf6)

</p>
<p>
Open file explorer, click on this pc, click on the C drive and go to the Users folder.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 115946](https://github.com/user-attachments/assets/de48fd0a-1d0e-4146-abe2-df9517e79392)

</p>
<p>
Because lil.jof isn't an admin, he cannot access the labuser folder.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 120211](https://github.com/user-attachments/assets/eac461a5-711a-4591-bc27-eaebb3c5e708)

</p>
<p>
To conclude this lab,go to Azure and in the virtual machines section select both vms and stop them by selecting the three dots on the top right.
</p>
<br />

<p>
  
![Screenshot 2025-03-10 120216](https://github.com/user-attachments/assets/1a30e6a4-f769-4947-b35d-15204db8e579)

</p>
<p>
Select Yes.
</p>
<br />
