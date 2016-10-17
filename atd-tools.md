# Adaptive Threat Division Tools

Tools written and released by ATD members, with a focus on red and blue team toolkits in Windows environments. This list covers some of the well-known ones, there are many other smaller tools that I have missed here. Suggestions and updates are welcome.


## [Empire][empire]

A post-exploitation agent written in PowerShell (and soon Python) with strong command and control crypto, and a flexible command architecture. As seen in the Watch_Dogs 2 trailer. Built with modularity in mind, you can add tools and run nearly any PowerShell tool against your agents.

[empire]:https://github.com/adaptivethreat/Empire

## [EmPyre][empyre]

A post-exploitation agent written in Python for macOS and Linux environments. Empyre is planned to be merged with Empire so you can control Windows, macOS, and Linux agents from the same C2 server. Empyre supports adding custom modules and has featured contributions from the community (see this Adobe pull request from BSidesLV 2016).

[empyre]:https://github.com/adaptivethreat/EmPyre

## [PowerSploit][sploit]

A framework of PowerShell tools for penetration tests and offensive infosec work. There are tools for use at every stage of an offensive assessment, especially for custom post-exploitation operations. This project houses some of the most popular ATD tools, including:

### [PowerView][pv]

Once called "the best tool for understanding Windows networks". An Active Directory reconnaissance tool, used by pentesters to query users, groups, computers, and domain trusts on a network.

### [PowerUp][pu]

PowerShell tool that checks for privilege escalation vectors through common vulnerabilities and misconfigurations. Phishing often gets beacons from non-admin users; try using PowerUp to find a way to get a high-integrity process.

### [Invoke-Mimikatz][i-m]

A PowerShell script that loads and executes Mimikatz in memory. Originally written by Joe Bialek, Invoke-Mimikatz is a powerful tool for credential dumping and Kerberos shenanigans.

[sploit]:https://github.com/PowerShellMafia/PowerSploit
[pv]:https://github.com/PowerShellMafia/PowerSploit/tree/master/Recon
[pu]:https://github.com/PowerShellMafia/PowerSploit/tree/master/Privesc
[i-m]:https://github.com/PowerShellMafia/PowerSploit/tree/master/Exfiltration

## [BloodHound][bh]

BloodHound is a tool used to map out user and group privileges in an Active Directory domain. Based on the work done by sixdub, wald0, harmj0y, and cptjesus, BloodHound uses graph theory to map out derivative local admin on a network, showing pentesters the shortest path to Domain Admin. Immensely useful in large and complex AD environments, much faster than spraying credentials everywhere or working out paths manually. 

[bh]:https://github.com/adaptivethreat/BloodHound

## [PowerSCCM][psccm]

PowerSCCM is a Powershell interface for System Center Configuration Manager (SCCM) for offensive and defensive purposes. SCCM access usually requires high privileges, but using SCCM is very powerful and can often deploy changes to almost any machine on a network. It is often not as closely audited as other programs, making it a useful choice for stealthy operations.

[psccm]:https://github.com/PowerShellMafia/PowerSCCM


## [PowerPick][pp] and [Unmanaged PowerShell][up]

Tools created by sixdub and tifkin_ to load PowerShell into other processes, aka "PowerShell without powershell.exe". Both tools load the core PowerShell libraries into memory to bypass certain whitelisting/blacklisting techiques and can inject into other long-running processes, such as lsass or spoolsv. Unmanaged PowerShell was eventually incorporated into both Cobalt Strike's [Beacon](beecon) and Metasploit's [Meterpreter](noogie) (along with an exhortation to give tifkin_ a noogie).

[pp]:https://github.com/PowerShellEmpire/PowerTools/tree/master/PowerPick
[up]:https://github.com/leechristensen/UnmanagedPowerShell
[beecon]:http://blog.cobaltstrike.com/2016/05/18/cobalt-strike-3-3-now-with-less-powershell-exe/
[noogie]:http://buffered.io/posts/continued-meterpreter-development/

## [CimSweep][cs]

CimSweep is a tool used to run Common Information Model (CIM) and Windows Management Instrumentation (WMI) queries against a network. You can query processes, services, registry keys, files, and others out the box, and CimSweep can be extended with nearly any WMI query. It provides an abstraction to interface with WMI across many endpoints in a network.

[cs]:https://github.com/PowerShellMafia/CimSweep

## [PowerShellArsenal][psa]

PowerShell Arsenal is a collection of PowerShell tools to help reverse engineering on Windows. No need to run strings.exe when you have Get-String!

[psa]:https://github.com/mattifestation/PowerShellArsenal

## [PowerForensics][pf]

PowerForensics is a disk forensics toolkit written in PowerShell. 

[pf]:https://github.com/Invoke-IR/PowerForensics


## [Uproot][ur]

Uproot is a proof of concept for intrusion detection via WMI Event Subscriptions. It can run commands upon certain triggers, such as process creation or logon events, and actively push alerts to a central server or listening post.

[ur]:https://github.com/Invoke-IR/Uproot

# Other Tools We Love
ATD relies on the collective skill and knowledge of the infosec community to do our best work. This is just a brief list, there are far too many tools to list here...

+ Cobalt Strike by Raphael Mudge
+ Metasploit Framework
+ Mimikatz
+ Capstone Engine (Veris Group is a premier sponsor)
+ SimplyEmail
+ Responder
+ Inveigh
+ ysoserial
+ PowerUpSQL