<h1>Challenge Lab C: Log File Archiving</h1>

<h2>Description</h2>
** This lab is modeled after Challenge Lab C within the 'Linux Essentials' course from the Network Development Group (NDG). **

The purpose of this lab is to demonstrate proficiency of navigating the Linux filesystem, creating and modifying directories, and archiving information (specifically, log files in this scenario). In this lab, we are tasked with preserving a specific set of log files on the system in order to investigate some potentially suspicious activity that may have occurred. In the documented steps below, I proceed to create the new directories of 'archive' and 'backup' in order to store the necessary log info, use proper command syntax in order to gather the necessary log info and create a new archive file named 'log.tar', and lastly, extract the contents of 'log.tar' into the 'backup' directory which allows for the log info to be safely preserved for further analysis.
<br />


<h2>Key Points Within Lab: </h2>

- <b>Creation of 'archive' and 'backup' directories for proper file collection and storage.</b>
- <b>Creation of 'log.tar' file archive to be stored within the 'archive' directory located inside of /home/user/.</b>
- <b>Utilization of verbose output in order to track which files are being archived.</b>
- <b>Proper tag utilization to list 'archive' contents without extraction.</b>
- <b>Extraction of files to 'backup' directory for log preservation.</b>


<h2>Lab walk-through:</h2>

<p align="center">
In the image below, we are initially located within the /var/log directory since our goal is to view and eventually copy all log files that end in '.log'. With the command "ls *.log" we are able to see the scope of the log files which we will be archiving in the near future. Next, we switch back to our home directory in order to properly create and store the 'archive' and 'backup' directories.<br/>
<img src="https://i.imgur.com/BEFhvS2.png" height="80%" width="80%" alt="AD Home Lab"/>
<br />
<br />

<p align="center">
After creating the 'archive' and 'backup' directories inside of /home/, we are now back in /var/log/. With the command "tar -cvf ~/archive/log.tar *.log", I am able to successfully create a new file named 'log.tar' which will be housed in the 'archive' directory and it will contain all log files which end in '.log'. (I would like to note that sudo is employed in the screenshot in order to give me the necessary permissions to access the log files and write them to log.tar). Additionally, the -v tag of the former command provides a verbose output which showcases all of the log files that have been copied into the new log.tar file. However, we are still able to use the command "tar -tf ./archive/log.tar" in order to list the contents of 'log.tar' and ensure that all necessary files were archived accordingly.    <br/>
<img src="https://i.imgur.com/I5WX1Vs.png" height="80%" width="80%" alt="AD Home Lab"/>
<br />
<br />

<p align="center">
Finally, we switch into the 'backup' directory which was created earlier. Using the command "tar -xvf ~/archive/log.tar" we extract the contents of the log.tar file into the 'backup' directory. Using 'ls' we are able to check the 'backup' directory and see that everything which was contained in log.tar is now also stored in 'backup'. From here, the log files will be safely preserved until further notice which will allow us to examine them for any information that may need to be investigated further.  <br/>
<img src="https://i.imgur.com/E9V1kcS.png" height="80%" width="80%" alt="AD Home Lab"/>
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
