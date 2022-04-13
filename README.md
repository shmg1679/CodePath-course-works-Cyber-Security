# Project 8 - Pentesting Live Targets

Time spent: **X** hours spent in total

> Objective: Identify vulnerabilities in three different versions of the Globitek website: blue, green, and red.

The six possible exploits are:

* Username Enumeration
* Insecure Direct Object Reference (IDOR)
* SQL Injection (SQLi)
* Cross-Site Scripting (XSS)
* Cross-Site Request Forgery (CSRF)
* Session Hijacking/Fixation

Each color is vulnerable to only 2 of the 6 possible exploits. First discover which color has the specific vulnerability, then write a short description of how to exploit it, and finally demonstrate it using screenshots compiled into a GIF.

## Blue

Vulnerability #1: SQLi

Description: trying to test each URL id using ' to see if theres any response and found that blue responded with a database query failed which means SQLi attacks works on it whereas the other two just redirects you back to the other page where it listed all salesperson. So when I put ' OR SLEEP(5)=0--' in, it actually slept for the 5 seconds before loading the page.

<img src="https://user-images.githubusercontent.com/91004979/163130805-b3c96837-2489-4e14-952f-81074493d41f.gif">

Heres the part where it sleep for 5 seconds.
<img src="https://user-images.githubusercontent.com/91004979/163131324-096eb690-bb98-4785-a782-74537a0f7ece.gif">


Vulnerability #2: __________________

Description:

<img src="blue-vuln2.gif">

## Green

Vulnerability #1: XSS

Description: enter any random name and email with the XSS attack in the comment/feedback section will create the attack when staff or anyone else who's able to view the feedback section. The staff will get hit by each and every one of the attacks if they were to click the ok option continuously.

<img src="https://user-images.githubusercontent.com/91004979/163120045-9748bc7f-3dad-4eef-9fe5-36f7be09a2d6.gif">

Vulnerability #2: __________________

Description: 

<img src="green-vuln2.gif">


## Red

Vulnerability #1: __________________

Description:

<img src="red-vuln1.gif">

Vulnerability #2: __________________

Description:

<img src="red-vuln2.gif">


## Notes

Describe any challenges encountered while doing the work
