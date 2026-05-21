Class: Computer Networks

Description: WEEK 8 – TCP vs UDP

1. Write 8 different services (for example: YouTube, Zoom, Gmail, Online Game, etc.) and for each one specify whether it uses TCP or UDP, and explain why

Youtube
Zoom
Gmail
Brawl Stars
Antigravity editor 
Yandex Music
Github
AWS

2. Explain what connection-oriented and connectionless communication mean (in your own words, 5–7 sentences)

Connection-oriented is a communication mode where the end-nodes are establishing a logical association or virtual circuit before data transfer begins. Process includes state synchronization, initializing sequence numbers and agree on optimal window size. Example of connection-oriented is TCP. 
Connectionless communication mode usually refers to UDP where data packets are sent from source to destination without establishing prior connection.


3. For the following scenarios, choose TCP or UDP and explain your choice
   - File download
   TCP as the file needs to be complete

   - Live video streaming
   UDP as in case of Live streaming missing what happened a second ago is tolerable but loss of speed and lag for complete loading are not suitable

   - Online multiplayer game
   UDP as it's more important to keep the player constantly recievinf the latest data not an outdated packet that doesn't matter anymore

   - Sending email
   TCP as there is no rush with delivering emails and even more we will need to check integrity because we don't want the email to be bugged but instead reliable 

   - Voice call (VoIP)
   UDP because while having a conversation it's convinient to miss a word or two for having smaller delay and latest data  stream also even if the packet is delivered after a delay there is no particular need to process the outdated data because it will result in glitches and lags 

4. Describe the 3 main features of TCP (reliability, ordering, retransmission) and give examples

TCP features:
- Reliablilty
   TCP makes sure that every chunck of information sent over the network is recieved by the client. In case of packet loss the server sends the lost packet again.

- Ordering
   While reliability is an essential part of TCP it would be very insufficient not to "index" the packets. Except that while sending a large file over a network some may arrive in mixed order so you would need to sort them with indexes.

- Retransmission
  If the client doesn't acknowledge that a packet was recieved the server should suppose it was lost for any reason. It once again sends the exact chunk of information that wasn't acknowledged  .

5. Describe the advantages and disadvantages of UDP (at least 3 points for each)
