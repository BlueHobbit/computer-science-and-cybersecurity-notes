# Summary
-  The room covers a variety of PowerShell commands, and explains the reasoning behind and origins of PowerShell as an application. WCL stands for Windows command line. 
-  The commands I remember and what they do:
  -  get-command displays a list of every available command on the powershell including ones from external modules that have been installed and imported to the session. You can add filters to search for specific commands by type and by name amongst other things. 
  -  get-alias displays the alias's for various powershell commands which are usually equivalents in other shells such as cd or dir or ls.  
  -  get-content works in essentially the same way as type or more in WCL. 
  -  get-help gets the help page for the specified command or if run on it's own the help page for itself. -examples can be added to have examples added to the output. 
  -  set-location is basically cd but in powershell and you have to use a -path option.
  -  get-childitem is basically ls but in powershell and you have to use a -path option.
  -  find-module finds an external powershell module based on the relevant schema supplied using options like -name. -includedependencies is great with this especially when installing applications that have a lot of dependencies to rely on. 
  -  install-module installs an external module of the given critera primarily name. 

# Notes

-  I'd like to learn more about how PowerShell was originally created, I wonder if the source code is open source?

-  Powershell seems more intuitive than cmd.exe especially with the verb noun cmdlet syntax essentially making a pseudo-english interface so far.

-  Looking at the Get-Command output I'm seeing a number of commands that could be used to bypass accessing certain graphical interfaces such as the lusrmgr.msc application by running commands like New-LocalUser.
  -  I've just realized the obvious which is that the l in lusrmgr.msc stands for local, so it's local user manager.

-  Is there a manual page or similar for the get-command command since -commandtype is clearly an operator that would show me other possible operators or command types to filter by?
  - Yes there is should have read further before asking questions, you can run a command called get-help followed by the command you want help with to access the man/help page. 
  - The help pages actually look quite clear and less obfuscated behind technical jargon than some linux help pages I've attempted to read before. The command syntax is still a tad overwhelming to look at initially.

- Is powershell essentially it's own scriping language within Windows?
  - The more I read about objects and how it's possible to create certain objects like a DateTime object the more I'm reminded of coding python classes and the like and a general OOP paradigm structure to the language. I see no reason why it wouldn't be possible to sequence commands together though I don't know the syntax for that yet.

- I think I'm in love, there's a -examples option that literally shows you examples for the command. This is actually kind of crazy and feels so much easier after Linux to some degree. 
  - Ooh there's an alias command for the powershell aliases for cmd.exe commands.

- Can you still write cmd commands within the powershell application to get their desired effects?
  -  I realize this might seem a bit redundant but I wonder if there are use cases for this?
  -  Yes you can do, which does seem fairly useful as you can probably run a script of cmd.exe commands within powershell without needing to open up a separate terminal amongst other things.

- My only concern with powershell right now is that the commandlets are taking longer to type out than their equivalent commands in some cases.
  -  I'm wondering if a kind of bilinguality would be appropriate to get the fastest results taking advantage of certain commandlets that don't have strict aliases in the regular command prompt.
  -  On the other hand that could really hamper readibility of a script that was written if that's possible.
  -  I wonder if other's have had this idea and whether or not it's possible to run an application or adjusting a setting that will help autocomplete commands so that typing them out is quicker, though I should possibly avoid that function for now to make my learning more effortful.

- How extensively can pipeing be used? Can I chain commands together especially when I might want to filter and then sort for example get-childitem | where-object -property "extension" -eq ".txt" | sort-object name? 
  - So you can pipe the same object at least multiple times. I think there's a non-technical limit on this thinking about it which is that piping too many commands together is liable to get messy and reduce the understandibility of the command or script being executed.

- Definitely needed a bit of a refresher on ADS randomly turning up, I'm going to read the malware bytes article at a minimum and then do the advent of cyber room that it recommends.

-It definitely feels like there's a colossal amount of other material that could be covered that simply isn't in the scope of the room given the sheer variety of commands available and the combinatorial possibilities of piping with them. 



