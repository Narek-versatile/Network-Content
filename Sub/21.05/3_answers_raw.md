Part 3: SSH

1. What is SSH used for?

SSH is used for secure shell connection over a remote network. It is used to connect to a remote server and execute commands on it.

2. Why is SSH used instead of directly accessing a server physically?

For convenience. Imagine you have servers in datacenters far away from you. You can't possibly go and plug your monitor and keyboard to all of them. 

3. What information is required to connect to a server using SSH?

You need the IP address of the server, the username, and the password. In some cases you can use an SSH key instead of a password.

4. Write an SSH command structure for connecting to a server.

ssh username@ip_address

or when connecting via key

ssh -i path/to/key.pem username@ip_address

5. Why is SSH considered secure?

SSH is considered secure because it uses cryptographic algorithms to encrypt the connection between the client and the server. This ensures that the data transmitted between the two is protected from eavesdropping and tampering.

6. What actions can be performed after connecting to a server through SSH?

any actions that the logged in user can perform. You can install software, run scripts, edit files, manage services, and etc.