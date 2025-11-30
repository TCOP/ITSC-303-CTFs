# Hack The Box - SpookyPass

### Analysis

This challenge is another reversing CTF. Before we begin examining the code with Ghidra, we will run `strings` and see what we find.

![alt text](strings.png)

<br>

![alt text](pass.png)

We may have found the password hardcoded into the codebase. If this is the case we won't even need to use Ghidra. Lets try it out!

![alt text](file.png)

Looks like this binary is made for Linux, I will need to swap to a new machine to run it.

![alt text](pass2.png)

Looks like the hardcoded password we found gave us the flag, lets try it out.

![alt text](flag.png)

Nice! That flag worked.
