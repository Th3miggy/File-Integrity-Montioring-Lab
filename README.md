# File-Integrity-Montioring-Lab

## Objective

In this lab our goal is to establish a SIEM on our Ubuntu machine get our windows machine add as an endpoint and setup file integrity montioring on the endpoint and final test the montioring by creating and deleting files to see if they created event logs on our Wazuh Dashboard.

### Skills Learned

- Advanced understanding of SIEM concepts and practical application.
- Proficienet in SIEM setup as a control and a endpoint.
- Better understanding of File integrity montioring application.

### Tools Used

- Security Information and Event Management (SIEM) system namely Wazuh and Open source SIEM.
- Notpad or other text editor to note which directory we want to monitor.
- a Linux ubuntu machine to act as our manager and a windows device to be our endpoint.

## Steps
Below will be steps and images to document the process of completing this lab.

Ref 1: First step in the lab is to confirm the IP on our Ubuntu machine and windows machines as they will both be needed in the setup of the SIEM. we can do this by using ifconfig on our ubuntu machine and ipconfig on our windows machine.

![not-working](https://github.com/Th3miggy/File-Integrity-Montioring-Lab/blob/main/Screenshot%20from%202026-07-26%2022-11-27.png?raw=true)

Ref 2: Next we will head to the Wazuh and find the manager installer for ubuntu and run that script.

![not-working](https://github.com/Th3miggy/File-Integrity-Montioring-Lab/blob/main/Screenshot%20from%202026-07-26%2015-25-53.png?raw=true)

![not-working](https://github.com/Th3miggy/File-Integrity-Montioring-Lab/blob/main/Screenshot%20from%202026-07-26%2016-40-01.png?raw=true)

 Ref 3: After the install of the manager is done, we are give a usename and password for which to login to our dashboard. Using the Ip address of our ubuntu machine we can login to our dashboard.

 ![not-working](https://github.com/Th3miggy/File-Integrity-Montioring-Lab/blob/main/ChatGPT%20Image%20Jul%2026,%202026,%2010_24_23%20PM.png?raw=true)

Ref 4: The next step we will go the deploy new agents tab and fill out the information with our manager IP address and agent name. This will created a command for us to run on our windows machine.

![not-working](https://github.com/Th3miggy/File-Integrity-Montioring-Lab/blob/main/Screenshot%20from%202026-07-26%2022-34-06.png?raw=true)

Ref 5: It is important to note that for running the command on your windows device it must be ran as admin and a windows powershell prompt

![not-working](https://github.com/Th3miggy/File-Integrity-Montioring-Lab/blob/main/Screenshot%202026-07-26%20173828.png?raw=true)

Ref 6: Once the script has been completed and the Wazuh agent has been installed we can return to our ubuntu device and check the manager to make sure we can see the device under agents

![not-working](https://github.com/Th3miggy/File-Integrity-Montioring-Lab/blob/main/Screenshot%20from%202026-07-26%2017-42-39.png?raw=true)

Ref 7: Now that the agent is install and we can manager the device from our ubuntu machine we have access to several powerful tools that we will dive into on a later project for now we are going to focus on the file integrity montioring tools. first we will return to our windows machine and edit the ossec.conf in a text editor (such as notpad) to add the directory we want to montior to the file integrity montior section of the file. in this case the directory we are montioring is C:/downloads/test/ 

![not-working](

