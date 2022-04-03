# WordPress

**Unit 7 finding Vulnerabilities**: 

## XSS Attack
**This XSS attack will just display the user's cookie**:
1. Posting the script in the comment section. Although this isn't really malicious it still show that this vulnerability exist.

<img src="https://user-images.githubusercontent.com/91004979/160264464-5bd2cd3c-67b3-4f50-a350-9e14d6beac8d.png" width="500" height="400">

2. XSS attack alert display the user's cookie when they visit the page.

<img src="https://user-images.githubusercontent.com/91004979/161449826-ff6a297a-62ff-4406-a006-8b6df886160f.gif" width="700" height="400">


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


## CSRF Attack
**Showing a simple CSRF attack if a user were to goto a link**
1. using burp to see what were the parameters I need to use to post a comment.

<img src="https://user-images.githubusercontent.com/91004979/161451511-f97b13d7-d991-40ef-922b-88336671d2de.png" width="900" height="100">

2. writing the code:

<img src="https://user-images.githubusercontent.com/91004979/161451575-051f9a68-143f-45fc-9099-ca947ca72e50.png" width="900" height="400">

3. Posting it and then wait for someone to click them. Though I'm not proficient enough in JS to make this a perfect attack so I would need to
rely on the victim's gullibleness.

<img src="https://user-images.githubusercontent.com/91004979/161451666-ae1afa87-3b45-46fa-9d4a-11e5a8f9c444.gif" width="900" height="400">








