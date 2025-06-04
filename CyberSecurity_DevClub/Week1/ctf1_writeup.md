<h1>CTF held on 2 June 2025:</h1>

<h2>Challenges:</h2>

<h4>Welcome Agent:</h4>
<h5>We were given the ssh username, port and password and we had to simply login. After that there was a readme.txt, which could be seen by the 'cat' command.</h5>

<h4>Process Hunter:</h4>
<h5>Again log in using the given ssh username and password. Then we were told that a process was running. Using the 'ps aux' command, i saw all the running processes. Then I used the command - "cat /proc/1/cmdline | tr '\0' ' '" 
, to view the command line argument for process with PID 1 and so on. The argument in PID 1 itself contained the required flag.</h5>

<h4>Log Explore:</h4>
<h5>In this challenge, we were given a logGen file, which contained the key. I used the commands - 'chmod +x logGen' followed by './logGen', to run the file which after a few seconds gave the required key.</h5>

<h4>Locked Vault:</h4>
<h5>In this challenge we were given a .tar file with4 txt files in it. I simply opened the files in notepad and got the base64 encoded key from the step 3 file.</h5>

<h4>Hidden in the Crowd:</h4>
<h5>In this challenge I logged in using the given ssh credentials. In that we had a directory consisting of many files. After using the 'cat *' command I found out that none fo the files had the key in them. Then I used the 'ls -a' command i found hidden files which contained the flag.</h5>

<h4>Event Digger:</h4>
<h5>In this challenge, I firstly base64 decoded the given string which gave me an array of the format "var = [...]". After a bit of experimenting, I observed that if we take the numbers in the array to be ascii codes then the array gives the key of the format "dcctf{...}", which was the required key.</h5>

<h4>Dumpster Diver:</h4>
<h5>In this challenge we were given a program file, which on running showed 'Running Forever...'. I dumped the stack in which the program was running using the command - 'dump memory stack_dump.bin 0x7ffc0c1ae000 0x7ffc0c1cf000' and then searched the stack_dump.bin for the key of the form "dcCTF{...}", using the command - 'strings stack_dump.bin | grep dcCTF'</h5>
