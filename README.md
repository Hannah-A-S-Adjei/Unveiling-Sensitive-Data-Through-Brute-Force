<h1>Brute Force</h1>
A brute force attack is a method used by hackers to gain unauthorized access to a system or account by systematically trying every possible combination of usernames and passwords until the correct one is found. This technique relies on the sheer computational power to crack passwords, making it one of the oldest and simplest forms of cyber attack. Despite its straightforward approach, brute force attacks can be highly effective if proper security measures such as strong passwords and account lockout policies are not in place. These attacks pose a significant cybersecurity threat, emphasizing the importance of implementing robust defense mechanisms to safeguard sensitive information and systems.
<br />



<h2>Requirements</h2>


- Target Machine(VM1)</b> 
- Kali Linux(VM2)</b>
- NMAP Software</b>
- Hydra Software</b>
- VMware</b>

<h2>Steps</h2>
Through social engineering, Beate Dietrich, an individual employed by an organization, had her information gathered. Subsequently, the account information belonging to Beate Dietrich was obtained using brute force with the password cracking tool named "HYDRA," as illustrated in the figure below. The command utilized "-L" to indicate the directory of the username. However, the command was executed within the directory where both the username and password were stored as such the directory was not specified. The "-f" command instructed Hydra to cease attempts once a successful login occurred. In other words, upon successful login, further password trials were unnecessary.

<p align="center">
Credential for Ms. Beate:  <br/>
<img src="https://imgur.com/Oxu5oHm.png" height="80%" width="80%" alt="Disk Sanitization 
 Steps"/>
<br />
<br />
 
After acquiring the account credentials for Ms. Beate, namely the username "bdietrich" and password "my2kids," highlighted in light green in Figure above, a successful remote login from Kali using SSH was initiated, as demonstrated in the figure below."

<p align="center">
Remote LogIn:  <br/>
<img src="https://imgur.com/CEsZ9kv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br /> 
 
Upon logging into the Mars VM remotely from the Kali machine with the account of "bdietrich," the command "ls -la" was employed to display all files, including hidden ones. 

<p align="center">
Files in Finance Directory: <br/>
<img src="https://imgur.com/kCY3PWL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 
Subsequently, the data was exfiltrated from the target machine onto Kali using the secure copy protocol (SCP), and the files were opened successfully revealing the account information as well as the passwords as illustrated in the figure below. 

<p align="center">
Files in Finance Directory: <br/>
<img src="https://imgur.com/M47dVLB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 
The figure below shows the company's online banking account information (account details and credentials) stored in a file “bank.xls”.

<p align="center">
Files in Finance Directory: <br/>
<img src="https://imgur.com/hf2NZn1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

<h2>Key Takeaways </h2>

A proficient security analyst should possess a thorough comprehension of system vulnerabilities, especially concerning authentication mechanisms. Through methodical evaluation of password strength, deficiencies such as insufficient policies and login vulnerabilities can be discerned. The acquired insights play a crucial role in informing security enhancements such as the implementation of more robust password policies and the deployment of system hardening to effectively mitigate brute force attacks.
