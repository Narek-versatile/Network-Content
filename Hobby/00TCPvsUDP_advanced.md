

# Advanced Transport Layer Architecture: TCP, UDP, and the Modern Web

## Chapter 1: The TCP Reliability Engine
TCP is a **sliding window, byte-stream protocol**. Its job is to make an unreliable network look like a perfect, ordered pipe to the application.

### 1.1 The State Machine (The Life of a Connection)
Beyond the `SYN` and `ACK`, the state machine manages how connections end and how they handle errors.
* **Establishment:** The 3-way handshake syncs **Sequence Numbers**. These numbers are not just IDs; they represent the byte-count of data sent, allowing the receiver to reassemble fragments in the correct order.
* **Termination:** Uses a 4-way handshake (`FIN` -> `ACK` -> `FIN` -> `ACK`). 
* **TIME_WAIT:** The most misunderstood state. After closing a connection, the OS keeps the socket "reserved" for 2MSL (Maximum Segment Lifetime). This prevents delayed packets from a previous session from being mistakenly accepted by a new session using the same IP/Port.



### 1.2 Flow Control vs. Congestion Control
* **Flow Control (The Receiver’s Limit):** The receiver tells the sender, "My buffer is this big (**RWND**). Don't send more than this." It prevents the sender from overwhelming the receiver.
* **Congestion Control (The Network’s Limit):** The sender monitors the network for drops or delays. It maintains a **CWND** (Congestion Window). The actual amount of data sent is the minimum of these two:
    $$\text{Allowed Data} = \min(RWND, CWND)$$



---

## Chapter 2: The UDP Revolution (QUIC & NAT)
UDP is no longer just for DNS and VoIP. It is being used to rebuild the internet because TCP is too rigid to update.

### 2.1 The Problem with TCP: Head-of-Line (HOL) Blocking
In TCP, if Packet #1 is lost, Packets #2 and #3 stay in the buffer even if they arrived perfectly. The application cannot see them until #1 is retransmitted. This is "Head-of-Line Blocking."

### 2.2 The Solution: QUIC (HTTP/3)
QUIC runs on top of **UDP** but adds its own reliability. 
* **Streams:** It treats different files (e.g., an image and a CSS file) as independent streams. If the image packet is lost, the CSS file keeps loading.
* **0-RTT Handshake:** It combines the security handshake (TLS) and the transport handshake into one, saving precious milliseconds.

### 2.3 NAT Traversal
Since most devices are behind routers (NAT), they don't have public IPs. UDP uses:
* **STUN:** To discover your public IP.
* **ICE:** To find the best path between two peers.
* **TURN:** A fallback relay server if the firewall is too "symphatetic" (strict).



---

## Chapter 3: Performance Mathematics
To tune a high-performance network, you need to calculate your limits.

### 3.1 Bandwidth-Delay Product (BDP)
This defines how much data "fills the pipe." If you want a 10Gbps link to be efficient, your TCP window must be at least as large as the BDP.
$$BDP = \text{Bandwidth (bits/sec)} \times RTT \text{ (seconds)}$$

### 3.2 The Mathis Equation
This calculates the theoretical maximum throughput on a link with packet loss ($p$):
$$\text{Max Throughput} = \frac{MSS}{RTT \cdot \sqrt{p}}$$
* **Takeaway:** If packet loss is 1%, your speed will never exceed a certain threshold, no matter how much bandwidth you buy.

---

## Glossary: New & Advanced Terms

| Term | Definition |
| :--- | :--- |
| **BBR (Bottleneck Bandwidth and RTT)** | A modern congestion control algorithm by Google that ignores packet loss and instead focuses on the actual speed of the link. |
| **SACK (Selective ACK)** | Allows a receiver to say "I got packets 1, 2, 4, and 5" so the sender only retransmits packet 3, rather than everything from 3 onwards. |
| **MSS (Maximum Segment Size)** | The largest amount of data (in bytes) that TCP can handle in a single, unfragmented segment. Usually 1460 bytes on Ethernet. |
| **Anycast** | A routing method where a single IP address is shared by multiple servers in different locations; the network routes you to the "closest" one (common in DNS/CDNs). |
| **Head-of-Line (HOL) Blocking** | A performance bottleneck where one delayed or lost packet holds up an entire sequence of otherwise successful packets. |
| **Zero-Window** | A TCP signal from a receiver telling the sender to stop transmitting entirely because its local buffer is full. |
| **Nagle's Algorithm** | A technique that buffers small outgoing packets to send them all at once, reducing header overhead but increasing latency (often disabled in gaming). |
| **L7 Load Balancing** | Distributing traffic based on the content of the data (HTTP headers, cookies) rather than just the IP/Port (L4). |

