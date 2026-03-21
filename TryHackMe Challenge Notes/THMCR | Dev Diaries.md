# Summary

This room requires you to find a variety of information of the given website URL: marvenly.com based on the scenario of a freelance developer deleting the website source code and not finishing the project.
  - The subdomains of the marvenly.com domain.
  - The GitHub username of the developer.
  - The developer's email address.
  - The reason for removing the source code in the commit history.
  - The secret flag hidden in the scenario.

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
- The trick was fairly simple and just required adding .patch to the end of a GitHub commit.
  - This brings up information about the commit which generally includes the email of the person who made the commit.
  - It's here I found the email: freelancedevbycoder23@gmail.com
