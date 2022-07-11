
<h1>Implement an Antivirus Policy</h1>

<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b> 

<h2>Environments Used </h2>

- <b>Windows Server 2019</b> 


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

  <h2>Directions</h2>
    <p>From the <b>Windows Start</b> icon, click on the <b>Server Manager</b> button. This will open the Server Manager application.</p>
    
![WinSer](https://user-images.githubusercontent.com/107451613/176472227-241244e8-da20-4378-9780-5e9296010dd3.png)

<hr>

 <p>From the Server Manger menu bar, select <b>Tools > Group Policy Management</b> to open the Group Policy Management Console.</p>

![GropPolicyMgmt](https://user-images.githubusercontent.com/107451613/176472656-153ee581-c17e-45ca-b731-a442870ed249.png)

<hr>

<p>In the left pane of the Group Policy Management Console, expand <b>Group Policy Objects</b> and navigate to <b>Default Domain Policy</b> and right click to select the <b>Edit</b> option.</p>

![Default Domain Policy](https://user-images.githubusercontent.com/107451613/176473831-32e84d07-9ccf-423e-b22e-16002f61bb02.png)

<hr>
