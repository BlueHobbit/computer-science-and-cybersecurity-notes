# Summary

# Notes

- I used nslookup in one of the previous rooms as a linux command line utility to learn as part of Linux fundamentals.

- Cname records are important for multi-national companies such as Amazon which can map for instance www.amazon.co.uk to www.amazon.com.
  - I actually checked this using whois and www.amazon.co.uk is mapped onto www.amazon.com

- How are unauthorized changes to DNS server records prevented for example to stop someone from changing the MX record to their own mail server rather than a companies?

- What is tshark, is it derivative of Wireshark?

- Guidance on domain name registrant responsibilities related to the accuracy of records etc. --> https://www.icann.org/resources/pages/whois-data-accuracy-2017-06-20-en
  - No more guidance on how to actually register the domain but I'm sure the process is fairly autological.

- Using whois on a target website feels like a fairly basic recon task that I'm sure most pentesters use to some degree, though automating it would probably be easiest. 

- Are the creation dates and other dates on the whois record done with the american date arrangment or the usual one? e.g. MM/DD/YYYY vs. DD/MM/YYYY

- Yes, using telnet to get information - so very secure. Totally infallible. 

- I got bored of waiting for the telnet connection on the server's port 80 to return the result of the GET request so I just typed flag.html onto the address and then examined the page source to find the flag.

- I could really do with setting up flash cards for the memorization of some of this information such as standard and non-standard ports for different protocols such as HTTP and IMAP.
  - Quizlet would be ideal for this but it's also a paid service to do more than a bare minimum of cards from what I remember so I will have to assess.

- The numbers next to the responses represent the FTP codes for the different response. For example, 220 indicates that a new user is connecting and is sent to show that the server is ready.
  - This is similar to the HTTP codes such as the infamous error 404 code. 

- The wireshark view of the FTP exchange is very interesting as it shows that there's a translation layer between entering ls and the command that is actually sent to the server as ls becomes LIST. 
  - I notice that syntactically this is similar to HTTP's use of GET for example as it is an all caps near-english/autological command. 
  - Yes I'm correct in this idea as the same syntax/format continues with SMTP

- I remember doing another room before on TryHackMe last summer I think that went over most of these protocols but in less depth and applied them more in the context of exploits which was exciting but not as informative on reflection.

- Why is EHLO an alternative to HELO, also why omit the second L in the full word? Convenience?

- From what I remember SMTP/POP3 form an email sending/retrieval pair that represents one of the main ways of having an email box and you can have an email server that runs entirely around the protocol rather than IMAP. 
  - Moreover POP3 deletes the email from the server holding the original after it has been downloaded to the destination device, which is not particularly helpful if you want to synchronize your emails across devices. 

- Using any of these without an application handling all the actual messages/sending is really quite cumbersome but a potentially useful skill for the future though I doubt I would want to be doing this with telnet again if I had any sense of security.
  - At minimum this feels vital for having a broader understanding of what is actually going on under the hood of email clients amongst other things. 

- IMAP definitely seems more useful than POP3 though storing the emails continuously requires more storage obviously for the remote server that the email is hosted on.
  - I wonder if there are any other issues with it generally tbf. 

- What are DoT, MQTTS and SIPS?

- This is an extension for this room that goes into the TLS handshake - https://tryhackme.com/room/networksecurityprotocols
  - For some reason this room is considered outside the scope of the 101 course I'm doing despite the TLS handshake being a vital part of web security.

- Handy free TLS certificate service --> https://letsencrypt.org/

- Why would the owner of a site want to have a self-signed TLS certificate if it automatically flags the website as somewhat untrustworthy?

- I should also mention that I merged two of the rooms together in this one since they lead heavily into each other and I didn't think too hard about it. 

- I'm impressed by the intelligence of the design of TLS, having it secure existing protcols by not tampering with them but adding to the encapsulation process in essence with no influence on higher or lower protocols relative to the OSI model. 

- What are X11 and tunneling in more detail and what's the similarity to VPN aside from the idea of routing other protocols through itself?

- The challenge site included in this room for the cleartext vs. secure ports really was a "are you paying attention?" exercise.

- Which countries consider VPN's illegal?

- How do you test a VPN connection more broadly, and what is a DNS leak test?

- What is the VNC protocol?




