To find the programming language used i ran gobuster command
```
gobuster dir -u http://10.10.11.28 -w /usr/share/wordlists/dirb/common.txt
```
output:
![[Pasted image 20250306214144.png]]
i see there is an index.php which lead me to know this is running php on an apache server 2.4.41

after looking at htb for hints they said check themes dir...
command ran:

```
gobuster dir -u http://10.10.11.28/themes/ -w /usr/share/wordlists/dirb/common.txt -x php,txt,log,bak
```


![[Pasted image 20250306220601.png]]

holy smokes i think we hit the jackpot! will ask chatgpt what these mean as i am new to hacking, one day i will know :D

I was suggested to curl them with case sensitivitity:
 keep getting 404s