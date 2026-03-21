# Summary

This room requires you to find a variety of information of the given website URL: marvenly.com based on the scenario of a freelance developer deleting the website source code and not finishing the project.
  - The subdomains of the marvenly.com domain.
  - The GitHub username of the developer.
  - The developer's email address.
  - The reason for removing the source code in the commit history.
  - The secret flag hidden in the scenario.
I've already finished the room at the time of writing this but wanted to go over how I got there. 

# Notes
Subdomains:
- I initially used nslookup to see if the subdirectories were listed however this didn't work whatsoever.
- I tried whois to see if I could get any other information but this just lead to a domain holding company based in Iceland.
- I resorted after this to a quick google search using the site: syntax to search for the specific website but this only brought up a blank webpage and no subdomains.
- After trying these I resorted to using https://subdomainfinder.c99.nl/ as this is one of the better subdomain enumeration tools freely available online
  - This brought up two subdomains: admin.marvenly.com and uattesting.marvenly.com
  - I deduced that the uat testing subdomain was the development version that was the flag for this question.
 
Username:
- The username was far simpler to find as once I had the two subdomain addresses I was able to open both of them up.
- I then found a line at the bottom stating "Developed by: notvibecoder23", I entered this in and THM confirmed it was the username.
  - In future it would be better to check that a user by that name exists on GitHub first before assuming that this is the username.
  - Especially in a challenge were incorrect guesses are penalized.
 
Email:
- Amusingly I actually got the email last in this challenge room as it used a feature I wasn't initially familiar with.
- The trick was fairly simple and just required adding .patch to the end of a GitHub commit for the source code found in the username's only public repo.
  - This brings up information about the commit which generally includes the email of the person who made the commit.
  - It's here I found the email: freelancedevbycoder23@gmail.com
 
The reason for not finishing the project:
- This was fairly easy to find as well as it just required looking into the commit history for the public website repository I found by looking up the GitHub username on GitHub.
  - Worth noting this was specifically the website that the developer had originally been hired to develop in the scenario.
  - The commit history showed the reason was: "The project was marked as abandoned due to a payment dispute". This served as the flag for this question.
 
The secret message:
- So I ended up finding the secret message before I found the third and fourth flags because I simply navigated through the commits and found the commit where it was removed from later versions which was admittedly quite anti-climactic.
  - The secret message was simply THM{g1t_h1st0ry_n3v3r_f0rg3ts}.

I did a certain degree of research to complete this room as I wasn't aware about the usage of .patch | .diff for seeing the username of the developer who made the commit. Moreover, I had to look for alternative solutions for the first question after my first two attempts didn't work as expected since the domain itself wasn't registered under DNS anymore but the subdomains had been left running as far as I can tell. 
