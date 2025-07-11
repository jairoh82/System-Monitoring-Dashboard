# System Monitoring Dashboard
Allows to monitor real time dashboared for following: CPU,RAM,disk,network, and your running processes


## Objective
To set up a real time system monitoring dashboard on Linux machine that provides visibility into system performance, resource usage, and running services. This will demonstrate the ability to monitor and maintain system health.

### Introduction
This project sets up a real time monitoring dashboard on a Linux VM to track CPU, memory, disk, and network usage. Using Netdata, I’m going to build a visual dashboard to help identify performance issues and monitor system health this will demonstrate core IT support and system admin skills.

### The tools I will use include:

- Netdata: Real time system monitoring tool provides detail insight

- Ubuntu: Operating System


## Steps and Results

*1: Setting Up the Environment*

To  begin, Ubuntu will need to install Netdata to do this. You will need to enter into your bash this will be your terminal on ubuntu. Once in the bash you will need to enter the following command  sudo apt update and sudo apt install netdata -y this is our tool that we are going to be using to monitor real time dashboards.

![step 1](https://github.com/user-attachments/assets/1b4b8d07-4c8a-46f4-8488-075c61d2d613)


*2: Starting Netdata*

We are going to start Netdata by using the next 2 commands sudo systemctl start netdata and sudo systemctl enable netdata. Once you have netdata install now we enter the browser and enter http://localhost:19999 this will give you the dashboard where you will be able to see CPU,RAM,disk,network, and your running processes. But let’s not forget we will also see System alerts, charts, and health status.

![step 2](https://github.com/user-attachments/assets/3b0ee35c-711c-4ed3-b999-8f663bb770b7)

![Step 3](https://github.com/user-attachments/assets/d308153e-4ef9-4d53-a29f-517f5a437cab)

![Step 4](https://github.com/user-attachments/assets/41f423df-84d1-41b2-ac12-b21653cbd7d4)


### Conclusion

