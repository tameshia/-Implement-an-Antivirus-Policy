
<h1>Implement an Antivirus Policy</h1>

<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b> 

<h2>Environments Used </h2>

- <b>Windows 2019 (admin account)</b> 


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
  
If a user attempts to turn off <b>real-time, cloud delivered, and tamper protection</b>, they will be unable to do so. We (the administrator) have set up a policy that prevents any changes to these settings. Local management only allows administrators to change settings for that particular workstation. These changes will not be implemented across the entire organization. Using Advance Directory makes it easy to change settings once and these changes will be deployed to several computers automatically. The next steps will show how to use the Group Policy Management Console to manage Windows Defender settings centrally from the domain controller. </p>

<hr>
