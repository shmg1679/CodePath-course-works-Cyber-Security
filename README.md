# WordPress

**Unit 7 finding Vulnerabilities**: 

## XSS attack
**This XSS attack will just display the user's cookie**:
1. Posting the script

<img src="https://user-images.githubusercontent.com/91004979/160264464-5bd2cd3c-67b3-4f50-a350-9e14d6beac8d.png" width="500" height="400">

2. XSS attack alert display of the user's cookie

<img src="https://user-images.githubusercontent.com/91004979/160264595-210da73b-bbc6-4223-beb0-54087dbb4d6f.png" width="700" height="400">


## User Enumeration
**Show brute forcing actually works with Burp Suite**

1. Getting the POST request by entering something random

<img src="https://user-images.githubusercontent.com/91004979/160264668-5e97b267-f120-4bec-b03b-a3c22b25c33e.png" width="500" height="400">

2. Now that I have this I'll send it to intruder

<img src="https://user-images.githubusercontent.com/91004979/160264717-fe2aed9d-c72c-49bc-8d14-779f54229979.png" width="500" height="700">

3. Set the parameter for brute forcing
<img src="https://user-images.githubusercontent.com/91004979/160264861-6b80e353-63ab-45fe-89f3-2bcbafb70155.png" width="900" height="500">

4. Found Admin and Pest which is a user I've created for testing

<img src="https://user-images.githubusercontent.com/91004979/160264916-336c0097-8ba2-482e-bc53-9745656a41ec.png" width="900" height="400">
