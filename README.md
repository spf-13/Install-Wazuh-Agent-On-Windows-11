# Install Wazuh Agent on Windows 11

**Hardware:** MacBook M4  
**Software:** UTM  
**Goal:** Install the Wazuh Agent on Windows 11 and monitor it through the Wazuh Dashboard.  

## Step-by-Step Installation Guide

### 1. Download Wazuh Agent
- Download link: https://packages.wazuh.com/4.x/windows/wazuh-agent-4.14.4-1.msi  
- Alternative: [Wazuh Agent for Windows documentation](https://documentation.wazuh.com/current/installation-guide/wazuh-agent/wazuh-agent-package-windows.html)

### 2. Install Wazuh Agent
- Go to your **Downloads** folder
- Run `wazuh-agent-4.14.4-1.msi`
- Accept the License Agreement
- Click **Install**
- Check the box **"Run Agent configuration interface"** and **Finish**

### 3. Configure Wazuh Agent
- In the Agent configuration window, enter the **Manager IP** (IP address of your Wazuh Server)
- Click **Save**
- Open Windows PowerShell as Administrator
- Run
```
net start wazuh
```

### 4. Verify in Wazuh Dashboard
- Open the Wazuh Dashboard
- Login
- Go to ```Agents management``` -> ```Summary```
- Your Windows 11 agent should now appear. Congratulations!

Useful COMMANDS
### Start/stop services
```
sudo systemctl start wazuh-indexer
```
```
sudo systemctl stop wazuh-indexer
```
```
sudo systemctl start wazuh-manager
```
```
sudo systemctl stop wazuh-manager
```
```
sudo systemctl start wazuh-dashboard
```
```
sudo systemctl stop wazuh-dashboard
```
### Start / Stop Wazuh Agent service (Windows PowerShell)
```
net stop wazuh
```
```
net start wazuh
```
### List connected agents
```
sudo /var/ossec/bin/agent_control -l
```
### List all agents
```
sudo /var/ossec/bin/manage_agents -l
```
### # Extract key for agent ID 001
```
sudo /var/ossec/bin/manage_agents -e 001
```

## Screenshots
<img width="1278" height="837" alt="Screenshot 2026-04-05 at 11 29 26 AM" src="https://github.com/user-attachments/assets/d49ea2e0-cffd-4e95-9740-84023fd88e73" />
<img width="1126" height="633" alt="Screenshot 2026-04-05 at 11 38 29 AM" src="https://github.com/user-attachments/assets/5807b07b-55e3-49d9-a85e-764b5bdc430b" />
<img width="496" height="393" alt="Screenshot 2026-04-05 at 11 38 40 AM" src="https://github.com/user-attachments/assets/06a7a054-a10e-4ffa-b4f5-52555056e2d2" />
<img width="494" height="393" alt="Screenshot 2026-04-05 at 11 38 49 AM" src="https://github.com/user-attachments/assets/66540a18-bed5-4d50-ab40-7a08c47d8ac3" />
<img width="319" height="280" alt="Screenshot 2026-04-05 at 11 39 07 AM" src="https://github.com/user-attachments/assets/e7e2dc38-7997-4aed-9b40-0e9743b02de7" />
<img width="1028" height="619" alt="Screenshot 2026-04-05 at 11 41 58 AM" src="https://github.com/user-attachments/assets/998365a1-2ab8-460b-bd5c-f06511d7a084" />
<img width="322" height="285" alt="Screenshot 2026-04-05 at 11 42 21 AM" src="https://github.com/user-attachments/assets/4ed4c7dd-4f2b-4645-ae14-e8098ef88150" />
<img width="1279" height="841" alt="Screenshot 2026-04-05 at 11 29 13 AM" src="https://github.com/user-attachments/assets/53fdbdd3-4441-45da-a97b-5513834c4d87" />
<img width="1276" height="841" alt="Screenshot 2026-04-05 at 11 42 43 AM" src="https://github.com/user-attachments/assets/59813a14-bbbc-4165-8298-064ee22c2fad" />
<img width="1277" height="838" alt="Screenshot 2026-04-05 at 11 42 55 AM" src="https://github.com/user-attachments/assets/08c318eb-2d2c-4607-a6f5-bb6e8ed9e79f" />
<img width="1634" height="737" alt="Screenshot 2026-04-05 at 11 43 50 AM" src="https://github.com/user-attachments/assets/aa31a800-f95c-4154-a2f4-1358956552cc" />
<img width="815" height="580" alt="Screenshot 2026-04-05 at 11 50 54 AM" src="https://github.com/user-attachments/assets/178c4f1f-f7a4-41d2-bccc-da8b675554c0" />



## Useful for
- Wazuh Agent deployment
- Monitoring endpoints
- Portfolio project 

This repo shows how I install Wazuh Agent on Windows 11 endpoint.
