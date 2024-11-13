# Over view

## Background Information

### IT Block Setup
| Location                          | Number of Desktops |
|-----------------------------------|---------------------|
| Director Office                   | 2                  |
| Network Manager Room              | 1                  |
| Technical Officers’ Room          | 2                  |
| Staff Office                      | 5                  |
| Meeting Room                      | 2                  |
| Computer Lab 1                    | 60                 |
| Computer Lab 2                    | 60                 |
| Digital Learning and Media Centre | 30                 |
| Printers                          | 3                  |
| Wi-Fi                             | 2                  |

### Department Block Setup
| Location                                | Number of Desktops |
|-----------------------------------------|---------------------|
| 4 Lecture Halls                         | 4                  |
| 14 Staff Rooms                          | 14                 |
| 4 Technical Officers Rooms              | 4                  |
| Department Meeting Room                 | 2                  |
| Computer Lab 1                          | 50                 |
| Computer Lab 2                          | 50                 |
| Network Engineering Lab                 | 10                 |
| Microprocessor Lab                      | 12                 |
| Computer Vision and Machine Learning Lab| 50                 |
| Department Office                       | 2                  |
| Wi-Fi                                   | 1                  |
| Printer                                 | 1                  |

---

## VLAN Configuration


| VLAN Name                                | Needed Size | VLAN No | Allocated Size | Subnet Mask       | Network Address | Assignable Range              | Broadcast ID     |
|------------------------------------------|-------------|---------|----------------|--------------------|-----------------|--------------------------------|------------------|
| Computer Lab 1 (IT Block)                | 60          | 1       | 62             | 255.255.255.192   | 10.20.0.0       | 10.20.0.1 - 10.20.0.62         | 10.20.0.63       |
| Computer Lab 2 (IT Block)                | 60          | 2       | 62             | 255.255.255.192   | 10.20.0.64      | 10.20.0.65 - 10.20.0.126       | 10.20.0.127      |
| Computer Lab 1 (Department Block)        | 50          | 3       | 62             | 255.255.255.192   | 10.20.0.128     | 10.20.0.129 - 10.20.0.190      | 10.20.0.191      |
| Computer Lab 2 (Department Block)        | 50          | 4       | 62             | 255.255.255.192   | 10.20.0.192     | 10.20.0.193 - 10.20.0.254      | 10.20.0.255      |
| Computer Vision and Machine Learning Lab | 50          | 5       | 62             | 255.255.255.192   | 10.20.1.0       | 10.20.1.1 - 10.20.1.62         | 10.20.1.63       |
| Digital Learning and Media Centre        | 31          | 6       | 62             | 255.255.255.192   | 10.20.1.64      | 10.20.1.65 - 10.20.1.126       | 10.20.1.127      |
| Staff Rooms                              | 14          | 7       | 14             | 255.255.255.240   | 10.20.1.128     | 10.20.1.129 - 10.20.1.142      | 10.20.1.143      |
| Microprocessor Lab                       | 12          | 8       | 14             | 255.255.255.240   | 10.20.1.144     | 10.20.1.145 - 10.20.1.158      | 10.20.1.159      |
| Network Engineering Lab                  | 10          | 9       | 14             | 255.255.255.240   | 10.20.1.160     | 10.20.1.161 - 10.20.1.174      | 10.20.1.175      |
| Lecture Halls                            | 8           | 10      | 14             | 255.255.255.240   | 10.20.1.176     | 10.20.1.177 - 10.20.1.190      | 10.20.1.191      |
| Staff Office                             | 5           | 11      | 6              | 255.255.255.248   | 10.20.1.192     | 10.20.1.193 - 10.20.1.198      | 10.20.1.199      |
| Technical Officers Rooms (Department)    | 4           | 12      | 6              | 255.255.255.248   | 10.20.1.200     | 10.20.1.201 - 10.20.1.206      | 10.20.1.207      |
| Department Office                        | 3           | 13      | 6              | 255.255.255.248   | 10.20.1.208     | 10.20.1.209 - 10.20.1.214      | 10.20.1.215      |
| Meeting Room (IT Block)                  | 3           | 14      | 6              | 255.255.255.248   | 10.20.1.216     | 10.20.1.217 - 10.20.1.222      | 10.20.1.223      |
| Department Meeting Room                  | 3           | 15      | 6              | 255.255.255.248   | 10.20.1.224     | 10.20.1.225 - 10.20.1.230      | 10.20.1.231      |
| Director Office                          | 2           | 16      | 2              | 255.255.255.252   | 10.20.1.232     | 10.20.1.233 - 10.20.1.234      | 10.20.1.235      |
| Technical Officers Rooms (IT Block)      | 2           | 17      | 2              | 255.255.255.252   | 10.20.1.236     | 10.20.1.237 - 10.20.1.238      | 10.20.1.239      |
| Printing Room                            | 2           | 18      | 2              | 255.255.255.252   | 10.20.1.240     | 10.20.1.241 - 10.20.1.242      | 10.20.1.243      |
| Network Manager Room                     | 1           | 19      | 2              | 255.255.255.252   | 10.20.1.244     | 10.20.1.245 - 10.20.1.246      | 10.20.1.247      |
| Lobby Area                               | 1           | 20      | 2              | 255.255.255.252   | 10.20.1.248     | 10.20.1.249 - 10.20.1.250      | 10.20.1.251      |


