<h1>Active Directory</h1>



<h2>Description</h2>
In this project i wanted to RDP into a traget PC using a kali linus brute force tool called crowbar and see the activity it generates in splunk, to complete this lab i need to create a splunk server and a windows server, i also had tp set up a target PC and and an attacker PC. i weas able to RDP into the target PC but i was able to use Atomic Red Team to generte some activity in splunk.
Project was created in virtual Box and consists of a windows server (used to monitor and create user perfile), splunk server (used to moniter trafic and collect network telemetry) windows target PC (simulate users on the network) and kali linux ( Attacker cumputer)  
<br />


<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b> 
- <b>linux</b>

<h2>Environments Used </h2>

- <b>virtual box</b> (21H2)


<h2>Lab Diamgram:</h2>
<img src="https://i.imgur.com/jOKYZwU.png " height="80%" width="80%" alt="Disk Sanitization Steps"/>

<h2>Program walk-through:</h2>

<p align="center">
This image shows all the diffrent machinces set up and all set to NAT network: <br/>
<img src="https://i.imgur.com/54kZDKF.png="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Splunk server setup and with IP:  <br/>
<img src="https://i.imgur.com/AvTbI90.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Windows PC remaned to "target PC": <br/>
<img src="https://i.imgur.com/cOsM4Be.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Target PC IP set up:  <br/>
<img src="https://i.imgur.com/1x5P87Y.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Donload sysmon and set it up using powershell (may take some time):  <br/>
<img src="https://i.imgur.com/UOfMPD0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
remane windows server PC to "ADDC01 and change IP (may take some time):  <br/>
<img src="https://i.imgur.com/EhlxBDK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/eEnWg4N.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
endpoint file created and added to both Target and server PC splunk system files and then endpoint index created on splunk  (may take some time):  <br/>
<img src="https://i.imgur.com/WskOYYb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Kali linux IP set up:  <br/>
<img src="https://i.imgur.com/pwJikYg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
download and set brute force tool I used crowbar turn on RDP on target PC, unfortunatly i was unable to RDP into the target PC:  <br/>
<img src="https://i.imgur.com/nASeCW6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
download and set Atomic Red Team in powershell:  <br/>
<img src="https://i.imgur.com/89VuLLF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
run "add new user" test to generate telemetry in splunk :  <br/>
<img src="https://i.imgur.com/YANlsXt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
look at the splunk event logs to see the telemetry created by Atomic red Team:  <br/>
<img src="https://i.imgur.com/cJ1UVgr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
