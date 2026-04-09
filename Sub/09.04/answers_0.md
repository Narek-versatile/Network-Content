# PART 1: THEORY QUESTIONS

## Explain what a computer network is and why it is used. Give at least 3 real-life examples.

Computer network is a group of nodes which can communicate inbetween them.

Few examples include hospital network, home network and school network.

## What is the difference between LAN, WAN, MAN, and PAN? Give one example for each.

**Local Area Network**
- Office network

**Wide Area Network**
- Network that interconnects few offices over a wide area

**Metropolitan Area Network**
- A network that connects very specific geographic area like a campus to a bigger center like headquarters

**Personal Area Network**
- Smallest type of network, interconnects personal devices over a very small distance

## Describe the following network topologies:

**Star**
- Nodes are connected as a star center is a single switch

**Bus**
- Low redundancy network

**Ring**
- Not too optimal use of cabling connecting nodes in a circle

**Mesh**
- Only appropriate if you need crazy redundant network and have extra money

### Which one is most commonly used today and why?

Star topology is state-of-the-art for small offices considering easy managing and cost efficiency.

## What is the role of each of the following devices:

**Router**

It takes the internet connection provided by the modem and "routes" it to all your various devices (phones, laptops, smart fridges). It also assigns local IP addresses to make sure data intended for your laptop doesn't accidentally end up on your TV.

**Switch**

A Switch is used to connect multiple devices together within the same network. Unlike a "dumb" hub, a switch is "smart"—it learns the hardware addresses (MAC addresses) of every device plugged into it. When it receives a packet of data, it sends it only to the specific device it was meant for.

**Hub**

A Hub is the ancestor of the switch. It also connects multiple devices on a network, but it lacks the "intelligence" of a switch. When a hub receives data, it doesn't know who it's for, so it simply broadcasts (screams) that data out to every single port and device connected to it.

**Modem - Modulator-Demodulator**

Its primary job is to convert the signal from your Internet Service Provider (ISP)—whether it's coming through cable, fiber, or a phone line—into a digital format your computer can actually understand.

**Access Point**

A Wireless Access Point (WAP) provides a wireless connection to an existing wired network. If you have a long Ethernet cable running to a far corner of your house, you can plug in an Access Point to create a Wi-Fi "bubble" in that area.

## What is the difference between routing and switching?

Routing involves assigning IP-s and flexibility. Switching involves forwarding to the destination that is identified by MAC address.

## Compare wired and wireless networks in terms of:

| Criterion | Winner |
|-----------|--------|
| Speed | Wired |
| Security | Wired |
| Mobility | Wireless |

## What is an IP address? Why do devices need it?

Internet Protocol is a unique identifier of a device in the local network. It defines the standard way of communicating with each other.

## What is the difference between IPv4 and IPv6?

**IPv4**
- Has 4 octaves, each consisting of 8 bits
- Decimal address looks like this: 192.168.10.1

**IPv6**
- Has 8 octaves, each consisting of 16 bits
- Hex address looks like this: 2001:0db8:85a3:0000:0000:8a2e:0370:7334

## Explain the difference between public and private IP addresses.

Private IP addresses are used for communicating over local network. Public IP is used for accessing networks outside your own.

## Give 3 examples of private IP ranges.

- 10.0.0.0 – 10.255.255.255 (10.0.0.0/8): Commonly used in large enterprise networks.
- 172.16.0.0 – 172.31.255.255 (172.16.0.0/12): Frequently used for docker containers or guest networks.
- 192.168.0.0 – 192.168.255.255 (192.168.0.0/16): Standard for home routers and small office networks.

## What is NAT and why is it used?

Network Address Translation is a practice where under few public addresses many local addresses are hidden under different port numbers.

## What is a network protocol? What is a port?

**Network protocols** are standardized sets of rules that govern how data is formatted, transmitted, and received across computer networks, enabling devices from different manufacturers to communicate effectively.

**Network ports** are virtual, software-based endpoints managed by operating systems to identify specific processes or services, allowing devices to differentiate traffic types over a single connection.

## Match the following protocols with their ports and purpose:

| Protocol | Port(s) | Purpose |
|----------|---------|---------|
| HTTP | 80 | HyperText Transfer Protocol |
| HTTPS | 443 | HyperText Transfer Protocol Secure |
| FTP | 20, 21 | File Transfer Protocol |
| SSH | 22 | Secure Shell |
| DNS | 53 | Domain Name Server |
| DHCP | 67, 68 | Dynamic Host Configuration Protocol |

## What is HTTP and how does it work (request/response model)?

HTTP (Hypertext Transfer Protocol) is the foundation of data communication for the World Wide Web, acting as an application-layer protocol for transferring web resources (HTML, images, videos). It operates via a client-server model, where a browser (client) sends a request, and the server sends back a response.

## What is the difference between HTTP and HTTPS?

HTTP (HyperText Transfer Protocol) and HTTPS (Secure) are protocols for data transmission, with HTTPS being the secure, encrypted version of HTTP. HTTPS uses SSL/TLS certificates to encrypt data and authenticate servers, protecting sensitive information from interception, unlike HTTP which sends data in plain text.

## What are HTTP status codes? Explain the difference between:

**2xx - Success**

Confirms the request was received, understood, and accepted. Common codes include 200 (OK), 201 (Created), 204 (No Content), and 206 (Partial Content).

**3xx - Redirection**

Signals that further action is needed to complete the request, usually involving a different URL. Examples are 301 (Moved Permanently), 302 (Found), 304 (Not Modified), and 308 (Permanent Redirect).

**4xx - Client Error**

Indicates a request error, such as bad syntax or an invalid request. Examples include 400 (Bad Request), 401 (Unauthorized), 403 (Forbidden), 404 (Not Found), and 429 (Too Many Requests).

**5xx - Server Error**

Indicates the server failed to fulfill a valid request. Common errors are 500 (Internal Server Error), 502 (Bad Gateway), 503 (Service Unavailable), and 504 (Gateway Timeout).
