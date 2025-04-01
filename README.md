# *Network Packet Sniffer Tool 🌐*
##  *Overview*
It is a packet sniffer tool that captures and analyzes network packets and display relevant information such as source and destination IP addresses, protocols, and payload data. Ensure the ethical use of the tool for educational purposes. This Python script uses **Scapy** to capture and analyze network traffic in real-time, extracting key details like:  
- 🏷 Source/Destination IPs
- 🔄 Protocols (TCP/UDP/ICMP, etc.)  
- 📦 Payload Data

## *Tech Stack*
📚 *Core Libraries*  
Scapy– A powerful packet manipulation library for network analysis, sniffing, and decoding.

## *Key Features*  
### *Packet Capture*  
✅ Sniffs live network traffic in promiscuous mode (if permitted).  
✅ Filters IP packets (IPv4) and extracts:  
   - 🌍 Source & Destination IPs
   - 🔗 Protocol (TCP/UDP/ICMP, etc.)  

### Payload Inspection 
🔍 Extracts & attempts to decode TCP/UDP payloads (if Raw layer exists).  
⚙️ Handles encoding errors gracefully (utf-8 with fallback).  

### Real-Time Output  
📌 Prints packet metadata (IPs, protocol) and payload (if decodable).  

## *Workflow*  
1️⃣ **Sniffing:**  
   - 🏗 `scapy.sniff()` captures packets **in real-time**.  
   - 🎯 `prn=packet_callback` processes each packet via the **callback function**.  

2️⃣ *Analysis*  
   - 🛡 Checks for **IP layer**, then **TCP/UDP layers**.  
   - 📝 Attempts to **decode payloads** and prints if successful.  

This setup makes the packet sniffer **efficient, insightful, and extensible! 🚀
