# WordPress

**Unit 7 & 8 finding Vulnerabilities**: 

## XSS Attack
**This XSS attack will just display the user's cookie**:
1. Posting the script in the comment section. Although this isn't really malicious it still show that this vulnerability exist.

<img src="https://user-images.githubusercontent.com/91004979/160264464-5bd2cd3c-67b3-4f50-a350-9e14d6beac8d.png" width="500" height="400">

2. XSS attack alert display the user's cookie when they visit the page.

<img src="https://user-images.githubusercontent.com/91004979/161449826-ff6a297a-62ff-4406-a006-8b6df886160f.gif" width="700" height="400">

#
## User Enumeration
**Show brute forcing actually works with Burp Suite**

1. Getting the POST request by entering something random

<img src="https://user-images.githubusercontent.com/91004979/160264668-5e97b267-f120-4bec-b03b-a3c22b25c33e.png" width="500" height="400">

2. Now that I have this I'll send it to intruder

<img src="https://user-images.githubusercontent.com/91004979/160264717-fe2aed9d-c72c-49bc-8d14-779f54229979.png" width="500" height="700">

3. Set the parameter for brute forcing
<img src="https://user-images.githubusercontent.com/91004979/160264861-6b80e353-63ab-45fe-89f3-2bcbafb70155.png" width="900" height="500">

4. As you can see, I found Admin and Pest which is a user I've created for testing. These two had different length compared to others which mean 
allows me to know that they exist.

<img src="https://user-images.githubusercontent.com/91004979/160264916-336c0097-8ba2-482e-bc53-9745656a41ec.png" width="900" height="400">

5. Now trying to find the password for admin

<img src="https://user-images.githubusercontent.com/91004979/160265113-57e94fc9-b628-4b2f-98bc-c58469eaf222.png" width="900" height="400">

<img src="https://user-images.githubusercontent.com/91004979/160265142-a32af7b1-41de-435a-a79c-30bf1e225375.png" width="900" height="400">

As you can see, we now confirm that the username and password is both admin, it shows that user enumeration attack works as well as on the pest test
account below here, too. 

<img src="https://user-images.githubusercontent.com/91004979/161450211-625e094e-1b7f-4274-8a44-d1f2795554b8.png" width="900" height="400">

<img src="https://user-images.githubusercontent.com/91004979/161450188-4a205537-d3c6-49f2-8ca1-9052d94e57ee.png" width="900" height="400">

#
## CSRF Attack
**Showing a simple CSRF attack if a user were to goto a link**
1. using burp to see what were the parameters I need to use to post a comment.

<img src="https://user-images.githubusercontent.com/91004979/161451511-f97b13d7-d991-40ef-922b-88336671d2de.png" width="900" height="100">

2. writing the code:

<img src="https://user-images.githubusercontent.com/91004979/161455676-9cef2f42-d235-49a4-90ea-65d9f236b1d7.png" width="800" height="400">

3. Posting it and then wait for someone to click them. Though it seem like I'm not proficient enough in JS to figure out how to be able to
bypass this pop up to make them indirectly click the continue option so I'd need to rely on their gullibleness

<img src="https://user-images.githubusercontent.com/91004979/161455335-aabec88c-b3e4-49f5-8cd7-5a2087226f60.gif" width="900" height="400">

#
## Privilege Escalation
**After commenting and if the Admin approves your comment once, your comment will stop being pending.**

1. As you can see, this this comment is waiting for moderation

<img src="https://user-images.githubusercontent.com/91004979/161878161-ea53aada-d16e-427c-a18f-14e795bd836b.png" width="900" height="300">

2. Approving it on admin

<img src="https://user-images.githubusercontent.com/91004979/161878519-3ca7d298-a468-417d-a2af-d00545cad37b.png" width="800" height="500">

3. Now this user doesn't need to wait for moderation/approve anymore and has free reign in posting anything which will lead to being able 
to post XSS attacks.

<img src="https://user-images.githubusercontent.com/91004979/161879212-15adee63-34f1-4056-862a-fa7d6b33e62d.gif" width="900" height="400">

