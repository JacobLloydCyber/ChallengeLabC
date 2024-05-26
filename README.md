<h1>Challenge Lab C: Log File Archiving</h1>

<h2>Description</h2>
** This lab reflects Challenge Lab C in the 'Linux Essentials' course from the Network Development Group. **

The purpose of this lab is to demonstrate proficiency while navigating the Linux filesystem, creating directories for information storage, and transferring log files to alternate locations to help ensure data preservation. This lab states that suspicious activity has been detected on the system, therefore, we must archive and preserve a specific set of log files so that they may be further analyzed. In this lab we are tasked with the following steps:

- Gather all files in /var/log that end with the '.log' extension, and send these files to a new archive named "log.tar".
- When archiving the log files, utilize tags to help showcase that the correct information was collected.
- Extract the collected log files to a separate and tamper-free backup directory where the information can be safely analyzed.


<h2>Key Points Within Lab: </h2>

- <b>Demonstrate ability to create directories within a Linux server.</b>
- <b>Demonstrate ability to use 'tar' to archive info to a new file and extract the collected info to a new directory.</b>
- <b>Demonstrate correct tag usage with 'tar' to produce verbose output, list file contents, and perform extraction.</b>


<h2>Lab walk-through:</h2>

<p align="center">
In the image below, I am located within the /var/log directory. By issuing the command "ls *.log" I am able to see the scope of the log files which I will be archiving in the near future. Before I collect any information, I must first create the directories in which I will archive and extract the log files to. So, after switching back into my /home directory, I am able to use the 'mkdir' command to create two new directories which I have called "archive" and "backup".<br/>
<img src="https://i.imgur.com/BEFhvS2.png" height="80%" width="80%" alt="LinChallLab"/>
<br />
<br />

<p align="center">
With the "archive" and "backup" directories created, I can now switch back into /var/log and begin collecting the necessary info. By issuing the command "tar -cvf ~/archive/log.tar *.log", I am able to create a new archive file named "log.tar". This new file will be stored in the "archive" directory and it will contain all log files from /var/log which end in ".log". I would like to note that the -v tag included in the previous tar command provides a verbose output which allows me to see all of the log files that were collected and copied to create log.tar. Additionally, the command "tar -tf ./archive/log.tar", allows me to check the contents of log.tar in order to confirm that all necessary files were archived accordingly.    <br/>
<img src="https://i.imgur.com/I5WX1Vs.png" height="80%" width="80%" alt="LinChallLab"/>
<br />
<br />

<p align="center">
With the necessary log files archived, I can finally switch into the "backup" directory to perform data extraction. By running the command "tar -xvf ~/archive/log.tar" I am able to extract the contents of the log.tar file into the "backup" directory. Now, by listing the directory contents, I am able to confirm that all the data which was archived in log.tar is now also stored in the "backup" directory. At this point, the log files will be safely preserved until further notice, allowing them to be examined for any information that may need to be investigated further.  <br/>
<img src="https://i.imgur.com/E9V1kcS.png" height="80%" width="80%" alt="LinChallLab"/>
<br />
<br />



<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
