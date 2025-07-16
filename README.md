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

## Test Scenarios
*Simulation of High CPU Usage*

To this scenario if you haven’t already installed stress on your vm you will need to. To do this You would need to do into your terminal and do the following command after that you will use the rest of the commands to do this simulation of high CPU usages.

Sudo apt install stress

![test scenarios CPU 1](https://github.com/user-attachments/assets/433a4bff-9e69-479e-b1cb-2519b4c0ac5e)

Run 4 times Yes > /dev/null & 

![test scenarios CPU 2 4 runs](https://github.com/user-attachments/assets/179f6120-8cce-4b39-936c-ad78a5eda46b)


Graph Results

![test scenarios CPU 2 4 runs results](https://github.com/user-attachments/assets/0162d1e3-f5c4-4597-9760-85eba950bbb5)

TO TERMINATE RUN killall yes

![test scenarios CPU 2 4 run killall](https://github.com/user-attachments/assets/c5e0b6be-12a3-4438-b7a0-4ffa10e9e876)

*RAM*

To simulate RAM usage we are going to run 2 memory workers, each user at 1G for 30 seconds than it will stop.

--vm 2 : Run memory workers

--vm-bytes 1G: Each uses 1GB

--timeout 30: Runs for 30 seconds, then stops.

Command:

Stress -- vm 2  --vm-bytes 1G –timeout 30

![ram commandd](https://github.com/user-attachments/assets/efed6861-d3ca-4675-8fcc-8025c2e2c432)


RESULTS

<img width="997" height="741" alt="RAM Results" src="https://github.com/user-attachments/assets/50b963c4-ef18-407c-bc95-c81ce6311dc2" />

*Network*

Use ping -f to flood packets ( 2 times)

-f is flooding ping: sends as many as possible per second

Download a large File with wget

Wget http:ipv4.dowload.thinkbroadband.com/100mb.zip

<img width="1263" height="771" alt="network test command line" src="https://github.com/user-attachments/assets/c0b6f03f-9a9b-4e4f-9ce4-f920700897a2" />


RESULTS

<img width="1082" height="799" alt="network test results" src="https://github.com/user-attachments/assets/b8193c23-ae74-4a45-9923-ea61db6b34be" />



### Conclusion
This project shows how to proactively maintain system health, diagnose problems, and increase reliability using real-time monitoring technologies. I was able to mimic real-world IT support scenarios like high CPU load, memory strain, and network traffic spikes, as well as visualize performance indicators and customize alarms, by installing and testing Netdata on a Linux server. In production settings, this type of active system monitoring is crucial for locating bottlenecks and guaranteeing uptime.
