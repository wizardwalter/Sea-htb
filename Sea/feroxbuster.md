![[Pasted image 20250306214336.png]]
out from command:
```
feroxbuster -u http://10.10.11.28 -w /usr/share/wordlists/dirb/common.txt -t 50 -r
```

after running ferox buster i want to find the content management system so i run:

```
dirsearch -u http://10.10.11.28/themes/ -e php,txt,zip,log -t 40
```

![[Pasted image 20250306215537.png]]
i see i am getting more dirs within themes(this was a hint from htb), i will try to just go to these in the browser. nothing cool so far
... will try something else


i then tried:
```
feroxbuster -u http://10.10.11.28/themes -e -r -k -x php,txt,html,json -t 50
```
took forever but found this below link that returned 200 OK :D
![[Pasted image 20250306235028.png]]
![[Pasted image 20250306234348.png]]

i am asking chatGPT what the CMS could be for this :
WonderCMS came up

now again htb is asking :
What is the 2023 CVE ID for an unauthenticated cross site scripting vulnerability in WonderCMS that can lead to remote code execution?

chat gpt gave me flag:
CVE-2023-41425 
<3



