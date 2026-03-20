# Summary

# Notes
I've already used active directory when I was completing my cybersecurity project setting up and hardening a Windows Server 2016 VM. 

How does the active directory authentication process work?

This is covered later in the room and uses a process called Kerberos authentication or if necessary/the system is legacy then NTLM would be used. 

What's the difference between security groups on Windows and normal user groups on Windows?

Security groups are used to allocate privileges regarding resource access whereas normal user groups are used to apply policies and more broad configuration. 

I could really do with finding some sort of memory retrieval practice software or creating my own flashcard style software. Quizlet does this but charges for a premium version - I've given it a go just now and I'm honestly quite impressed so far - it's definitely what I'm after arguably. 

Default security group list plus extra explanation --> https://learn.microsoft.com/en-us/windows-server/identity/ad-ds/manage/understand-security-groups

What are security principals? (I can kind of guess but it's better to have a formal definition to understand in the context)
  -  https://learn.microsoft.com/en-us/windows-server/identity/ad-ds/manage/understand-security-principals
  -  The security principals definition seems to be an explicit idea of AD with them representing user accounts, computer accounts, and security groups. 
  -  By this definition security groups are groups that user and computer accounts can be added to with specific resource or privilege allocations being given to them based on that group. 
  -  There also appears to be a layering of the security group mechanism to allow for inheritance of privilges and resource access from what is essentially a parent security group?

Being able to reset passwords from the active directory users and computers repository is definitely helpful.

What do the additional containers that have shown up pertain to when I enable advanced features view?

What's the formal definition of a container - it seems autological but somehow perhaps unnecessarily technical?

I think I interacted with GPO's during my cybersecurity project but I'm unsure whether I actually applied the policies created to any OU's which is weird because it would have been a clear part of the set up really. 
  -  This may have been some other form of group policy set up that I ended up dealing with but I'm not sure yet what that could have been.

Are there CLI alternatives for opening up group policy manager and the active directory respository?

What's the difference between domain and enterprise admins?

Enterprise admins are able to control the system for the enterprise (e.g. multiple trees/a forest) whereas domain admins only control their individual domain tree typically. 

Okay yeah, I've definitely interacted with group policy management in some way before as the options I'm seeing when it comes to editing the GPO's are ones I've definitely seen and modified before as part of setting up and hardening an MS Server 2016 VM.

Did I just access the group policy management editor directly in some way, is that possible?

I also remember the explain section for the different policy parts which is really helpful as always.

What is a network share in the context of SYSVOL?
  -  It's just a regular packet share but specifically used in the context of sharing the GPO's as far as I can tell.
  -  I remember setting up a network share for my networking assignment were we had to simulate a network with CISCO packet tracer and then with a virtual machine to demonstrate the ability to do other parts of it, specifically creating a shared network folder and then applying NTFS permissions to it from what I remember. 
  -  ^ I think I used powershell for it??

gpupdate /force <-- Forces group policies to be updated immediately rather than at their natural pace. The group policy update normally happens in a 90 minute cycle based on my research but I'm still not sure why this is.
  -  Okay so there's more to it than what I had initially read. The group policy doesn't wait 90 mins to be updated rather that 90 minute interval plus up to an extra 30 mins is used to handle all of the requests that lead to the GPO change being registered by computers while they are still running moreover it commits to that timeframe for any computers that are logged into during the time as the new policies are instantly applied to them (at least in theory.)

Can you interact with windows using Linux?

Yes, there's support for this apparently in the form of WSL (Windows Subsystem for Linux), it's actually really interesting as it seems to allow you to run Linux within windows itself on the same system without the use of a virual machine. There's a couple of youtube tutorials I can see that I'll have to see:
  -  https://www.google.com/url?sa=t&source=web&rct=j&opi=89978449&url=https://www.youtube.com/shorts/nPfd0921o6I&ved=2ahUKEwigw7qLqIGTAxWnRkEAHQ5ABFYQtwJ6BAgQEAI&usg=AOvVaw1qYfvBcenip77Dg6WuhBPT 

Anyway back to GPO's. 

What's a forest in AD (Is it just the name for a collection of users/computers within a domain or maybe even across individual domains)?

What does NTLM stand for?

NT LAN manager apparently though I'm not sure what NT stands for. 

How is the result of the authentication in NTLM kept secure?

How would you go about setting up a forest and the constituent trees in reality, as this doesn't seem possible in the basic active directory users and computers menu?

How are trust relationships authenticated?

How are the privileges and so on of users who are able to access another tree managed by that tree?

Ooh there's a hardening active directory room and an attacking active directory room - it would probably be best to do both as the latter informs of the kind of threats that can occur while the former should show how to defend against those threats.
  -  https://tryhackme.com/room/activedirectoryhardening
  -  https://tryhackme.com/module/hacking-active-directory (This is a whole module rather than couple of rooms so I may have to wait a bit before getting round to tackling this)

Okay I've finished this room now.
