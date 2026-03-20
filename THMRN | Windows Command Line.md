# Summary
This room feels fairly basic overall covering a broad range of basic commands without using many operators or options that are clearly more broadly available looking at the help pages for the different commands.
The room used the commands: set, ver, systeminfo, ipconfig, ipconfig /all, netstat, nslookup, ping, tracert, cd, dir, cd .., cd \Users\user, tree, help, mkdir, rmdir, type, more, echo, chkdsk, driverquery, sfc /scannow, tasklist, taskkill, shutdown.
These are all of the commands I remember. 
  -  Set on it's own shows a summary of system environmental variables such as PATH but can be used more broadly to modify, delete, and add environment variables to the system. 
  -  Ver primarily just displays the system version which was a specific version of Windows in this case
  -  systeminfo displays a broad display of system information much like the summary page of the msinfo32 application. 
  -  ipconfig displays basic networking information with the /all option displaying a broader range of information such as the specifics of the medium used to connect it to the broader network and whether Hyper-V is being used. 
  -  netstat displays all of the established network connections and listening ports on the device. However, it won't show the listening ports without using the -a flag as the command on its own will show only established connections such as the sshd connection for the room. -b shows the program associated with the room such as sshd.exe for the port 22 ssh connection. -o shows the process ids related to the connections on the device. -n displays the address information in a numerical form.
  -  nslookup literally looks up the listed mac and IP addressing information available via the DNS since it literally stands for name service lookup. It's possible to specify the name server that's being checked for the information by following the name that's being checked with that name servers IP address.
  -  ping sends a small data packet to the intended destination which is a good check for connectivity and transmission speed generally and has a number of diagnostic uses including by utilizing the other command flags which can change the formatting of the ping packet or even specify it's contents.
  -  tracert traces the route that a packet takes to arrive at it's destination by logging the TTL values being sent back by the nodes on its route. This can end up sometimes with timeout results for the requests for the TTL information which isn't massively helpful and is exactly what occured with this room.
  -  cd displays the current directory and can be used in conjunction with file paths or the . and .. shorthand to navigate between directories on a windows system. It's a generally useful command.
  -  dir displays the objects in the current or target directory such as folders and files. The /s flag can be used to display the subdirectories of the target directory as well and the /a command can be used similar to ls -a in linux to view hidden files etc. This isn't in the same graphical form provided by tree which inherently covers all of the sub directories and ignores any files since it's sole purpose is to display the directory tree.
  -  tree displays a graphical representation of the hierarchy of directories from the current or target directory. It does this until there are no more parent or child directories to be displayed.
  -  help displays help information for the relevant command but doesn't work with all commands though it will usually point you in the right direction if you use it on a command by telling you it's potential help page syntax such as /?.
  -  mkdir makes a directory with the given name at the given location
  -  rmdir removes a directory with the given name at the given location
  -  type outputs the contents of a text file but doesn't limit it unlike more which restricts the output to a single terminal page at a time with flow controls.
  -  echo echoes text back to you but is a fast way of creating a text file via the >> operator which writes the echo output to a given file.
  -  chkdsk checks the integrity of the system's disk(s) by checking for errors, poor use of space, and more.
  -  driverquery displays information for all of the installed drivers on the system such as their names and areas of function.
  -  sfc /scannow scans for corruption within the system and attempts to repair it where possible.
  -  tasklist displays every process on the target system possibly barring those that have been specifically hidden from view. Moreover, it displays the process id of each of those processes and with flags can be used to display some basic information about the process itself. There is also a handy /FI filter flag which is excellent for finding information relating to a specific process with the /? help page providing more information on the filters available to apply. 
  -  taskkill will kill a process using it's given PID or name. I believe you can also specify the exact signal to be sent to kill the process. 
  -  shutdown 
# Notes

I've already gotten started a bit here, first part was SSHing into a windows server by the looks of it. 

set --> Grabs all of the current enviroment variables on the system + can also be used to create, modify, and delete environmental variables. See: https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/set_1

ver --> displays the OS version

systeminfo --> similar to the msinfo32 executable but display the system info it summarises as text rather than in a GUI. See: https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/systeminfo

more --> displays one page of output at a time - can be used with commands like systeminfo and driverquery to minimize output to one page. 

Using [Space] is the best way to navigate down the list created by more though [Enter] can be used to go line by line instead of [Space] which goes terminal page size by terminale page size.

It's worth noting as well that | works in windows cmd for piping in the same way it works for Linux from what I can see so far. 
Is there a difference between | syntactically in Winodws CMD and Linux CLI?

mkdir is pretty much the same as the Linux equivalent as far as I can tell. I wonder if certain commands are inherited by the joint UNIX heritage of Windows and Linux. 

What's the difference between del and erase as commands? Does one have more functionality?

rmdir is also used in Linux but doesn't work very well with nested directories or directories with contents. From what I remember rm -r is better as the -r flag recursively deletes the objects and all of the hierarchal sub-objects.

The move commmand seems to work relative to the current directory, same is true for copy as I've just checked. If I use .. or . they work relative to my current directory even if the directory they are being moved/copied on isn't on the previous/next layer. 

Wonderful little tip at the end that * works as a wildcard symbol for *.txt for example. Is there a difference between it's function in Linux and it's function in Windows?
  -  I've used it plenty more times in Linux, it can be a great way for finding all the text files etc. in a directory amongst other things. 

Oh and cd\ takes you to the root directory on Windows CMD, found out by checking the MS learn page: https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/cd

What's the difference between type and more reasonably, is there any reason to use type apart from cases where I might want to view all of the text at once or more is disabled for some reason?
  -  I do find it vaguely amusing that type is nowhere near it's parralel usage in Linux where it's used to identify file types. Instead it's used like the cat command.

Progress on this room has been a lot slower as it's required a certain degree of set up everytime I want to do anywork on it and I've kept on getting interrupted. 
  -  It also generally takes longer when I'm asking lots of questions and doing more research but that has it's own indelible value. 
