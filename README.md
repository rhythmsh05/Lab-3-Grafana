# Lab-3-Grafana

## Lab: Grafana Installation and Dashboard Creation on Ubuntu Server

### Lab Objective

This report details the Azure Monitor agent setup, Grafana installation on an Ubuntu server, and dashboard development for performance metrics visualization.

###  Steps Covered

## Task 1: Prepare the Ubuntu Server

```bash
sudo apt-get update && sudo apt-get upgrade -y
```
## Task 2: Install Grafana

###  Start and Enable Grafana

```bash
sudo systemctl daemon-reload
sudo systemctl start grafana-server
sudo systemctl enable grafana-server
```
![image](https://github.com/user-attachments/assets/4f574e47-30c0-4e80-bff7-0ae4f18c5d9a)

## Task 3: Connect Grafana to Azure Monitor with Inbound Security Rules

*Add Inbound Security Rule*

![image](https://github.com/user-attachments/assets/0069bb0d-b07d-4c24-969c-b97375f1f955)

*Connect Grafana to Azure Monitor*

![Screenshot (356)](https://github.com/user-attachments/assets/888b492a-2a14-4628-85c9-0b79ea0a94a8)

## Task 4: Configure Grafana for Azure Monitor
- Enabled System Assigned Managed Identity on the Azure VM.
- Assigned roles in Azure:
   - Monitoring Reader on Azure Monitor
   - Reader on the Subscription

![Screenshot (357)](https://github.com/user-attachments/assets/a213ea29-06ab-4123-989e-357845e865e0)

## Task 5: Create Grafana Dashboard

- Created a new dashboard.
- Select Azure Monitor as the data source.
- Added a panel to visualize Percentage CPU:
  - Data Source: Azure Monitor
  - Metric Namespace: microsoft.compute/virtualmachines
  - Aggregation: Average

![Screenshot (363)](https://github.com/user-attachments/assets/e46dc5e8-5bc9-4687-8362-527660b95103)

### Final Dashboard Overview
![Screenshot (364)](https://github.com/user-attachments/assets/f7fb1109-84d1-4231-9b3e-ea5b73e4b634)





