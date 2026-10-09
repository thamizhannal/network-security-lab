
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
  * Drill down into any field's structure.[cite: 2]
* **Packet Bytes Pane (Bottom):**[cite: 2]
  * Raw hexadecimal and ASCII view.[cite: 2]
  * Highlights bytes matching the selected field in the details pane.[cite: 2]
  * Useful for low-level byte inspection.[cite: 2]

---

## 4. Reading Packet Information[cite: 2]

| Field | Description |
| :--- | :--- |
| **Source / Destination** | The sending and receiving IP addresses of a packet. |
| **Protocol** | The protocol used (e.g., TCP, UDP, DNS, HTTP, HTTPS). |
| **Packet Length** | Total size of the packet in bytes. |
| **Ports** | Source and destination port numbers identifying the service. |[cite: 2]

---

## 5. Introduction to Wireshark Filters[cite: 2]

* **Why Use Display Filters?**[cite: 2]
  * Raw captures can contain thousands of packets.[cite: 2]
  * Filters narrow the view to only relevant traffic.[cite: 2]
* **Where Filters Are Applied:**[cite: 2]
  * Typed into the display filter bar at the top of Wireshark.[cite: 2]
  * **Green bar:** Valid syntax.[cite: 2]
  * **Red bar:** Invalid syntax.[cite: 2]
* **Result:**[cite: 2]
  * Only packets matching the filter expression remain visible.[cite: 2]

---

## 6. Common Display Filters[cite: 2]

* `tcp` / `udp` — Show only TCP or UDP traffic.[cite: 2]
* `dns` — Show only DNS query and response packets.[cite: 2]
* `http` / `https` — Show web traffic over HTTP or HTTPS (TLS).[cite: 2]
* `ip.addr` / `tcp.port` — Filter by a specific IP address or port number.[cite: 2]

---

## 7. Using Filter Operators and Expressions[cite: 2]

| Operator / Expression | Function | Examples |
| :--- | :--- | :--- |
| `==` / `!=` | Equal to / not equal to a given value | `ip.addr == 192.168.10.1`<br>`ip.addr != 192.168.10.1` |
| `>` / `<` | Greater than / less than a given value | `tcp.len > 1000`<br>`frame.len < 100` |
| `contains` | Field or payload contains a given substring | `http.request.uri contains "login"`<br>`tcp contains "password"` |
| `and` / `or` / `not` | Combine or negate multiple filter expressions | `ip.addr == 192.168.10.1 and tcp.port == 443` |[cite: 2]

---

## 8. Analyzing Web Traffic[cite: 2]

* **Examining HTTP Requests & Responses:**[cite: 2]
  * Inspect request methods: GET, POST, PUT, DELETE.[cite: 2]
  * Check response codes: 200 OK, 301, 404, 500.[cite: 2]
* **Key Fields to Review:**[cite: 2]
  * Host, URI, headers, and packet content payload.[cite: 2]
  * Use filter: `http.request` or `http.response`.[cite: 2]
* **Traffic Flow Sequence:**[cite: 2]
  1. Client Request[cite: 2]
  2. DNS Resolution[cite: 2]
  3. TCP Handshake[cite: 2]
  4. HTTP GET/POST[cite: 2]
  5. Server Response[cite: 2]

---

## 9. Following Network Conversations[cite: 2]

* **What is 'Follow Stream'?**[cite: 2]
  * Reassembles all packets in a single TCP/UDP conversation.[cite: 2]
  * **Action:** Right-click a packet → **Follow** → **TCP/UDP/HTTP Stream**.[cite: 2]
* **Why It's Useful:**[cite: 2]
  * View a full exchange between client and server in order.[cite: 2]
  * Colors distinguish each side of the conversation:[cite: 2]
    * **Red:** Client request/data[cite: 2]
    * **Blue:** Server response/data[cite: 2]
* **Common Use Cases:**[cite: 2]
  * Reconstructing credentials, files, or full HTTP sessions.[cite: 2]

---

## 10. Searching and Sorting Captured Traffic[cite: 2]

* **Sort by Column:** Click any column header to sort packets by that field.[cite: 2]
* **Find Packet:** Press **Ctrl+F** to open search across packet contents, bytes, or fields.[cite: 2]
* **Search Scope:** Search within packet list, details, or bytes pane.[cite: 2]
* **Search Direction:** Search forward or backward from the currently selected packet.[cite: 2]

---

## Hands-on Lab: HTTP Login & Packet Analysis[cite: 2]

### Exercise Setup:[cite: 2]
1. Open the Kali Linux terminal.[cite: 2]
2. Launch Wireshark by typing `wireshark`.[cite: 2]
3. Select the network interface (e.g., `eth0`).[cite: 2]

### Lab Walkthrough:[cite: 2]
1. Open a web browser and navigate to `http://testfire.net`.[cite: 2]
2. Open the login page and enter a test username and password.[cite: 2]
3. In Wireshark, apply the filter: `http`.[cite: 2]
4. Locate the `POST /doLogin HTTP/1.1` request packet.[cite: 2]
5. Inspect the **Packet Details** pane under **HTML Form URL Encoded** to locate submitted form fields:[cite: 2]
   * `uid` = `jsmith`[cite: 2]
   * `passw` = `Demo1234`[cite: 2]
   * `btnSubmit` = `Login`[cite: 2]
6. Apply IP filter: `ip.src == 192.168.181.128`.[cite: 2]
7. Right-click the HTTP session and select **Follow** → **HTTP Stream** to analyze the complete request and response payload.[cite: 2]

