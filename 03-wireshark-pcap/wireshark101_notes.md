# Wireshark 101: Masterclass
## Introduction to Network Packet Analysis and Packet Filtering[cite: 2]

---

## What We'll Cover[cite: 2]

1. Introduction to Wireshark[cite: 2]
2. Understanding Network Packet Capture[cite: 2]
3. Understanding the Wireshark Interface[cite: 2]
4. Reading Packet Information[cite: 2]
5. Introduction to Wireshark Filters[cite: 2]
6. Common Display Filters[cite: 2]
7. Using Filter Operators and Expressions[cite: 2]
8. Analyzing Web Traffic[cite: 2]
9. Following Network Conversations[cite: 2]
10. Searching and Sorting Captured Traffic[cite: 2]

---

## 1. Introduction to Wireshark[cite: 2]

* **What is Wireshark?**[cite: 2]
  * A free, open-source network protocol analyzer.[cite: 2]
  * Captures and displays data traveling on a network in real time.[cite: 2]
* **Role as a Packet Analyzer / Traffic Sniffer:**[cite: 2]
  * Inspects individual packets at a granular level.[cite: 2]
  * Helps diagnose network issues, security incidents, and protocol behavior.[cite: 2]
* **Widely Used in Security, IT, and Forensics:**[cite: 2]
  * Standard tool for network troubleshooting and penetration testing.[cite: 2]

---

## 2. Understanding Network Packet Capture[cite: 2]

* **Selecting the Network Interface:**[cite: 2]
  * Choose the correct adapter (Wi-Fi, Ethernet, VPN, etc.).[cite: 2]
  * Wireshark lists live traffic activity per interface before capture.[cite: 2]
* **Starting a Packet Capture:**[cite: 2]
  * Click the shark-fin icon or press **Ctrl+E** to begin capturing.[cite: 2]
  * Packets appear live in the Packet List pane as they arrive.[cite: 2]
* **Stopping a Packet Capture:**[cite: 2]
  * Click the red square icon or press **Ctrl+E** again to stop.[cite: 2]

---

## 3. Understanding the Wireshark Interface[cite: 2]

* **Packet List Pane (Top):**[cite: 2]
  * Summary line for every captured packet.[cite: 2]
  * Shows No., Time, Source, Destination, and Protocol.[cite: 2]
  * Click a row to inspect it in detail.[cite: 2]
* **Packet Details Pane (Middle):**[cite: 2]
  * Expandable tree of protocol layers (Ethernet II, IPv4, TCP/UDP, etc.).[cite: 2]
  * Drill down into any field's structure.