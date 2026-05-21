Part 6: Practical Questions

1. Imagine you want to create your own website. Write all steps from beginning to end.

a) Choose a domain name
b) Choose a hosting provider
c) Buy a domain name
d) Buy hosting
e) Connect the domain to the server
f) Install Nginx
g) Configure Nginx
h) Configure firewall
i) Set up DNS
j) Configure SSL/TLS
k) Restart Nginx
l) Test the website

2. What are the steps required after purchasing a domain?

a) Configure DNS settings to point the domain to your server's IP address
b) Set up DNS records (e.g., A record, CNAME record) as needed
c) Configure email settings if you plan to use email with your domain
d) Set up SSL/TLS certificates for secure connections
e) Configure domain forwarding or parking if necessary
f) Verify domain ownership through registrar-specific verification processes

3. What are the steps required after creating a server?

a) Update the server's package list and upgrade existing packages
b) Install necessary software (e.g., Nginx, Node.js, Python, MySQL)
c) Configure the firewall to allow only necessary ports (e.g., 80, 443, 22)
d) Set up SSH access with strong authentication (e.g., SSH keys)
e) Configure a non-root user with sudo privileges for security
f) Set up automatic security updates
g) Create backups and configure monitoring

4. How would you connect a domain to your server?

a) Obtain the server's public IP address
b) Log in to your domain registrar's control panel
c) Navigate to the DNS management section
d) Create an A record that points the domain name to the server's IP address
e) For subdomains, create CNAME records pointing to the main domain or A records pointing to the IP address
f) Save the changes and wait for DNS propagation (which can take anywhere from a few minutes to 48 hours)
g) Verify the connection by accessing the website through the domain name

5. What could be possible reasons if your website does not open?

a) DNS propagation hasn't completed yet
b) The domain name is not pointing to the correct IP address
c) Firewall rules are blocking access
d) The web server (e.g., Nginx) is not running or misconfigured
e) The application server is not running or misconfigured
f) The domain name has expired
g) SSL/TLS certificate issues
h) Port conflicts or incorrect port configurations
i) Insufficient server resources (CPU, RAM, storage)
j) Network connectivity issues between the user and the server

6. If your domain points to the wrong IP address, what could happen?

a) Users will be directed to the wrong server or website
b) If the wrong IP belongs to an active server, users might see someone else's website
c) If the wrong IP is invalid, users will see an error message like "This site can't be reached"
d) Email services associated with the domain might not work correctly
e) SSL certificates might not validate properly
f) It can cause confusion and erode user trust in the website

7. If Nginx is stopped, what could happen to the website?

a) The website will become completely inaccessible to users
b) Users will see an error message such as "502 Bad Gateway" or "Connection Refused"
c) The server will continue to run, but Nginx will no longer be there to handle incoming HTTP requests
d) Any associated application server (e.g., Node.js, Python) will still be running, but users won't be able to access it through the domain
e) SSL/TLS termination will fail, preventing secure connections
f) If configured as a reverse proxy, all traffic will be blocked from reaching backend applications

8. Why might a website work on the server itself but not open from another computer?

a) The firewall on the server is blocking access from external networks
b) The web server is configured to only listen on localhost (127.0.0.1) instead of all interfaces
c) DNS propagation hasn't completed, so external computers can't resolve the domain name correctly
d) The server's public IP address is incorrect or has changed
e) Network routing issues prevent external traffic from reaching the server
f) SSL/TLS certificate issues are preventing external access
g) Local network restrictions or proxies are blocking the connection

9. Why do developers test websites before making them public?

a) To ensure functionality across different browsers and devices
b) To identify and fix bugs before they affect real users
c) To verify that performance meets expected standards
d) To confirm security measures are effective
e) To ensure the user experience is smooth and intuitive
f) To validate that all features work as intended
g) To verify that the website works with the domain name and DNS configuration

10. Why is understanding DNS and hosting important for developers?

a) It allows developers to deploy and manage their websites effectively
b) Understanding DNS helps in troubleshooting connectivity issues
c) Knowledge of hosting enables developers to choose the right infrastructure for their applications
d) It enables developers to configure SSL/TLS certificates correctly
e) Understanding DNS and hosting helps developers optimize website performance
f) It allows developers to manage domain names and subdomains
g) Understanding DNS and hosting helps developers troubleshoot connectivity issues