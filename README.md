# 🏨 Hotel Management Network (Cisco Packet Tracer)

> 🎓 Lab project for **CSE321: Computer Networks**, Daffodil International University (Spring 2025) · Team of 5

A complete hotel network infrastructure designed and simulated in **Cisco Packet Tracer**. Each department and floor has its own VLAN and subnet, routers connect the whole building, DHCP hands out IP addresses automatically, and the network supports **wireless access points** and **VoIP IP phones**.

🌐 **Project website:** https://inglorious-star.github.io/Hotel-Management-Network-Cisco-Packet-Tracer/

![Network topology in Cisco Packet Tracer](IMG/project%20ss.jpg)

---

## ✨ Features

- 🧩 **VLANs** to separate each department and floor
- 🔀 **Cisco 2811 routers** connecting departments and floors
- 🔌 **Cisco 2950 switches** for LAN connectivity inside each department
- 📡 **DHCP** for automatic IP address assignment
- 📶 **Wireless access points** in the Admin Office, Reception and Second Floor
- ☎️ **VoIP IP phones** in the IT Department, Second Floor and Third Floor
- 🏗️ **Hierarchical design** that is easy to scale and maintain

---

## 🌐 Network zones and subnets

| Zone | Network | Subnet | Devices |
|---|---|---|---|
| Admin Office | LAN 1 | 192.168.10.0/24 | Laptops, PC, Access Point |
| Reception Area | LAN 2 | 192.168.12.0/24 | PCs, Access Point |
| Marketing Department | LAN 1 | 192.168.13.0/24 | PCs |
| IT Department | LAN 2 | 192.168.19.0/24 | PCs, IP Phone |
| Second Floor | LAN 3 | 192.168.15.0/24 | PCs, Access Point, IP Phone |
| Third Floor | LAN 4 | 192.168.18.0/24 | PCs, IP Phone |
| Server Room | Internal LAN | 192.168.17.0/24 | Servers |

## 🧰 VLANs

| VLAN | Department |
|---|---|
| 10 | Admin Office |
| 12 | Reception |
| 13 | Marketing |
| 15 | Second Floor |
| 17 | Server Room |
| 18 | Third Floor |
| 19 | IT Department |

## 🔗 Key interface addresses

| IP address | Interface |
|---|---|
| 192.168.10.1 | Switch0 to Router1 |
| 192.168.11.1 / 192.168.11.2 | Router1 to Router7 link |
| 192.168.12.1 | Reception Area (LAN 2) |
| 192.168.13.1 | Marketing Department (LAN 1) |
| 192.168.14.1 / 192.168.14.2 | Router7 to Router8 link |
| 192.168.15.1 | Second Floor (LAN 3) |
| 192.168.16.1 | First Floor segment |
| 192.168.17.1 | Router8 (Server Room) |
| 192.168.18.1 | Switch5 to Router8 (Third Floor) |
| 192.168.19.1 | IT Department (LAN 2) |

---

## 🛠️ Technologies

| Technology | Purpose |
|---|---|
| VLAN | Logical segmentation of the network |
| DHCP | Automatic IP address assignment |
| Wireless (Access Points) | Wireless connectivity for laptops and mobile devices |
| VoIP (IP Phones) | Internal voice communication |
| Cisco 2950 Switch | LAN connectivity inside departments |
| Cisco 2811 Router | Routing between VLANs and floors |

---

## 📁 Project structure

```
Hotel-Management-Network-Cisco-Packet-Tracer/
├── index.html   # Project showcase website (topology, subnets, VLANs, team)
├── IMG/         # Topology screenshot
└── README.md
```

---

## 👥 Team

