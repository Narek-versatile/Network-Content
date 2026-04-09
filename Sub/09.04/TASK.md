Class: Computer Networks

Description: PART 1: THEORY QUESTIONS

1. Explain what a computer network is and why it is used. Give at least 3 real-life examples.

2. What is the difference between LAN, WAN, MAN, and PAN? Give one example for each.

3. Describe the following network topologies:
   - Star
   - Bus
   - Ring
   - Mesh  
   Which one is most commonly used today and why?

4. What is the role of each of the following devices:
   - Router
   - Switch
   - Hub
   - Modem
   - Access Point

5. What is the difference between routing and switching?

6. Compare wired and wireless networks in terms of:
   - Speed
   - Security
   - Mobility

7. What is an IP address? Why do devices need it?

8. What is the difference between IPv4 and IPv6?

9. Explain the difference between public and private IP addresses.  
   Give 3 examples of private IP ranges.

10. What is NAT and why is it used?

11. What is a network protocol? What is a port?

12. Match the following protocols with their ports and purpose:
   - HTTP
   - HTTPS
   - FTP
   - SSH
   - DNS
   - DHCP

13. What is HTTP and how does it work (request/response model)?

14. What is the difference between HTTP and HTTPS?

15. What are HTTP status codes? Explain the difference between:
   - 2xx
   - 3xx
   - 4xx
   - 5xx


════════════════════════════════════════════════════════════

PART 2: PRACTICAL TASKS

1. Open terminal and run:
   hostname  
   Write your device hostname.

2. Run:
   ping google.com  
   What does ping show? Write 2–3 observations.

3. Find your local IP address using one of the commands:
   ip a  
   ifconfig  
   Write your IP and explain if it is private or public.

4. Run:
   curl -I LINK  
   Write the status code and at least 3 headers you see.

5. Run:
   curl -v LINK  
   What extra information do you see compared to normal curl?

6. Run:
   ss -tuln   or   netstat -tuln  
   Write 3 open/listening ports from your system.

7. Draw your home network:
   - Internet
   - Router/Modem
   - Devices (phone, laptop, TV)  
   Explain how data flows between them.

8. Identify:
   - Do you use Wi-Fi or Ethernet?
   - What cable type (if wired)?
   - Why is this setup used?

9. Visit 5 different websites and check their status codes using curl.  
   Write results like:
   - site → status code

10. Send a POST request:
   curl -X POST -d "name=test" LINK  
   What response do you get?


════════════════════════════════════════════════════════════

PART 3: ANALYTICAL / THINKING TASKS

1. Your school network is slow. List 3 possible reasons related to:
   - Devices
   - Network type
   - Media (cables/Wi-Fi)

2. When would you choose:
   - Fiber over Ethernet?
   - Ethernet over Wi-Fi?

3. Why is mesh topology rarely used in home networks?

4. If all devices in a network have private IPs, how do they access the internet?

5. What would happen if DNS did not exist?

6. Why is HTTPS more secure than HTTP?

7. If port 80 is blocked, what happens when you try to open a website?

8. Imagine you are designing a network for a small office (10 people):
   - What topology would you use?
   - What devices are needed?
   - Wired or wireless?

9. Why is IPv6 important for the future?

10. Explain a real-life example of client-server communication using HTTP.


════════════════════════════════════════════════════════════

PART 4: SHORT QUIZ (MULTIPLE CHOICE)

1. Which device connects different networks?
   A) Switch  
   B) Router  
   C) Hub  
   D) NIC  

2. Which topology has a central node?
   A) Ring  
   B) Bus  
   C) Star  
   D) Mesh  

3. Which protocol uses port 443?
   A) HTTP  
   B) HTTPS  
   C) FTP  
   D) SSH  

4. Which is a private IP?
   A) 8.8.8.8  
   B) 192.168.1.5  
   C) 1.1.1.1  
   D) 172.300.1.1  

5. What does DNS do?
   A) Encrypts data  
   B) Converts domain to IP  
   C) Sends emails  
   D) Routes packets  

6. Which command checks connectivity?
   A) curl  
   B) ping  
   C) ssh  
   D) chmod  

7. Which is wireless technology?
   A) Fiber  
   B) Ethernet  
   C) Wi-Fi  
   D) Coaxial  

8. What does HTTP stand for?
   A) Hyper Transfer Text Protocol  
   B) HyperText Transfer Protocol  
   C) HighText Transfer Protocol  
   D) HyperText Transmission Process  

9. Which layer concept includes IP addressing?
   A) Physical  
   B) Network  
   C) Application  
   D) Data link  

10. What does a switch do?
    A) Connects internet  
    B) Connects devices in LAN  
    C) Converts signals  
    D) Provides Wi-Fi  


════════════════════════════════════════════════════════════

