# 🏨 Hotel Management Network (Cisco Packet Tracer)

> 🎓 Lab project for **CSE321: Computer Networks**, Daffodil International University (Spring 2025) · Team of 5

A complete, **fully working** hotel network designed and simulated in **Cisco Packet Tracer**. Every department and floor has its own VLAN and subnet, three routers share routes with **OSPF**, **DHCP** hands out addresses automatically, guests and staff connect over **WPA2 Wi-Fi**, an internal **web + DNS server** hosts `hotel.local`, and **VoIP IP phones** call each other through Cisco CallManager Express.

🌐 **Project website:** https://inglorious-star.github.io/Hotel-Management-Network-Cisco-Packet-Tracer/

![Network topology in Cisco Packet Tracer](IMG/project%20ss.jpg)

---

## ✨ Features

- 🧩 **9 VLANs** separating departments, floors, servers and voice traffic
- 🔀 **3 × Cisco 2811 routers** with router-on-a-stick inter-VLAN routing
- 🗺️ **OSPF (area 0)** dynamic routing across the whole building
- 🔌 **Cisco 2960** access switch + **2 × Cisco 3560-24PS** PoE switches (they power the IP phones)
- 📡 **DHCP** pools on the routers for every user and voice VLAN
- 📶 **3 WPA2-PSK wireless networks**: `Hotel-Admin`, `Hotel-Reception`, `Hotel-Floor2`
- 🖥️ **Server0**: DNS (`hotel.local`) and HTTP (custom hotel intranet page)
- ☎️ **VoIP**: CallManager Express on the core router, extensions **1001–1003**, dedicated voice VLANs

---

## 🌐 Zones, VLANs and subnets

| Zone | VLAN | Subnet | Gateway (router) | Devices |
|---|---|---|---|---|
| Admin Office | 10 | 192.168.10.0/24 | Router1 | PC0, Access Point0, TabletPC |
| Reception | 12 | 192.168.12.0/24 | Router1 | PC1, PC2, Access Point1, Smartphone |
| Marketing | 13 | 192.168.13.0/24 | Router1 | PC3, PC4 |
| Server Room | 17 | 192.168.17.0/24 | Router2 | Server0 (192.168.17.10, static) |
| IT Department | 19 | 192.168.19.0/24 | Router2 | PC5 |
| IT Voice | 20 | 192.168.20.0/24 | Router2 | IP Phone0 (ext. 1001) |
| Second Floor | 15 | 192.168.15.0/24 | Router3 | PC6, Access Point2, TabletPC |
| Third Floor | 18 | 192.168.18.0/24 | Router3 | PC7 |
| Floors Voice | 21 | 192.168.21.0/24 | Router3 | IP Phone1 (1002), IP Phone2 (1003) |

### 🔗 Links between routers

| Link | Subnet | Addresses |
|---|---|---|
| Router1 ↔ Router2 (cross-over cable) | 192.168.11.0/24 | .1 / .2 |
| Router2 ↔ Router3 (transit VLAN 14 through SW2) | 192.168.14.0/24 | .1 / .2 |

> In the Packet Tracer file the routers are labelled **Router0 / Router1 / Router2** and the switches **Switch0 / Multilayer Switch0 / Multilayer Switch1**; their hostnames (in the CLI) are **Router1 / Router2 / Router3** and **SW1 / SW2 / SW3**.

---

## 🚀 How to open and test

1. Install **Cisco Packet Tracer 9.0** or newer (free with a [Cisco NetAcad](https://www.netacad.com/) account).
2. Download **[`HCMS.pkt`](HCMS.pkt)** from this repo and open it.
3. Wait about a minute (or click the ⏩ fast-forward button a few times) so DHCP, OSPF and the phones finish starting up.

Then try these tests:

| Test | How | Expected result |
|---|---|---|
| DHCP | Click any PC → Desktop → IP Configuration | An address in its zone's subnet, DNS 192.168.17.10 |
| Routing across floors | PC0 → Desktop → Command Prompt → `ping 192.168.18.11` | Replies from PC7 on the Third Floor (TTL 125) |
| DNS + web | PC0 → Desktop → Web Browser → `http://hotel.local` | The hotel intranet homepage from Server0 |
| Wi-Fi | Click a tablet or the smartphone → Config → Wireless0 | Connected to its SSID with a DHCP address |
| VoIP call | IP Phone2 → GUI → lift the handset → dial `1001` | IP Phone0 rings (Floor 3 → IT department) |

Wi-Fi password for all three SSIDs: `HotelWiFi2025` (demo lab only).

---

## 🛠️ Technologies

| Technology | Purpose |
|---|---|
| VLAN + 802.1Q trunks | Logical segmentation of the network |
| Router-on-a-stick | Inter-VLAN routing with router subinterfaces |
| OSPF | Dynamic routing between the three routers |
| DHCP (with option 150) | Automatic addressing for PCs, wireless devices and IP phones |
| WPA2-PSK Wi-Fi | Secure wireless access per zone |
| DNS + HTTP | Internal `hotel.local` website |
| CallManager Express + voice VLANs | Internal VoIP telephony |
| PoE (3560-24PS) | Powering the IP phones over Ethernet |

---

## 📁 Project structure

```
Hotel-Management-Network-Cisco-Packet-Tracer/
├── HCMS.pkt     # The working Packet Tracer network (built in PT 9.0.1)
├── configs/     # CLI configuration of every router and switch
├── index.html   # Project showcase website
├── IMG/         # Topology screenshot
└── README.md
```

> The `.pkt` file is a rebuild of the original lab project in Packet Tracer 9.0.1, so it opens in current versions and every service works out of the box.

---

## 👥 Team

| Member | Responsibility |
|---|---|
| Fahim Montasir ([@inglorious-star](https://github.com/inglorious-star)) | Server Room & Final Testing |
| Mst. Tabassum Binte Zia Prova | VLAN Configuration & Switching |
| Mubas Sera Noon | DHCP & Wireless Network |
| Raiyan Jahan ([@rynrafsan](https://github.com/rynrafsan)) | Network Design & IP Addressing |
| Md. Ibna Labid | VoIP Configuration |