| Member | Responsibility |
|---|---|
| Fahim Montasir ([@inglorious-star](https://github.com/inglorious-star)) | Server Room & Final Testing |
| Mst. Tabassum Binte Zia Prova | VLAN Configuration & Switching |
| Mubas Sera Noon | DHCP & Wireless Network |
| Raiyan Jahan ([@rynrafsan](https://github.com/rynrafsan)) | Network Design & IP Addressing |
| Md. Ibna Labid | VoIP Configuration |
# 🏨 Hotel Management Network (Cisco Packet Tracer)

> 🎓 Lab project for **CSE321: Computer Networks**, Daffodil International University (Spring 2025) · Team of 5

A complete hotel network infrastructure designed and simulated in **Cisco Packet Tracer**. Each department and floor has its own VLAN and subnet, routers connect the whole building, DHCP hands out IP addresses automatically, and the network supports **wireless access points** and **VoIP IP phones**.

🌐 **Project website:** https://inglorious-star.github.io/Hotel-Management-Network-Cisco-Packet-Tracer/

![Network topology in Cisco Packet Tracer](IMG/project%20ss.jpg)

---

## ✨ Features

- 🧩 **VLANs** to separate each department and floor
- 🔀 **Cisco 2811 routers** connecting departments and floors
- 🔌 **Cisco 2950 switches** for LAN connectivity inside each department
- 📡 **DHCP** for automatic IP address assignment
- 📶 **Wireless access points** in the Admin Office, Reception and Second Floor
- ☎️ **VoIP IP phones** in the IT Department, Second Floor and Third Floor
- 🏗️ **Hierarchical design** that is easy to scale and maintain

---

## 🌐 Network zones and subnets

| Zone | Network | Subnet | Devices |
|---|---|---|---|
| Admin Office | LAN 1 | 192.168.10.0/24 | Laptops, PC, Access Point |
| Reception Area | LAN 2 | 192.168.12.0/24 | PCs, Access Point |
| Marketing Department | LAN 1 | 192.168.13.0/24 | PCs |
| IT Department | LAN 2 | 192.168.19.0/24 | PCs, IP Phone |
| Second Floor | LAN 3 | 192.168.15.0/24 | PCs, Access Point, IP Phone |
| Third Floor | LAN 4 | 192.168.18.0/24 | PCs, IP Phone |
| Server Room | Internal LAN | 192.168.17.0/24 | Servers |

## 🧰 VLANs

| VLAN | Department |
|---|---|
| 10 | Admin Office |
| 12 | Reception |
| 13 | Marketing |
| 15 | Second Floor |
| 17 | Server Room |
| 18 | Third Floor |
| 19 | IT Department |

## 🔗 Key interface addresses

| IP address | Interface |
|---|---|
| 192.168.10.1 | Switch0 to Router1 |
| 192.168.11.1 / 192.168.11.2 | Router1 to Router7 link |
| 192.168.12.1 | Reception Area (LAN 2) |
| 192.168.13.1 | Marketing Department (LAN 1) |
| 192.168.14.1 / 192.168.14.2 | Router7 to Router8 link |
| 192.168.15.1 | Second Floor (LAN 3) |
| 192.168.16.1 | First Floor segment |
| 192.168.17.1 | Router8 (Server Room) |
| 192.168.18.1 | Switch5 to Router8 (Third Floor) |
| 192.168.19.1 | IT Department (LAN 2) |

---

## 🛠️ Technologies

| Technology | Purpose |
|---|---|
| VLAN | Logical segmentation of the network |
| DHCP | Automatic IP address assignment |
| Wireless (Access Points) | Wireless connectivity for laptops and mobile devices |
| VoIP (IP Phones) | Internal voice communication |
| Cisco 2950 Switch | LAN connectivity inside departments |
| Cisco 2811 Router | Routing between VLANs and floors |

---

## 📁 Project structure

```
Hotel-Management-Network-Cisco-Packet-Tracer/
├── index.html   # Project showcase website (topology, subnets, VLANs, team)
├── IMG/         # Topology screenshot and team photos
└── README.md
```

---

## 👥 Team

| Member | Responsibility |
|---|---|
| Fahim Montasir ([@inglorious-star](https://github.com/inglorious-star)) | Server Room & Final Testing |
| Mst. Tabassum Binte Zia Prova | VLAN Configuration & Switching |
| Mubas Sera Noon | DHCP & Wireless Network |
| Raiyan Jahan ([@rynrafsan](https://github.com/rynrafsan)) | Network Design & IP Addressing |
| Md. Ibna Labid | VoIP Configuration |
