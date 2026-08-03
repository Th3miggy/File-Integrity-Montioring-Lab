# File-Integrity-Montioring-Lab

## Objective

In this lab, our goal is to set up a SIEM on our Ubuntu machine, add our Windows machine as an endpoint, configure file integrity monitoring on the endpoint, and finally test the monitoring by creating and deleting files to see if they generate event logs in our Wazuh Dashboard.

### Skills Learned

* Advanced understanding of SIEM concepts and practical application.
* Proficient in SIEM setup for controls and endpoints.
* Better understanding of File integrity monitoring applications.

### Tools Used

* Security Information and Event Management (SIEM) system, namely Wazuh and an open-source SIEM.
* Notepad or other text editor to note which directory we want to monitor.
* A Linux Ubuntu machine to act as our manager and a Windows device to be our endpoint.

## Steps
Below will be steps and images to document the process of completing this lab.

Ref 1: The first step in the lab is to confirm the IP addresses on our Ubuntu machine and Windows machines, as they will both be needed in the setup of the SIEM. We can do this by using ifconfig on our Ubuntu machine and ipconfig on our Windows machine.

![not-working](https://github.com/Th3miggy/File-Integrity-Montioring-Lab/blob/main/Screenshot%20from%202026-07-26%2022-11-27.png?raw=true)

Ref 2: Next, we will head to Wazuh and find the manager installer for Ubuntu and run that script.

![not-working](https://github.com/Th3miggy/File-Integrity-Montioring-Lab/blob/main/Screenshot%20from%202026-07-26%2015-25-53.png?raw=true)

![not-working](https://github.com/Th3miggy/File-Integrity-Montioring-Lab/blob/main/Screenshot%20from%202026-07-26%2016-40-01.png?raw=true)

 Ref 3: After the install of the manager is done, we are given a username and password to log in to our dashboard. Using the IP address of our Ubuntu machine, we can log in to our dashboard.

 ![not-working](https://github.com/Th3miggy/File-Integrity-Montioring-Lab/blob/main/ChatGPT%20Image%20Jul%2026,%202026,%2010_24_23%20PM.png?raw=true)

Ref 4: The next step we will go the deploy new agents tab and fill out the information with our manager IP address and agent name. This will create a command for us to run on our Windows machine.

![not-working](https://github.com/Th3miggy/File-Integrity-Montioring-Lab/blob/main/Screenshot%20from%202026-07-26%2022-34-06.png?raw=true)

Ref 5:  It is important to note that for running the command on your Windows device, it must be run as admin and in a Windows PowerShell prompt

![not-working](https://github.com/Th3miggy/File-Integrity-Montioring-Lab/blob/main/Screenshot%202026-07-26%20173828.png?raw=true)

Ref 6: Once the script has been completed and the Wazuh agent has been installed, we can return to our Ubuntu device and check the manager to make sure we can see the device under agents

![not-working](https://github.com/Th3miggy/File-Integrity-Montioring-Lab/blob/main/Screenshot%20from%202026-07-26%2017-42-39.png?raw=true)

Ref 7: Now that the agent is installed and we can manage the device from our Ubuntu machine, we have access to several powerful tools that we will dive into on a later project; for now we are going to focus on the file integrity monitoring tools. First, we will return to our Windows machine and edit the ossec.conf in a text editor (such as Notepad) to add the directory we want to monitor to the file integrity monitor section of the file. In this case, the directory we are monitoring is C:/downloads/test/

![not-working](https://github.com/Th3miggy/File-Integrity-Montioring-Lab/blob/main/Screenshot%202026-07-26%20224557.png?raw=true)

Ref 8,9,10: adding this text to the .conf file will now create a log when files are added, deleted, or moved in the directory. For instance, if we add a Test.txt, it will create an event log in our Wazuh manager; additionally, it will create another log if the Test.txt file is deleted.

![not-working](https://github.com/Th3miggy/File-Integrity-Montioring-Lab/blob/main/Screenshot%202026-07-26%20175543.png?raw=true)

![not-working](https://github.com/Th3miggy/File-Integrity-Montioring-Lab/blob/main/Screenshot%20from%202026-07-26%2017-55-21.png?raw=true)

![not-working](https://github.com/Th3miggy/File-Integrity-Montioring-Lab/blob/main/Screenshot%20from%202026-07-26%2017-57-02.png?raw=true)

this conludes our Lab!

