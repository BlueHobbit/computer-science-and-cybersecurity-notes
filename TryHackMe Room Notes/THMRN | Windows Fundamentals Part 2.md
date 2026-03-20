TryHackMe Room Notes | Windows Fundamentals Part 2

- Already part way through with notes in my project workbook. 

What's the difference between the different memory dump/kernel dump options in the event of a system failure when looking at advanced system settings (start up and recovery)?

- Complete, kernel, and small all pertain to specific sizing of the memory dump created when the system stops unexpectedly. Complete requires a significant pagefile to be accessible and contains a full snapshot of system memory at the time of the failure. Kernel only dumps the memory in the kernel to the file and requires a noticeably smaller page file for storing the dump, this seems important for dealing with kernel specific issues that are unrelated to the functioning of the rest of the memory. A small dump is quite literally as small as possible only dumping the memory for the instruction on a thread where the failure has occurred. This gives a fairly isolated view of the issue which limits analysis, however a system that lacks significant storage space might initiate the usage of this option since a larger page file can't be created without issue or impairing functionality. 
- https://learn.microsoft.com/en-us/troubleshoot/windows-server/performance/memory-dump-file-options
- https://learn.microsoft.com/en-gb/windows-hardware/drivers/debugger/forcing-a-system-crash-from-the-keyboard
The two links above show relevant windows documentation for the memory dump file options and the second expressses how to initiate a system crash from the keyboard which I feel is interesting given the possible malware uses of such as shortcut. If possible it would seem sensible to disable this shortcut but I need to read the article further to have an idea of how to do this. 
I've read more into the second article, while a malware tool is almost certainly possible it requires registry access in the first place which is disabled on any even casually hardened windows system except for the administrator account or accounts requiring those permissions generally. Privilege escalation is probably required automatically to make the hypothetical malware usable. 

- The automatic memory dump option has most of the same information as the kernel option however in conjunction with the automatic page sizing it enables a larger page size to be created in order to accomodate the relevant information. This is temporary lasting for 4 weeks before returning back to the regular size and is an automatic process triggered by the failure if the regular page file is too small.

- What is a page file? (I already know but useful to remember)
--  A page file is virtual memory created on a drive of a windows system. 
--  The use of a page file in this context is likely to be as temporary storage for an image of the relevant memory areas for the back up before it is actually backed onto the drive itself permanently (or at least until another error occurs or another memory dump is required for another reason.)

What is windows server backup?

- It's a native backup utility specifically made for backing up windows servers. I don't remember working with this for my WindowsServer 2016 project, it was possible just too far outside of the scope though back ups would be an important part of a recovery strategy linking back to hardening the server overall.

I'm not happy with the degree of depth the room goes into with regards to the advanced systems settings or the different options for the boot tab of msconfig. The room doesn't cover for example the functionality of no GUI as a boot option and the usefulness that option can have as a diagnostic tool.

I need to do some research into VSS and volume level back ups plus back ups in general. 

Moving onto computer management, the event viewer is an important tool for troubleshooting auditing measures as well as ensuring they work especially in terms of those auditing features which are native to Windows. 
- The different types of event etc. can be viewed at: https://learn.microsoft.com/en-us/windows/win32/EventLog/about-event-logging with more resources being available via some extra exploration. 

¬ This is an event logs room specifically for windows would definitely be good to work on. 
https://tryhackme.com/room/windowseventlogs -- I'm going to do this once I get home as this laptop will struggle with the remmina + Kali vm's both being connected I suspect. 

It would be interesting to research more advanced uses of disk management in Windows.

Is there a purpose to changing or assigning a new letter to a drive? Specific use cases?

  Changing the drive letter seemingly has a number of different use cases. 
  - Drive lettering can sometimes cause conflict when a new drive like a USB is plugged in that would share the same letter as a pre-existing drive so changing the drive letter in this case can just resolve the conflict. The drive serial numbers aren't used to get around this possibility for a reason I don't know yet. It appears that at least part of what I suspected is true as it's partially human convenience since typing out long complicated serial numbers isn't great for moving between directories etc. Moreover, certain legacy software and programs are written assuming that C: will be the primary drive so a volatile serial number wouldn't work with their referencing. There's also another possibility which is that serial numbers aren't guaranteed to be unique so conflicts could still occur. I'm still left wondering why a dual system using both wouldn't have originally made sense but I suspect we've hit the point of no return on the convention being changed to some degree or other. 
  - Using drive lettering to identify the purposes for individual drives especially since it seems that drive lettering can be pre-assigned to certain types of drive could be useful like U: for a USB drive with W: and so on being used for further connections. 
  - It probably also has networking uses with shared drives between computers and in situations where a single computer has many drives such as with a server. 
  - You could also probably have windows make an error were a drive simply isn't assigned a letter and therefore doesn't appear possibly as result of some incompatibility between the drive and Windows. You could then manually assign one. 

Is there a limit on the number of drives that can be assigned letters? 

  The hard limit is 24 in accordance with number of letters that can assigned alphabetically. I wonder if there's a way to abuse this with drive partitioning creating multiple virtual drives that don't actually do anything but block other drives from being added such as a USB that could be used to download a program etc. 

What is WMI control?

What does enabling routing and remote access in compmgmt do?

¬ Hardware resources section of msinfo32 (not for average computer user -> "that sounds like a challenge and we love a challenge lol")
https://learn.microsoft.com/en-us/windows-hardware/drivers/kernel/hardware-resources - Likely worth reading in part because it has relevance to registry editing from what I can see initially. 

I need to review my knowledge of subnet masks as I'm rusty on the meaning of different mask assignments and the numbers involved.

%windir% - environment variable pointing to the source directory -- used in file paths that access system binaries (%windir%\system32)

Side note: the interchanging of \ and / for different purposes can be really irkesome at times. 

I know that registry editor is usually disabled on almost every single account on a system or network as it can be easily abused. Haven't had the chance to do anything with it yet though but I'm sure it will be interesting and there's a room for it. 

If in doubt, run msconfig and pray there's a tool for it seems like a better idea with every question I answer in this room. 

Windows registry use documentation --> docs.microsoft.com/en-us/troubleshoot/windows-server/performance/windows-registry-advanced-users (Probably useful to read this at a future point and see if I can spot any of the exploitable uses for it reasonably.)

I wonder if Microsoft offer certifications for Windows or at least there own products - that could be a neat way into a slightly specialized role while gaining good knowledge for cybersecurity and challenge usage. 

Went into regedit to take a look and nearly had a heart attack thinking there wasn't a search bar or anything but turns out there is an address bar so copying relevant addresses from Windows docs into there can be done instead of manually clicking through registry folders like a madman. 

Summary:

compmgmt, msconfig, and msinfo32 are really good commands to have at your fingertips for both configuring the computer and getting a variety of information out. 

Their functions are fairly autological: 
  - compmgmt manages or enables you to view different aspects of the system such as user groups, users, disk space and more.
  - msconfig literally allows you to configure a variety of elements within the windows system and provides a handy tool menu to find and launch other applications that can be used for more specific configuration or troubleshooting.
  - msinfo32 literally gives you a bunch of information about the system like which ports there are, drive serial numbers, CPU information, software information. The information is specifically sectioned into hardware resources, software and components with a summary at the top which opens when you first launch it.



