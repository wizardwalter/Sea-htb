I looked up the vulnerability we found:
![[Pasted image 20250309214751.png]]

so i cloned it

i am now listening with netcat on port 9001 waiting for reverse shell and the script starts http server on port 8000. Essentially the injected script will send me a reverse shell:
![[Pasted image 20250309222821.png]]

now i have tried to submit form with script but looks like there is some sort of client side security blocking me, will try with burpsuite to encode this:

.... got no where
