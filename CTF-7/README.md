# HackTheBox - Baby RE

### Analysis

![alt text](file.png)
<br>
Looking at the executable, we can see it's a Linux ELF file.

![alt text](strings.png)

I ran `strings` on the file to try and get more info, looks like they don't want me to use it for this challenge.

![alt text](ltrace.png)

Running `ltrace` on the program shows that it's looking for `abcde122313` to be entered.

![alt text](flag.png)

When we put that extracted password into the program it gives us the flag!

![alt text](end.png)

Nice, that worked!
