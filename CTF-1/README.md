# CTF 1 - TryHackMe Basic Malware RE

### Flag 1

First, I downloaded the file from THM and opened it in Ghidra

![alt text](entry.png)

In the `entry` function we can see part of the flag is being hashed to MD5. It seems the highlighted address may be holding the flag for this challenge.

![alt text](disas.png)

At this address we can see the flag!

![alt text](flag-1.png)

Confirming this is the right flag.

### Flag 2

Upon opening the file in Ghidra, we can see a bunch of strings being pushed to the stack
![alt text](stack-string.png)

It looks like it is forming this string here.
![alt text](string.png)

Yep, that is the correct flag.
![alt text](flag-2.png)

### Flag 3

![alt text](3-entry.png)

![alt text](func-call.png)

When examining the entry function in ghidra, we can see where it gets called in the assembly.

We can also see that `LoadStringA` is passed a hardcoded value; `0x110`.

This is hex, when converted to an integer the value is `272`.

![alt text](272.png)

When we search for `272` we find what might be the flag, lets try it!

![alt text](flag-3.png)

We got the flag!
