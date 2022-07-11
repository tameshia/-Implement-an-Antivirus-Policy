
<h1>Implement an Antivirus Policy</h1>

<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b> 

<h2>Environments Used</h2>

- <b>Windows 2019 (admin account)</b> 
- <b>Active Directory domain controller</b> 


<h2>Lab Description</h2>
  <p>In this lab, I will implement an antivirus policy. An antivirus policy determines which controls will be used to combat viruses and malware. It sets rules for which settings users can adjust from the default antivirus settings and whether controls are required on each device. </p>
  
  <p>A basic antivirus policy may look something like this:
    <ol>
       <li>Approved 3rd-party antivirus/antimalware solutions are allowed, but only in addition to the use of Microsoft Defender.</li>
       <li>Settings for the virus protection software must not be altered in a manner that will reduce the software effectiveness</li>
       <li>Virus protection software must not be disabled or bypassed</li>
       <li>End users are aware of the security policies enforced on their workstations</li>
    </ol>
    </hr>
<p>This lab will use Windows Defender Antivirus (also known as Windows Security) to implement an antivirus policy. Windows Defender Antivirus is a full-scale anti-malware sofware solution that can protect computers and devices from viruses, spyware, trojans, bots and many other types of malware. 
  <h2>Directions</h2>
    <p>Log into your machine as the administrator. From the <b>Windows Start</b> icon, click on the <b>Settings</b> button.</p>
    
![windows settings](https://user-images.githubusercontent.com/107451613/178303658-171cfec8-b55f-4378-add5-e7448a08997d.png)

<hr>

 <p>Type <b>Virus</b> in the Search field, the select <b>Virus & threat protection</b></p>

![virus](https://user-images.githubusercontent.com/107451613/178304082-9ea6a2ab-5051-413b-9753-01b850eb4dc2.png)

<hr>

<p>This will open up the Virus & threat protection setting page. Clink <b>Manage settings</b> link.<</p>

![Virus settings](https://user-images.githubusercontent.com/107451613/178304651-19354084-c36d-4f4a-8075-84be4dedbc49.png)

<hr>

<p>Scroll down to the <b>Tamper Protection</b> settings and click the button to turn on tamper protection. This prevents others from making adjustments to virus and threat protection settings. <p>

![TampProtect](https://user-images.githubusercontent.com/107451613/178309980-b91b74a4-6e8e-4366-b49a-c8edfcbd4529.PNG)
  
If a user attempts to turn off <b>Real-time, Cloud delivered, and Tamper Protection</b>, they will be unable to do so. We (the administrator) have set up a policy that prevents any changes to these settings. Local management only allows administrators to change settings for that particular workstation. These changes will not be implemented across the entire organization. Using Advance Directory makes it easy to change settings once and these changes will be deployed to several computers automatically. The next steps will show how to use the Group Policy Management Console to manage Windows Defender settings centrally from the domain controller. </p>

<hr>

<p>Login to Windows Server account. From the taskbar click the <b>Windows Start</b> icon, then click the <b>Server Manager button</b> to open the Server Manager application.<p>

![Server](https://user-images.githubusercontent.com/107451613/178322369-0a93d98d-8eed-4c31-a98d-50abdf27c522.PNG)
  
<hr>
  
<p>From the Server Manager menu bar, select <b>Tools > Group Policy Management</b></p>

![GPM](https://user-images.githubusercontent.com/107451613/178326022-49902a75-444d-4866-81dc-49d0e55ea97f.PNG)

<hr>
<p>Locate the Group Policy Management Console in the left pane. From here, navigate to <b><Forest > Domains > Group Policy Objects > Default Domain Policy</b> to open the Default Domain Policy.</p>

![Default Domain Policy](https://user-images.githubusercontent.com/107451613/178328663-0db95780-d75c-42f7-bbbd-341e19ebd2f8.png)

<hr>

<p>Right click <b>Default Domain Policy</b> and select <b>Edit</b> to open the Group Policy Management Editor. 
  
 ![GPO editor](https://user-images.githubusercontent.com/107451613/178329398-e33dcb1a-1cfe-47e7-8163-9d33bf8f382d.png)
  
 <hr>

<p>Navigate to <b>Computer Configuration > Policies > Administrative Templates: Policy definitions (ADMX files) retrieved from the local computer > Windows Defender Antivirus > Real-time protection</b>to Real-time protection settings. 
  
![Realtimeprotection](https://user-images.githubusercontent.com/107451613/178332368-0bc9234e-015c-482d-8682-befbbfeae4c6.png)
  
 <hr>
 
<p>In the right pane, locate and double-click<b> Turn off real-time protection</b>

  
![turn off real time pro](https://user-images.githubusercontent.com/107451613/178333146-173ed2c5-170f-422e-a9c2-aa313b1dfaef.png)
  
 <p>In this setting, you can enforce the AD (Active Directory) to remember old passwords, up to the number specified, and prevent users from re-using old passwords.
 
<hr>
