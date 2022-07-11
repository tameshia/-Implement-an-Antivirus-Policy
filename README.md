
<h1>Implement an Antivirus Policy</h1>

<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b> 

<h2>Environments Used </h2>

- <b>Windows Server 2019</b> 


<h2>Lab Description</h2>
  <p>In this lab, I will implement a password protection policy. A password protection policy sets the rules and standards for password validity and management within an organization. A password policy can enforce and standardize password lenght, combinations, password attempts, implement a lock-out policy, determine the frequency in which passwords must be changed, enable multi-factor authentication, and set rules for password history and minimum age requirements.  </p>
  
  <p>A password policy may look something like this:
    <ol>
       <li>Passwords must be at least 9 characters in length and must contain 3 of the following: At least one upper case character, at least one numeric character, include at least one special character, [ e.g., ! @ # ? ] </li>
       <li>Users cannot use any of the previously used 10 passwords.</li>
       <li>Passwords must be changed every 90 days.</li>
       <li>User IDs and user names are not allowed</li>
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
