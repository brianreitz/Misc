# Adaptive Threat Division Blogs
Weblogs written by members of ATD, on red teaming, penetration testing, post-exploitation techniques, and general information security.

## [@harmj0y](https://twitter.com/harmj0y)
**Blog**: harmj0y - security at the misfortune of others - http://blog.harmj0y.net

**Highlights**:

*[The Empire Strikes Back][empirestrikesback]*  
*[The "Empire" Series][empireseries]*

There are a lot of exciting features in the upcoming release of Empire 2.0, including a new command packet structure, more robust command and control, and the ability to control macOS and Linux agents (formerly of the [EmPyre][empyre] project). However, there is a tremendous amount of value in the 8-part blog series about the 1.x branch Empire, spread over several blogs, that covers the usage of Empire through all stages of an assessment.

*[Trusts You Might Have Missed][trustsmissed]*  
*[Domain Trusts: Why You Should Care][trustcare]*  
*[The Trustpocalypse][trustpocalypse]*

Three posts about Domain Trusts and Domains, which are often mistaken for a security boundary. Large Active Directory environments often use a forest of domains to segment Active Directory by business function, geographical location, or other boundaries, but these posts cover how compromising even one domain can grant access to the entire forest. After reading these posts, the importance of controlling admin access even in your small Dev domain should be readily apparent.

*[A Case Study in Attacking KeePass][kp1]*  
*[KeeThief – A Case Study in Attacking KeePass Part 2][kp2]*

Two blog posts that outline the process of identifying a valuable target for red teamers, finding an exploitable vector, and creating a tool to make exploitation much easier in the future. In this case, the target is the password manager software KeePass, often used in enterprise environments as a way to store credentials for teams.

[empirestrikesback]: http://www.harmj0y.net/blog/empire/the-empire-strikes-back/
[empireseries]: http://www.harmj0y.net/blog/empire/expanding-your-empire/
[empyre]:https://github.com/adaptivethreat/EmPyre
[trustpocalypse]: http://www.harmj0y.net/blog/redteaming/the-trustpocalypse/
[trustcare]: http://www.harmj0y.net/blog/redteaming/domain-trusts-why-you-should-care/
[trustsmissed]: http://www.harmj0y.net/blog/redteaming/trusts-you-might-have-missed/
[kp1]: http://www.harmj0y.net/blog/redteaming/a-case-study-in-attacking-keepass/
[kp2]: http://www.harmj0y.net/blog/redteaming/keethief-a-case-study-in-attacking-keepass-part-2/

## [@mattifestation](https://twitter.com/mattifestation)
**Blog**: Exploit Monday - Security Research and Esoteric PowerShell Knowledge - http://www.exploit-monday.com

**Highlights**:

*[Investigating Subversive PowerShell Profiles][pssubversive]*

A post that covers the malicious use of PowerShell profiles, which are loaded before PowerShell execution. A sneaky way to add persistence or modify code execution in a way that can throw off defenders relying solely on command-line auditing.

*[WMI Persistence using wmic.exe][wmipersist]*

A post that shows how to use wmic.exe to add WMI persistence, which is quite the esoteric command line tool. Demonstrates step-by-step how to add an EventConsumer without launching PowerShell or writing files to disk.

*[Introduction to Windows Device Guard: Introduction and Configuration Strategy][dg1]*  
*[Using Device Guard to Mitigate Against Device Guard Bypasses][dg2]*

Two posts in a series about Windows Device Guard, Microsoft's strategy to avoid unwanted code execution in upcoming releases of Windows. When configured correctly, Device Guard should be able to lock down Windows very tightly, so much so that mattifestation issued a [public challenge][dgc] to run any executable against his Surface (a challenge which he himself [found a way to defeat][dgd] within a week)

[pssubversive]:http://www.exploit-monday.com/2015/11/investigating-subversive-powershell.html
[wmipersist]:http://www.exploit-monday.com/2016/08/wmi-persistence-using-wmic.html
[dg1]:http://www.exploit-monday.com/2016/09/introduction-to-windows-device-guard.html
[dg2]:http://www.exploit-monday.com/2016/09/using-device-guard-to-mitigate-against.html
[dgc]:https://twitter.com/mattifestation/status/779521505898164224
[dgd]:https://twitter.com/mattifestation/status/780976631053586433

## [@enigma0x3](https://twitter.com/enigma0x3)
**Blog**: enigma0x3: Red Teamer and Security Addict - https://enigma0x3.net/

**Highlights**:

*[Fileless UAC Bypass Using Eventvwr.exe and Registry Hijacking][uacfileless]*  
*[Bypassing UAC on Windows 10 using Disk Cleanup][uacdisk]*

Two blog posts about UAC bypass techniques, how to move from a medium-integrity process to a high-integrity process. Beyond covering the technique itself, and the release of code, there is also an overview of the discovery process itself: using tools to find specially-privileged programs, following the execution of those programs with Process Monitoring, and using PowerShell and WMI to automatically write to disk/registry and hijack the process.