---

## Configuration Steps

### Router Configuration
1. **Assign IP Addresses**: Configure IP addresses for each PC, printer, and other devices as per the network diagram.
2. **Access Restrictions**:
   - **Printers**:
     - Printer in the department office can only be accessed by department staff.
     - Printer in the IT Centre printing room is restricted to IT block staff.

<img width="468" alt="image" src="https://github.com/user-attachments/assets/a78f95d1-0a4e-48e9-8753-34019bb6c6bb">


<img width="387" alt="image" src="https://github.com/user-attachments/assets/693fafb6-34f2-4655-9849-f8df3fe87997">


### IP CONFIGURATION OF PC

<img width="468" alt="image" src="https://github.com/user-attachments/assets/3b45aa1a-062a-4ebd-bf8a-87870563a655">

<img width="468" alt="image" src="https://github.com/user-attachments/assets/a3a58103-9281-43d9-bc91-b62cf4890086">


### CONFIGURING WIRELESS ROUTER

<img width="468" alt="image" src="https://github.com/user-attachments/assets/06e6837e-0cfd-4f53-b04a-6ed9ca402d47">

<img width="464" alt="image" src="https://github.com/user-attachments/assets/42042ff4-ae9e-448a-a311-e8b45cbb6591">




### Switch Configuration (2960-24TT)
- **IT Block**:
  - **Computer Lab 1**: Use Switch 5, Switch 4, and Switch 1 to support 60 PCs.
  - **Digital Learning and Media Centre**: Use Switches 8 and 15 to manage connections.
  - 
 <img width="459" alt="image" src="https://github.com/user-attachments/assets/77810903-169a-4f1c-b7dc-b72790ecc1fc">

   
- **Department Block**:
  - **Meeting Room & Network Engineering Lab**: Connect via Switch 3.
  - **Computer Lab 1**: Use Switches 12, 18, and 19.

<img width="468" alt="image" src="https://github.com/user-attachments/assets/056d4c80-3c4b-4bcf-aa9b-6665f0d46739">


<img width="468" alt="image" src="https://github.com/user-attachments/assets/801dc829-88dc-4223-b038-fac4b14bd94f">



## Network Diagrams

- **Whole Network Diagram**:
  - ![image](https://github.com/user-attachments/assets/7f9dcdc1-f6ca-45c4-8d4f-9a4a6132be45)


- **IT Block Network Diagram**:
  - <img width="497" alt="image" src="https://github.com/user-attachments/assets/292fae4f-1273-4c0e-b583-4597b6484a15">

- **First floor-DEP**
<img width="459" alt="image" src="https://github.com/user-attachments/assets/782806af-4eb5-4e3d-a563-c0a7cbf29710">


- **Ground floor-DEP**
<img width="460" alt="image" src="https://github.com/user-attachments/assets/b75955e6-132e-4222-8bdb-a482b4118118">


- **Department Block Network Diagram**:
  - ![image](https://github.com/user-attachments/assets/0445a403-2061-4dc3-8a55-39a5173ddff6)




## Summary
This document outlines the structured setup of networked devices, VLAN configurations, and restrictions for the IT and Department blocks to maintain efficient and secure network access. The configuration includes IP addressing, VLAN allocation, and device-specific network access controls to meet departmental needs.
