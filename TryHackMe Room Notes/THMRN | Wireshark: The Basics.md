# Summary

# Notes
- Wireshark is one of the best packet analysis tools that seems to be around. I know a lot of forensics and troubleshooting uses it or something similar. 
  - I remember one of the guys at GR saying he used it and found out his hoover was talking to a server in China which was quite funny.

- README for creating wireshark packet dissectors --> https://github.com/boundary/wireshark/blob/master/doc/README.dissector

- Goddamit, was entering one of the flags and realized it was in American date format which is why it wasn't working. 

- Link to wireshark docs/website --> https://www.wireshark.org/docs/

- I tried looking up how to do a != (all not equal to) search in the display filter and there seems to be some conjecture over it.
  - https://www.wireshark.org/docs/wsug_html_chunked/ChWorkBuildDisplayFilterSection.html
  - The above details how to build display filters together in theory but the syntax of != or !== doesn't work on the Wireshark application I'm using.
  - What does work is putting a ! in front of the whole expression while having it be true e.g. !tcp.port == 80 gets all of the traffic that didn't happen on tcp port 80. 
    - Adding && tcp to the end of that expression further filters down to any tcp connections that didn't happen on port 80.
    - This seems potentially quite useful for checking for unauthorized connections of any type if the authorized ports are known. 

- https://tryhackme.com/room/wiresharkpacketoperations <-- This room is a lead on from the TryHackMe room that I've just finished.
  - I don't think this room is presented as the next step on this pathway but to be perfectly honest I would rather hone my skills from this room as it proved fairly dense to work through. 