*[The "Empire" Series][empireseries]*  
*[Phishing with Empire][empirephish]*  
*[An Empire Case Study][empirecase]*

These blog posts provide detailed step-by-step instructions of a typical penetration test with Empire, covering not just the techniques used in a pentest, but the reasons to use them. Many organizations can benefit from conducting spear-phishing exercises, improving user awareness and blue team detection, and the Phishing with Empire walks through exactly how to do one. The case study shows how to overcome different operational challenges in a pentest, an key part of offensive tradecraft.

*[10 Tips for Aspiring Security Professionals][10tips]*

Life lessons from a security professional who changed the game before he was even a security professional.

[uacfileless]: https://enigma0x3.net/2016/08/15/fileless-uac-bypass-using-eventvwr-exe-and-registry-hijacking/
[uacdisk]:https://enigma0x3.net/2016/07/22/bypassing-uac-on-windows-10-using-disk-cleanup/
[empirephish]:https://enigma0x3.net/2016/03/15/phishing-with-empire/
[empirecase]:https://enigma0x3.net/2016/01/28/an-empire-case-study/
[10tips]:https://enigma0x3.net/2015/04/15/10-tips-for-aspiring-security-professionals/

## [@subtee](https://twitter.com/subTee)
**Blog**: subTee - http://subt0x10.blogspot.com/

**Highlights**:

*[Bypass Application Whitelisting Script Protections - Regsvr32.exe & COM Scriptlets][squiblydoo]*

Also known as the 'squiblydoo' attack for some reason. A technique to bypass AppLocker restrictions that leaves almost no artifacts on a machine, and one that probably brought more attention to the .sct file extension than any other post of last 15 years.

*[Bypassing Application Whitelisting using MSBuild.exe][bypassmsbuild]*

