# Summary 

# Notes
- I've used nmap before when I went through the legacy cybersecurity 101 pathway but it has been a while.

- What does the -sn option do for nmap?

- Is there a point to confirming the targets to be scanned using -sL?

- Wouldn't an incomplete TCP handshake be more of a red flag with a "stealth" scan than a complete interaction?

- Note to self: -p- takes a really loooooonnngnggg time to finish more often that not though it is thorough and I've had to do it for a CTF room before.

- The -A option is generally far more useful than running just -O or -sV but can take longer and is noisier so running the specific option for what you're looking for can be better.

- Do the different T(num) timings have set intervals because that seems more detectable or do they exist within a set range?
  - Either one could be poor since a given regular range could be flagged.

- What are recommended settings for --max-parallelism and --min-parallelism in different situations?

- Moreover, what are the recommended settings for --max-rate and --min-rate in different situations?

- What would a suitable combination of both the above sets of options such as max with max look like?

- --Host-timeout is quite useful when working with slow connections, I've had to use it before on a CTF challenge as the recommended step was using nmap so I iterated through options and increasing the time out significantly enabled the server to reply.

- What's NSE and the actual script that's run with the scan?
  - Is it a version of the script that you can run through Metasploit for version detection, if so it's probably documented?
  - NSE is the nmap scripting engine which can apparently be used to write scripts in Lua to run through nmap. A Lua script is run when the -sV option is used.

- The -d option can be quite useful when a scan isn't working but you know through a different source that the host or port is up.

- This network security module seems really good: https://tryhackme.com/module/network-security

- I'm wondering if I would be better off blitzing my way through this pathway faster than I have been and then pursuing some of these other modules that seem more in-depth and engaging.








