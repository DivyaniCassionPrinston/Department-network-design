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

| VLAN Name                    | Needed Size | VLAN No | Allocated Size | Subnet Mask       | Network Address | Assignable Range        | Broadcast ID |
|------------------------------|-------------|---------|----------------|--------------------|-----------------|-------------------------|--------------|
| Computer Lab 1 (IT Block)    | 60          | 1       | 62             | 255.255.255.192   | 10.20.0.0       | 10.20.0.1 - 10.20.0.62  | 10.20.0.63   |
| Computer Lab 2 (IT Block)    | 60          | 2       | 62             | 255.255.255.192   | 10.20.0.64      | 10.20.0.65 - 10.20.0.126| 10.20.0.127  |
| Computer Lab 1 (Department)  | 50          | 3       | 62             | 255.255.255.192   | 10.20.0.128     | 10.20.0.129 - 10.20.0.190| 10.20.0.191 |
| ...                          | ...         | ...     | ...            | ...                | ...             | ...                     | ...          |

*(Add other VLANs as per the PDF details)*

---

## Configuration Steps

### Router Configuration
1. **Assign IP Addresses**: Configure IP addresses for each PC, printer, and other devices as per the network diagram.
2. **Access Restrictions**:
   - **Printers**:
     - Printer in the department office can only be accessed by department staff.
     - Printer in the IT Centre printing room is restricted to IT block staff.

### Switch Configuration (Cisco 2960-24TT)
- **IT Block**:
  - **Computer Lab 1**: Use Switch 5, Switch 4, and Switch 1 to support 60 PCs.
  - **Digital Learning and Media Centre**: Use Switches 8 and 15 to manage connections.
- **Department Block**:
  - **Meeting Room & Network Engineering Lab**: Connect via Switch 3.
  - **Computer Lab 1**: Use Switches 12, 18, and 19.

*(Add further configurations as per setup)*

### Wireless Router Configuration
- **Wi-Fi Setup**: Configure Wi-Fi routers to provide network access across IT and Department blocks with restricted access per VLAN.

---

## Network Diagrams
- **IT Block Network Diagram**:
  - *(Include a description or image if applicable)*

- **Department Block Network Diagram**:
  - *(Include a description or image if applicable)*

- **Whole Network Diagram**:
  - *(Include a description or image if applicable)*

---

## Summary
This document outlines the structured setup of networked devices, VLAN configurations, and restrictions for the IT and Department blocks to maintain efficient and secure network access. The configuration includes IP addressing, VLAN allocation, and device-specific network access controls to meet departmental needs.
