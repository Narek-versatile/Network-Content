Class: Computer Networks

Description: These are **hands-on tasks** you should complete before the exam. If you can do all of them without looking anything up, you are ready for the exam. Do each task in your terminal and write down the output in your notebook.

---

## TASK 1 — Map your own network

1. Draw your home or school network on paper. Include:
   - The **ISP line** coming in
   - **Modem**
   - **Router**
   - **Switch** (if any)
   - **Wi-Fi Access Point** (often built into the router)
   - All your **devices** (laptop, phone, TV…)
2. Draw an arrow showing how a request to `google.com` leaves your laptop and reaches the internet.
3. Label which parts are **wired** and which are **wireless**.

**Goal:** understand the role of every device in a real network.

---

## TASK 2 — Identify your IP addresses

Run each command and write down the result:

```bash
hostname
ip a                 # or: ifconfig
ip route             # shows your default gateway
curl ifconfig.me     # shows your PUBLIC IP
```

Now answer:
- What is your **local (private)** IP? Which private range is it in?
- What is your **public** IP?
- Why are these two addresses different? (One-sentence answer: **NAT**.)
- What is your **default gateway** and what role does it play?

---

## TASK 3 — Test connectivity

```bash
ping google.com
ping 8.8.8.8
ping -c 4 1.1.1.1
```

Answer:
- What does `ping` measure?
- What does the `time=` value mean?
- What would it mean if `ping google.com` fails but `ping 8.8.8.8` works?

**Hint:** this tells you your **DNS** is broken, not your internet.

---

## TASK 4 — Explore DNS

```bash
nslookup google.com
nslookup wikipedia.org
dig example.com
dig example.com MX
dig example.com AAAA
```

For 5 different domains, fill this table:

| Domain | Record type | Result |
|---|---|---|
| google.com | A |  |
| wikipedia.org | A |  |
| github.com | AAAA |  |
| gmail.com | MX |  |
| yandex.com | A |  |

Answer:
- What does the **A** record give you?
- What does the **MX** record give you?
- What does the **AAAA** record give you?

---

## TASK 5 — Explore HTTP with curl

Pick any 5 websites and run:

```bash
curl -I LINK
curl -I LINK
curl -I LINK
curl -v LINK
curl -X POST -d "name=test" LINK
```

For each one, write down:
- The **status code** (200, 301, 404, 500…)
- At least 3 **headers** in the response
- The **difference** between the output of `curl`, `curl -I`, and `curl -v`

---

## TASK 6 — See which ports are open

```bash
ss -tuln          # Linux
# or
netstat -tuln     # Linux / macOS
```

Write down **3 listening ports** on your machine and guess which service each one is.

Answer:
- What does it mean for a port to be "listening"?
- What service usually runs on port 22? 80? 443? 53?

---

## TASK 7 — Practice the port/protocol table from memory

Close your notes. On paper, fill in this table:

| Protocol | Port | Purpose |
|---|---|---|
| HTTP |  |  |
| HTTPS |  |  |
| SSH |  |  |
| FTP |  |  |
| DNS |  |  |
| DHCP |  |  |
| SMTP |  |  |

Check yourself. Repeat until you can do it with no mistakes.

---

## TASK 8 — Compare TCP and UDP

Fill this table from memory:

| Feature | TCP | UDP |
|---|---|---|
| Connection type |  |  |
| Reliability |  |  |
| Ordering |  |  |
| Speed |  |  |
| Example use cases |  |  |

For each of these services, say **TCP or UDP** and explain why in one sentence:

1. Downloading a file
2. Live video streaming
3. Online multiplayer game
4. Sending an email
5. DNS lookup
6. SSH login
7. Zoom audio call
8. Online banking website

---

## TASK 9 — IP address analysis

For each IP address below, answer two questions:
**(a) Is this IPv4 or IPv6? (b) Is it private, public, or invalid?**

1. `192.168.1.1`
2. `10.5.5.5`
3. `8.8.8.8`
4. `172.20.10.3`
5. `2001:db8::1`
6. `300.1.1.1`
7. `127.0.0.1`
8. `185.70.40.10`

---

## TASK 10 — Explain a scenario in your own words

Write a short paragraph (5–8 sentences) explaining what happens when you type `LINK in your browser and press Enter. Your answer must include: **DNS, TCP, HTTPS, server, response**.

---

## TASK 11 — MITM and security

Answer in your own words:
1. What is a **Man-in-the-Middle attack**?
2. How does **HTTPS** protect against it?
3. You get a browser warning "**Invalid certificate**" on a café Wi-Fi. What do you do?
4. Name 3 ways to protect yourself on public networks.

---

## TASK 12 — Cables and media

Rank these from **fastest** to **slowest** in typical use:
- Cat5
- Cat6
- Fiber optic (single-mode)
- Wi-Fi (802.11b)
- Wi-Fi (802.11ax / Wi-Fi 6)

In one sentence each, explain when you would choose:
- Fiber over Ethernet
- Ethernet over Wi-Fi
- Wi-Fi over Ethernet

---

## TASK 13 — Design a small office network

Your client has an office with **10 employees**. Write a short plan answering:

- Which **topology**?
- Which **devices** do you need?
- **Wired** or **wireless** — or both?
- How do devices get their IPs automatically? (Which protocol?)
- How do all 10 computers share **one public IP** to reach the internet? (Which technology?)

---

## TASK 14 — Socket programming concept

Even if you don't write the full C code, you should know:

1. What is a **socket**?
2. What does a **TCP server** do in order? (`socket → bind → listen → accept → recv/send → close`)
3. What does a **TCP client** do in order? (`socket → connect → send/recv → close`)
4. What is the **IP + port** combination called, and why is it unique?

---

## ✅ Final self-check

Before the exam, you must be able to do all of the following without notes:

- [ ] Draw your home network and label every device
- [ ] Recite the main port numbers (80, 443, 22, 21, 53, 67/68, 25)
- [ ] Recite the private IP ranges
- [ ] Explain router vs switch vs modem vs access point
- [ ] Explain IP vs MAC
- [ ] Explain TCP vs UDP with examples
- [ ] Explain HTTP status code groups (2xx / 3xx / 4xx / 5xx)
- [ ] Explain what DNS does and name 5 record types
- [ ] Run `ip a`, `ip route`, `ping`, `curl -I`, `nslookup` and read their output
- [ ] Explain in plain words what happens when you type a URL in a browser