A technique to bypass application whitelisting by using MSBuild for code execution. Can be used for lateral spread (see [xorrior's code][invoke-msbuild] to do this).

*[Application Whitelisting Bypass - CSI.EXE C# Scripting][bypasscsi]*

Yet another technique to use signed Microsoft executable to execute arbitrary code in constrained environments.

[squiblydoo]:http://subt0x10.blogspot.com/2016/04/bypass-application-whitelisting-script.html
[bypassmsbuild]:http://subt0x10.blogspot.com/2016/09/bypassing-application-whitelisting.html
[bypasscsi]:http://subt0x10.blogspot.com/2016/09/application-whitelisting-bypass-csiexe.html
[invoke-msbuild]:https://github.com/xorrior/RandomPS-Scripts/blob/master/Invoke-ExecuteMSBuild.ps1

## [@bluescreenofjeff](https://twitter.com/bluscreenofjeff)/[@sw4mpf0x](https://twitter.com/Sw4mP_F0x)
**Blogs**:  
Implicit Deny - https://implicitdeny.org  
bluescreenofjeff.com - https://bluescreenofjeff.com  
Pentest Armoury - https://pentestarmoury.com/about/

**Highlights**:

*[User Creeping with WMI Events][wmicreep]*

A post demonstrating how to use WMI Event Subscriptions as a trigger to fire off attacker code. In long-running and stealthy engagements, you may want to wait for a certain user to log on to trigger some code, rather than indiscriminately fire off code, leaving indicators everywhere. PowerLurk shows proof-of-concept code that can stealthily persistence on a system.

*[Cobalt Strike HTTP C2 Redirectors with Apache mod_rewrite][apachecobalt]*  
*[Expire Phishing Links with Apache RewriteMap][apachephish]*  
*[Combatting Incident Responders with Apache mod_rewrite][apacheir]*  
*[Operating System Based Redirection with Apache mod_rewrite][apacheos]*  
*[Strengthen Your Phishing with Apache mod_rewrite and Mobile User Redirection][apachemobile]*

A series of guides to greatly improve phishing and C2 on engagements by configuring Apache. With a little bit of logic on Apache serving as a proxy to Cobalt Strike or other launchers, you can fine-tune what a user sees, depending on operating system (useful with the coming merger of Empire and EmPyre), add content or block users who poke around on your phishing domain, and redirecting mobile users to avoid suspicion.

[apachecobalt]:https://implicitdeny.org/2016/06/cobalt-strike-http-c2-redirectors-apache-mod_rewrite/
[apachephish]:https://implicitdeny.org/2016/05/expire-phishing-links-apache-rewritemap/
[apacheir]:https://implicitdeny.org/2016/04/combatting-incident-responders-apache-mod_rewrite/
[apacheos]:https://implicitdeny.org/2016/04/operating-system-based-redirection-apache-mod_rewrite/
[apachemobile]:https://implicitdeny.org/2016/03/strengthen-your-phishing-with-apache-mod_rewrite/
[wmicreep]:https://implicitdeny.org/2016/07/user-creeping-wmi-events/

## [@xorrior](https://twitter.com/xorrior)
**Blog**: Xor'd - https://www.xorrior.com/

**Highlights**:

*[The Return of the EmPyre][empyrereturn]*

An overview of persistence on Mac OS X (now called macOS) and how EmPyre uses different hijackable locations for code execution between reboots. EmPyre will be integrated into Empire 2.0, but it's handy to understand how the agents will work "under the hood". From the [EmPyre series of blog posts][empyreseries]. 

*[A Brief Usage Guide for Wmic][wmic]*

A usage guide for wmic, the command line interface for WMI on Windows. WMI has been used extensively as a post-exploitation command channel (see mattifestation's research from BlackHat and others); consult this guide if you want to manually control WMI.

[empyrereturn]:https://www.xorrior.com/the-return-of-the-empyre/
[empyreseries]:http://www.harmj0y.net/blog/empyre/building-an-empyre-with-python/
[wmic]:https://www.xorrior.com/the-return-of-the-empyre/

## [@rvrsh3ll](https://twitter.com/424f424f)
**Blog**: rvrsh3ll’s Blog, a security odyssey - http://www.rvrsh3ll.net/blog/

**Highlights**:

*[Operating with EmPyre][empyreoperating]*

A blog post that covers the use of EmPyre throughout the pentest cycle, especially for reconnaissance and lateral movement in a OS X/macOS-heavy network A good breakdown if you thought you were safe by running OS X instead of Windows in a corporate environment. From the [EmPyre series of blog posts][empyreseries]. 

*[Exploiting JBoss with Empire and PowerShell][empirejboss]*

A blog post about finding and exploiting vulnerable JBoss servers to get Empire agents. It also serves as a good example of the extensibility of Empire through modules: a PowerShell module for HTTP reconnaissance (find_fruit), a new stager to generate .war files with an Empire launcher, and the exploit_jboss module to enable easy exploitation in the future.

[empyreoperating]: http://www.rvrsh3ll.net/blog/empyre/operating-with-empyre/
[empirejboss]: http://www.rvrsh3ll.net/blog/offensive/exploiting-jboss-with-powershell-and-empire/

## [@_wald0](https://twitter.com/_wald0)
**Blog**: wald0.com - https://wald0.com/

**Highlights**:

*[Automated Derivative Administrator Search][adas]*  
*[Introducing BloodHound][bhintro]*

This is a two-post blog, so it's worth reading both of the posts that detail the theory that powers BloodHound, an Active Directory reconnaissance tool. Specifically, graph theory and Djikstra's algorithm can exhaustively find all paths between two given nodes in a graph (if they exist), and by modelling users, computers, logon sessions, and domain trusts as nodes and egdes, a pentester can find attack paths to Domain Admin.

[adas]: https://wald0.com/?p=14
[bhintro]: https://wald0.com/?p=68

## [@sixdub](https://twitter.com/sixdub)
**Blog**: @sixdub - https://www.sixdub.net/

**Highlights**:

*[Common Ground Part 1: Red Team History & Overview][cg1]*  
*[Common Ground: Planning is Key][cg2]*  
*[Common Ground Part 3: Execution and the People Factor][cg3]*

A series of posts that seeks to define the practice of Red Teaming. Nearly 10,000 words about the history of red teaming, wargaming, table top exercises, the applicability of red teaming to the present day, cyber warfare as a military doctrine, and much more. 

*[Derivative Local Admin][dla]*

A blog post about Derivative Local Admin, or how local privilege escalation can be used with lateral movement to gain even more privileges. This concept formed the basis of one of ATD's tools for mapping privileges in Active Directory, BloodHound. 

[cg1]:https://www.sixdub.net/?p=705
[cg2]:https://www.sixdub.net/?p=709
[cg3]:https://www.sixdub.net/?p=714
[dla]:https://www.sixdub.net/?p=591

## [@jaredcatkinson](https://twitter.com/jaredcatkinson)
**Blog**: Invoke-IR - http://www.invoke-ir.com

**Highlights**:

*[On the Forensic Trail - Master Boot Record (MBR)][mbr]*  
*[Forensic Fridays series][ff]*

Invoke-IR is a defense oriented blog, specifically focused on the development and use of [PowerForensics][pf], a PowerShell forensics toolkit that is fast and uses built-in Windows APIs for disk forensics. You can use it to forensically identify deleted files in MFT Slack space, pull registry keys, or perform a bit-for-bit data copy with Invoke-ForensicDD (like the Unix tool dd).

[mbr]:http://www.invoke-ir.com/2015/05/ontheforensictrail-part2.html
[ff]:http://www.invoke-ir.com/search?q=Forensic+Friday
[pf]:https://github.com/Invoke-IR/PowerForensics


*Last updated October 10, 2016*
