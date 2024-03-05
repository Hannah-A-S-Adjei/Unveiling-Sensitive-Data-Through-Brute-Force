<h1> Brute Force</h1>

<h2>Description</h2>
A brute force attack is a method used by hackers to gain unauthorized access to a system or account by systematically trying every possible combination of usernames and passwords until the correct one is found. This technique relies on the sheer computational power to crack passwords, making it one of the oldest and simplest forms of cyber attack. Despite its straightforward approach, brute force attacks can be highly effective if proper security measures such as strong passwords and account lockout policies are not in place. These attacks pose a significant cybersecurity threat, emphasizing the importance of implementing robust defense mechanisms to safeguard sensitive information and systems.
<br />

<h2>Requirements</h2>
Virtual machines (Target and Victim)
Hydra Software



<h2>Steps</h2>
Through social engineering, Beate Dietrich, an individual employed by an organization, had her information gathered. Subsequently, the account information belonging to Beate Dietrich was obtained using brute force with the password cracking tool named "HYDRA," as illustrated in the figure below. The command utilized "-L" to indicate the directory of the username. However, the command was executed within the directory where both the username and password were stored as such the directory was not specified. The "-f" command instructed Hydra to cease attempts once a successful login occurred. In other words, upon successful login, further password trials were unnecessary.


<p align="center">
Scan Target Machine:  <br/>
<img src="https://imgur.com/TsNDJK2.png" height="80%" width="80%" alt="Disk Sanitization 
 Steps"/>
<br />
<br />
 
After acquiring the account credentials for Ms. Beate, namely the username "bdietrich" and password "my2kids," highlighted in light green in Figure 7 above, a successful remote login from Kali using SSH was initiated, as demonstrated in the figure below."

<p align="center">
MSFCONSOLE Launch:  <br/>
<img src="https://imgur.com/2opHAxu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br /> 
 
Upon logging into the Mars VM remotely from the Kali machine with the account of "bdietrich," the command "ls -la" was employed to display all files, including hidden ones. Subsequently, these files were copied from Mars onto Kali, as illustrated in the subsequent figure. Following the download, the files were opened in Kali, successfully revealing the account information as well as the passwords as shown below.

<p align="center">
Exploit Directory: <br/>
<img src="https://imgur.com/hQn3bTn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 
The figure below shows the company's online banking account information (account details and credentials) stored in a file “bank.xls”.

<h2>Key Takeaways: </h2>

A proficient security analyst should possess a thorough comprehension of system vulnerabilities, especially concerning authentication mechanisms. Through methodical evaluation of password strength, deficiencies such as insufficient policies and login vulnerabilities can be discerned. The acquired insights play a crucial role in informing security enhancements such as the implementation of more robust password policies and the deployment of system hardening to effectively mitigate brute force attacks.

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>

