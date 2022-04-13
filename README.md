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

Description: I notice that on each of the URL when viewing each salesperson theres an id= parameter which could be a potential SQLi exploit so I tried to test each URL id using ' to see if theres any response and found that blue responded with a database query failed which means SQLi attacks works on it whereas the other two just redirects you back to the other page where it listed all salesperson. So when I put ' OR SLEEP(5)=0--' in, it actually slept for the 5 seconds before loading the page.

<img src="https://user-images.githubusercontent.com/91004979/163130805-b3c96837-2489-4e14-952f-81074493d41f.gif">

Heres the part where it sleep for 5 seconds.
<img src="https://user-images.githubusercontent.com/91004979/163131324-096eb690-bb98-4785-a782-74537a0f7ece.gif">


Vulnerability #2: __________________

Description: Couldn't find it.

<img src="blue-vuln2.gif">

## Green

Vulnerability #1: Cross-Site Scripting

Description: enter any random name and email with the XSS attack in the comment/feedback section will create the attack when staff or anyone else who's able to view the feedback section. The staff will get hit by each and every one of the attacks if they were to click the ok option continuously.

<img src="https://user-images.githubusercontent.com/91004979/163120045-9748bc7f-3dad-4eef-9fe5-36f7be09a2d6.gif">

Vulnerability #2: Username Enumeration

Description: As I was testing out username enumeration I noticed that only on green the developer made it so that only users that exist would have the "Log in was unsuccessful" bold while when they don't exist, it becomes normal. Blue and red both has theirs bold no matter whether the user existed or not. Only green showed that if the user don't exist, it is not bold.

<img src="https://user-images.githubusercontent.com/91004979/163270537-dc912cda-4b1c-4361-b990-62ec88357781.gif">


## Red

Vulnerability #1: Insecure Direct Object Reference

Description: when I logged in using pperson on blue, I notice that there were two sales person with id=10 and id=11 that was not public and was only able to access 1-9 publically when I wasn't logged in. So I tried to access them on red and green as well and found that red did not prevent this information from being leaked to the public.

<img src="https://user-images.githubusercontent.com/91004979/163272273-13e53db1-ebfb-4457-9282-848ba3763f1a.gif">

Here is where I noticed there were two people I did not see on the salesperson publicly.
<img src="https://user-images.githubusercontent.com/91004979/163272386-96fa0bc4-62a0-45d7-8665-86cce6a03664.png">
Here I found that their id was 10 and 11. (heres the 11 one)
<img src="https://user-images.githubusercontent.com/91004979/163272575-2a52d46a-2509-45ee-b3ea-07fb3502f67b.png">


Vulnerability #2: CSRF(Cross-Site Request Forgery)

Description: I've tried posting each CSRF on blue, green and red but only red seem to work. In this csrf attack, I made the staff who is logged into the pperson account forcibly without consent to create a new user named "random user" once they goto the link I hosted on my github.

Gif showing this in action.
<img src="https://user-images.githubusercontent.com/91004979/163278828-a5e9b043-ae32-4f18-a97c-a14c96947d7c.gif">

Here is where I get all the variables names and other information using burp to create the CSRF by creating a test account first.
<img src="https://user-images.githubusercontent.com/91004979/163279238-e2820fbb-f61e-4ad7-b8a4-5c70acb9e393.png">

Here is my code, the highlighted part is where I change it to blue or green to tested on others but didn't work. So this only worked on red.
<img src="https://user-images.githubusercontent.com/91004979/163279434-bbc7235d-f682-489c-8baf-4ef1c7e5da89.png">


## Notes

Describe any challenges encountered while doing the work
